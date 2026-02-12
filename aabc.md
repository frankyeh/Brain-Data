# Downloading AABC from BALSA via command line (HPC / cluster)

## **Supply this instruction to yout ChatGPT and Germini to help you with the details.**

## 1) Confirm Aspera CLI is available on your cluster
You need the IBM Aspera command-line client (`ascp`). On some clusters it is provided as a module.

```bash
module load aspera-connect/3.11.0.5
which ascp
ascp -V
```

If `which ascp` fails, ask your admin to install Aspera or provide a module.

---

## 2) Obtain the “payload” (transfer spec) from BALSA
BALSA uses Aspera Connect and provides a JSON “transfer spec” (payload) that contains the file paths, host/user, ports, token, cookie, and SSH fingerprint.

1. Go to the AABC project page on BALSA and select the files you want.
2. Open Chrome DevTools → **Network** tab.
3. Click **Download** (this triggers Aspera Connect and may ask you to choose a local destination folder).
4. In DevTools → Network, find the request that starts the transfer (often called **start**).
5. Open that request and copy the **Request Payload** / **payload** JSON.
6. Save it on the cluster as a file, e.g. `payload.txt`.

**Note:** tokens can expire. If your cluster download fails with auth errors, regenerate a fresh payload.

---

## 3) Copy the Aspera Connect token-auth key to the cluster
Aspera Connect uses an “SSH-bypass” key named:

- `aspera_tokenauth_id_rsa` (passphrase-protected)

On Windows it is typically located at:

`C:\Users\<USERNAME>\AppData\Local\Programs\IBM\Aspera Connect\etc\aspera_tokenauth_id_rsa`

Copy that file to the cluster:

```bash
mkdir -p ~/.ssh
chmod 700 ~/.ssh
# copy file to ~/.ssh/aspera_tokenauth_id_rsa
chmod 600 ~/.ssh/aspera_tokenauth_id_rsa
```

---

## 4) Retrieve the passphrase used by Aspera Connect (Windows)
The key is encrypted; Aspera Connect provides the passphrase to `ascp` at runtime via the environment variable `ASPERA_SCP_PASS`.

1. Start an AABC download on Windows so `ascp.exe` is actively running.
2. Download and open Microsoft Sysinternals **Process Explorer**. (Google to find it)
3. Locate the running `ascp.exe` process.
4. Open its **Properties** → **Environment** tab.
5. Find `ASPERA_SCP_PASS` and copy its value.

On the cluster, store it in a protected file:

```bash
printf '%s\n' 'PASTE_PASSPHRASE_HERE' > ~/.ssh/aspera_pass
chmod 600 ~/.ssh/aspera_pass
```

**Security note:** Treat this like a password. Keep it private (`chmod 600`) and don’t paste it into shared documents.

---

## 5) Run the download on the cluster (recommended via SLURM)
For large downloads, avoid running on the login node. Use `sbatch` (or an interactive compute job if your site prefers that).

