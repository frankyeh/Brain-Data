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
# Aspera Download Script (token + cookie + passphrase + tags64)
# Usage:
#   ./download_tags.sh payload.txt /path/to/download_dir
#
# Assumptions:
#   - tokenauth key:  $HOME/.ssh/aspera_tokenauth_id_rsa
#   - passphrase:     $HOME/.ssh/aspera_pass
#   - payload.txt is a fresh BALSA transfer payload

set -euo pipefail

module load aspera-connect/3.11.0.5

PAYLOAD="${1:?Usage: $0 payload.txt [/path/to/download_dir]}"
DEST="${2:-$PWD}"
mkdir -p "$DEST" "$DEST/log"

ASPERA_KEY="$HOME/.ssh/aspera_tokenauth_id_rsa"
[[ -f "$ASPERA_KEY" ]] || { echo "ERROR: missing key: $ASPERA_KEY" >&2; exit 1; }
chmod 600 "$ASPERA_KEY" 2>/dev/null || true

[[ -f "$HOME/.ssh/aspera_pass" ]] || { echo "ERROR: missing passphrase file: ~/.ssh/aspera_pass" >&2; exit 1; }
export ASPERA_SCP_PASS="$(< ~/.ssh/aspera_pass)"

python3 - "$PAYLOAD" <<'PY'
import json, base64, uuid, sys, pathlib

p = pathlib.Path(sys.argv[1])
d = json.loads(p.read_text())
ts = d["transfer_specs"][0]["transfer_spec"] if "transfer_specs" in d else d

host   = ts["remote_host"]
user   = ts["remote_user"]
token  = ts.get("token","")
cookie = ts.get("cookie","")
cipher = ts.get("cipher","aes-128").replace("-","")  # aes-128 -> aes128
ssh_p  = int(ts.get("ssh_port",33001))
fasp_p = int(ts.get("fasp_port",ssh_p))
sshfp  = ts.get("sshfp","")

tags64 = base64.b64encode(
  json.dumps({"aspera":{"xfer_id":str(uuid.uuid4()),"xfer_retry":0}}).encode()
).decode()

open("file_list.txt","w").write("".join(
  item["source"] + "\n" for item in ts.get("paths",[]) if "source" in item
))

with open("vars.sh","w") as f:
  f.write(f'export ASPERA_SCP_TOKEN={token!r}\n')
  if cookie: f.write(f'export ASPERA_SCP_COOKIE={cookie!r}\n')
  f.write(f'ASPERA_HOST={host!r}\nASPERA_USER={user!r}\nASPERA_CIPHER={cipher!r}\n')
  f.write(f'ASPERA_SSH_PORT={ssh_p}\nASPERA_FASP_PORT={fasp_p}\n')
  f.write(f'ASPERA_SSHFP={sshfp!r}\nASPERA_TAGS64={tags64!r}\n')
PY

source vars.sh
[[ -s file_list.txt ]] || { echo "ERROR: file_list.txt is empty (no paths in payload)" >&2; exit 2; }

echo "Token set? $([[ -n "${ASPERA_SCP_TOKEN:-}" ]] && echo yes || echo no)"
echo "Cookie set? $([[ -n "${ASPERA_SCP_COOKIE:-}" ]] && echo yes || echo no)"
echo "Pass set?  $([[ -n "${ASPERA_SCP_PASS:-}"  ]] && echo yes || echo no)"
echo "Host/User: $ASPERA_USER@$ASPERA_HOST"
echo "Dest:      $DEST"
echo

ascp -q --mode=recv \
  --user="$ASPERA_USER" --host="$ASPERA_HOST" \
  -P "$ASPERA_SSH_PORT" -O "$ASPERA_FASP_PORT" \
  -c "$ASPERA_CIPHER" -k 2 --policy=fair \
  --precalculate-job-size \
  --file-manifest=text --file-manifest-path="$DEST/file-manifest" \
  --tags64="$ASPERA_TAGS64" \
  ${ASPERA_SSHFP:+--check-sshfp="$ASPERA_SSHFP"} \
  -i "$ASPERA_KEY" \
  --file-list=file_list.txt \
  -L "$DEST/log" \
  "$DEST"

rm -f vars.sh
echo "Done."
```

Make it private/executable:
```bash
chmod 700 download_tags.sh
```

### B) Submit as a SLURM job (recommended)
Save as `aspera_download.sbatch`:

```bash
#!/usr/bin/env bash
#SBATCH -J aspera_dl
#SBATCH -N 1
#SBATCH -n 1
#SBATCH -t 12:00:00
#SBATCH -p RM
#SBATCH -o aspera_dl.%j.out
#SBATCH -e aspera_dl.%j.err

set -euo pipefail
cd "$SLURM_SUBMIT_DIR"

DEST="/scratch/$USER/AABC"
mkdir -p "$DEST"

./download_tags.sh payload.txt "$DEST"
```

Submit:
```bash
sbatch aspera_download.sbatch
```

---

## Troubleshooting tips
- If it fails with authentication errors, your token likely expired → regenerate a fresh payload.
- If compute nodes cannot reach the Aspera host/port (firewall), you may need a transfer node or a throttled login-node download.
- Logs are in: `DEST/log/`
