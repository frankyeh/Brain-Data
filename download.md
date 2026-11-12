---
title: Download guide
---

# Download Fiber Data Hub data

### File Formats

The **Fiber Data Hub** provides compact file formats to reduce storage size. These files can be converted back to standard NIfTI format using **DSI Studio** or [Python scripts](https://dsi-studio.labsolver.org/doc/cli_data.html).

| Type | Extension | Contents | Notes |
|------|-----------|----------|--------|
| **Fib Files** | `*.fz` | Voxel-wise fiber orientation (fixels), DTI metrics (anisotropy, diffusivity), GQI metrics (QA, ISO) | **gqi.fz:** native space<br>**qsdr.fz:** MNI space |
| **SRC Files** | `*.sz` | 4D DWI volumes (after eddy/topup), includes b-table | Used as preprocessing input |
| **Database Files** | `*.dz` | Group-level DTI/GQI metrics in MNI space | Uses HCP-1065 fiber-orientation template |
| **QC Files** | `qc.tsv` | Quality-control metrics derived from `.sz` files | Tab-separated table |


### Example command line to convert files into NIFTI format

1. export diffusion metrics as NIFTI files from FIB files

```
dsi_studio --action=exp --source=subject.gqi.fz --export=dti_fa,md,rd,qa,iso
dsi_studio --action=exp --source=*.gqi.fz --export=dti_fa,md,rd,qa,iso
```

2. convert SRC files to 4D NIFTI files and bval/bvec

```
dsi_studio --action=rec --source=subject.sz --save_nii=subject_dwi.nii.gz
dsi_studio --action=rec --source=*.sz --save_nii=subject_dwi.nii.gz
```


---

### Download using Command Line (Linux / macOS — bash)

Example: download data-hcp/lifespan/hcp-ya
```bash
curl -s https://api.github.com/repos/data-hcp/lifespan/releases/tags/hcp-ya | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
```

### Download using Command Line  (Windows PowerShell 5.x)

In File Explorer you can go to a folder, click in the address bar, type `powershell` and press **Enter** to open PowerShell directly in that folder.
Example: download data-hcp/lifespan/hcp-ya
```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-hcp/lifespan/releases/tags/hcp-ya").assets | ForEach-Object { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```

### Download using DSI Studio

<img src="https://github.com/user-attachments/assets/55a16e70-09f5-4428-86bb-833e0faa84f9" width="600"/>

To make data access and analysis as seamless as possible, the Fiber Data Hub is fully integrated with DSI Studio, a comprehensive diffusion MRI and tractography software. Through DSI Studio’s graphical interface, researchers can directly download, inspect, and analyze data from the hub without additional preprocessing, saving time and computational resources. This integration allows researchers to jump-start tractography analyses using advanced tracking methods available in DSI Studio, including deterministic, probabilistic, differential, and correlational tracking.


## Example Python Code

### List all data repository (owner/repo/tag/) 

<a href="https://colab.research.google.com/github/frankyeh/Brain-Data/blob/gh-pages/list_repo.ipynb" target="_blank"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

```python
import requests
owners = ["data-hcp", "data-nih", "data-openneuro", "data-indi", "data-dandi", "data-others"]
def ft(owner, indent=""):
    repos = requests.get(f"https://api.github.com/users/{owner}/repos").json()
    print(f"{indent}{owner}/")
    for repo in repos:
        print(f"{indent}  {repo['name']}/")
        tags = requests.get(f"https://api.github.com/repos/{owner}/{repo['name']}/tags").json()
        [print(f"{indent}    {tag['name']}") for tag in tags if tag]
if __name__ == "__main__":
    [ft(owner) for owner in owners]
```


### Download fib files from repository data-hcp/lifespan/hcp-ya

<a href="https://colab.research.google.com/github/frankyeh/Brain-Data/blob/gh-pages/download_data.ipynb" target="_blank"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

```python
import requests, os, re; 
owner, repo, tag = "data-hcp", "lifespan", "hcp-ya"; # Define repo details
pattern = r".*\.fz$"; # select all .fz files 
api_url = f"https://api.github.com/repos/{owner}/{repo}/releases/tags/{tag}"; # API endpoint
def dl(u, p):
    try:
        r = requests.get(u, stream=True); r.raise_for_status(); s = int(r.headers.get('content-length', 0)); d = 0;
        with open(p, 'wb') as f:
            for c in r.iter_content(1024): f.write(c); d += len(c);
            print(f"\rDownloaded {os.path.basename(p)}: {(d/s)*100:.2f}%", end='');
        print("\nDone")
    except Exception as e: print(f"Error: {e}")
try:
    assets = requests.get(api_url).json().get('assets', []);
    [dl(asset['browser_download_url'], os.path.join(os.getcwd(), asset['name'])) for asset in assets if re.match(pattern, asset['name'])]
except Exception as e: print(f"Error fetching/processing assets: {e}")
```

### Search data using the QC report

<a href="https://colab.research.google.com/github/frankyeh/Brain-Data/blob/gh-pages/search_qc.ipynb" target="_blank"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

```python
import requests, io, pandas as pd
owner, repo, scan_name = "data-hcp", "lifespan", ""
try: assets = requests.get("https://api.github.com/repos/frankyeh/FiberDataHub/releases/tags/qc-data").json().get("assets", [])
except Exception as e: print(f"Err fetching assets: {e}"); assets = []
all_data = []
for a in assets:
    name = a["name"]
    if name.startswith(owner) and (not repo or repo in name) and name.endswith(".tsv"):
        resp = requests.get(a["browser_download_url"])
        resp.raise_for_status() # Stops if download fails
        if not (df := pd.read_csv(io.StringIO(resp.text), sep="\t", dtype=str)).empty and len(df.columns) > 0:
            filtered_df = df[df.iloc[:, 0].str.contains(scan_name, case=False, na=False)] if scan_name else df
            if not filtered_df.empty: all_data.append(filtered_df)
if all_data: pd.concat(all_data, ignore_index=True).to_csv("result_data.tsv", sep='\t', index=False); print("Saved result_data.tsv")
else: print("No data found.")
```


The Fiber Data Hub utilizes a versatile storage framework, incorporating multiple decentralized storage locations on GitHub repositories to ensure reliable data access and allow for future expansion. As new studies and datasets become available, the hub’s storage can easily scale to accommodate them, offering an ever-growing resource for the neuroimaging community. Additionally, a centralized web portal at brain.labsolver.org provides alternative access to the hub’s resources, giving researchers flexible options for data retrieval.