### A) Save this as `download_tags.sh`
```bash
#!/usr/bin/env bash
#SBATCH -J aspera_verbose
#SBATCH -N 1
#SBATCH -n 1
#SBATCH -t 72:00:00
#SBATCH -p RM
#SBATCH --array=0-15

# Usage: sbatch download_tags.sh payload.txt /path/to/download_dir

set -euo pipefail
module load aspera-connect/3.11.0.5

PAYLOAD="${1:?Usage: $0 payload.txt dest}"
DEST="${2:-$PWD}"
mkdir -p "$DEST/log"

# --- ID Setup ---
ID=${SLURM_ARRAY_TASK_ID:-0}
ASP_SESSION=$(( ID + 1 ))
ASP_TOTAL=${SLURM_ARRAY_TASK_COUNT:-16}

# --- Key Setup ---
KEY="$HOME/.ssh/aspera_tokenauth_id_rsa"
[[ -f "$KEY" ]] || { echo "ERROR: Key not found at $KEY"; exit 1; }
export ASPERA_SCP_PASS="$(< ~/.ssh/aspera_pass)"

echo "[Job $ID] Initializing Session $ASP_SESSION of $ASP_TOTAL..."

# --- Python: Hash Payload & Generate List (if needed) ---
eval "$(python3 - "$PAYLOAD" "$ID" <<'PY'
import json, base64, uuid, sys, pathlib, hashlib, os

src = pathlib.Path(sys.argv[1])
my_id = int(sys.argv[2])
d = json.loads(src.read_text())

# 1. Parse JSON
if "transfer_specs" in d:
    raw = d["transfer_specs"][0]
    ts = raw.get("transfer_spec", raw)
else:
    ts = d

# 2. Calculate Unique Hash for this Transfer Spec
spec_str = json.dumps(ts, sort_keys=True).encode("utf-8")
spec_hash = hashlib.md5(spec_str).hexdigest()[:8]
list_filename = f"file_list_{spec_hash}.txt"

# 3. Leader Logic (Job 0): Generate file ONLY if missing
if my_id == 0:
    if not os.path.exists(list_filename):
        paths = [p["source"] for p in ts.get("paths",[]) if "source" in p]
        
        # Write to temp and atomic rename to prevent race conditions
        tmp_name = f"{list_filename}.tmp"
        with open(tmp_name, "w") as f:
            f.write("\n".join(paths))
        os.rename(tmp_name, list_filename)
        print(f"echo '[Job 0] Generated new list: {list_filename}';")
    else:
        print(f"echo '[Job 0] Found existing list: {list_filename}';")

# 4. Output Variables for Bash
tags = base64.b64encode(json.dumps({"aspera":{"xfer_id":str(uuid.uuid4()),"xfer_retry":0}}).encode()).decode()

print(f'export FILE_LIST={list_filename!r}')
print(f'export ASPERA_SCP_TOKEN={ts.get("token","")!r}')
if "cookie" in ts: print(f'export ASPERA_SCP_COOKIE={ts["cookie"]!r}')
print(f'HOST={ts["remote_host"]!r}')
print(f'USER={ts["remote_user"]!r}')
print(f'CIPHER={ts.get("cipher","aes-128").replace("-","")!r}')
print(f'SSH_P={ts.get("ssh_port",33001)}')
print(f'FASP_P={ts.get("fasp_port",33001)}')
print(f'TAGS={tags!r}')
print(f'SSHFP={ts.get("sshfp","")!r}')
PY
)"

# --- Wait for Leader (if needed) ---
while [[ ! -f "$FILE_LIST" ]]; do
    echo "[Job $ID] Waiting for $FILE_LIST..."
    sleep 2
done

# --- Run Aspera (Verbose Mode) ---
# -DD = Enable Verbose Debug Logging (Level 2)
# -L  = Log Directory
echo "[Job $ID] Starting Aspera with verbose logging..."

ascp -T -l 1G -DD --mode=recv \
  --user="$USER" --host="$HOST" \
  -P "$SSH_P" -O "$FASP_P" \
  -C "${ASP_SESSION}:${ASP_TOTAL}" \
  --multi-session-threshold=0 \
  -c "$CIPHER" -k 2 --policy=fair \
  --tags64="$TAGS" \
  ${SSHFP:+--check-sshfp="$SSHFP"} \
  -i "$KEY" \
  --file-list="$FILE_LIST" \
  -L "$DEST/log" \
  "$DEST"

echo "[Job $ID] Session $ASP_SESSION finished."
```

Make it private/executable:
```bash
chmod 700 download_tags.sh
```

### B) Submit as a SLURM job (recommended)


Submit:
```bash
sbatch download_tags.sh payload.txt /path/to/download_dir
```

---

## Troubleshooting tips
- If it fails with authentication errors, your token likely expired → regenerate a fresh payload.
- If compute nodes cannot reach the Aspera host/port (firewall), you may need a transfer node or a throttled login-node download.
- Logs are in: `DEST/log/`
