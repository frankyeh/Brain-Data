# Fiber Data Hub

<img src="https://github.com/frankyeh/FiberDataHub/releases/download/qc-chart/qc_counts_combined.png" width="100%"/>

The **Fiber Data Hub** is a cloud-based platform designed to openly distribute processed fiber data derived from diffusion MRI, enabling scalable and reproducible research in brain connectivity. Currently, the Hub hosts over **40,000 processed fiber datasets**, providing comprehensive fiber information such as fiber orientation, anisotropy, diffusivities, and advanced diffusion metrics. These datasets originate from major neuroimaging initiatives, including the **Human Connectome Project (HCP)**, the **Adolescent Brain Cognitive Development (ABCD) Study**, **OpenNeuro**, and the **International Neuroimaging Data-sharing Initiative (INDI)**. By offering standardized and compact fiber data, the Hub significantly reduces computational demands, simplifies analytical workflows, and avoids redundant preprocessing. Users can explore data through an intuitive web interface featuring advanced metadata-driven search and built-in quality control measures, promoting collaboration, ensuring consistency, and supporting reproducible neuroscience research.

By consolidating curated and preprocessed fiber datasets from prominent research studies, the Fiber Data Hub enables researchers worldwide to explore brain connectivity without the need for resource-intensive data preparation. Whether studying neurodevelopment, neurological disorders, or population-level brain structure, the Fiber Data Hub offers an invaluable foundation for accelerating discoveries in neuroscience.

---

## 📁 File Formats

The **Fiber Data Hub** provides compact file formats to reduce storage size. These files can be converted back to standard NIfTI format using **DSI Studio** or [Python scripts](https://dsi-studio.labsolver.org/doc/cli_data.html).

### 🧠 Fib Files (`*.fz`)

* Stores **voxel-wise fiber orientation** (i.e., fixels), **DTI metrics** (e.g., anisotropy, diffusivity), and **GQI metrics** (e.g., QA, ISO).
* `gqi.fz`: data in **native space**
* `qsdr.fz`: data in **MNI space**

### 📦 SRC Files (`*.sz`)

* Stores **4D DWI volumes** (after eddy/topup correction)
* Includes the **b-table**

### 📊 Database Files (`*.dz`)

* Stores **group-level DTI/GQI metrics** across subjects in **MNI space**
* Uses the **HCP-1065 fiber orientation** template for alignment

### ✅ QC Files (`qc.tsv`)

* Tab-separated file with **quality control metrics** derived from `.sz` files

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

## Repository List

**If you would like to suggest a dataset, please feel free to reach out to me (frank.yeh@gmail.com). We will preprocess the data and distribute them**

- [data-hcp/lifespan](https://github.com/data-hcp/lifespan/releases)
- [data-hcp/disease](https://github.com/data-hcp/disease/releases)
- [data-nih/abcd](https://github.com/data-nih/abcd/releases)
- [data-nih/nda](https://github.com/data-nih/nda/releases)
- [data-nih/tcia](https://github.com/data-nih/tcia/releases)
- [data-openneuro/brain](https://github.com/data-openneuro/brain/releases)
- [data-openneuro/disease](https://github.com/data-openneuro/disease/releases)
- [data-openneuro/spine](https://github.com/data-openneuro/spine/releases)
- [data-openneuro/animal](https://github.com/data-openneuro/animal/releases)
- [data-indi/corr](https://github.com/data-indi/corr/releases)
- [data-indi/pro](https://github.com/data-indi/pro/releases)
- [data-indi/retro](https://github.com/data-indi/retro/releases)
- [data-others/brain](https://github.com/data-others/brain/releases)
- [data-others/disease](https://github.com/data-others/disease/releases)
- [data-others/animal](https://github.com/data-others/animal/releases)

To access the following restricted data (.sz, T1w...etc), please email me your signed NDA data use agreement. Once I receive your signed agreement, I will add you to the user list, enabling you to access the data.

- [data-hcp/lifespan-restricted (needs NDA-DUA)](https://github.com/data-hcp/lifespan-restricted/releases)
- [data-hcp/disease-restricted (needs NDA-DUA)](https://github.com/data-hcp/disease-restricted/releases)
- [data-nih/nda-restricted (needs NDA-DUA)](https://github.com/data-nih/nda-restricted/releases)

### How to Request Restricted Access

1. update DSI Studio to a version released after June 2025.
2. launch DSI Studio. When you see the login page, please right-click on the [Registry Entity]. Select [Select All], and then choose [Copy].

![image](https://github.com/user-attachments/assets/3f47933c-4701-47f1-8ecf-e666d9af2126)

3. Email your registry entity to frank.yeh@gmail.com and attached your NDA aggreement
4. We will setup your accesss and inform you. Once you restart DSI Studio, you will have access to the restricted folder.

---

## Example Code

### List all data repository (owner/repo/tag/) 

<a href="https://colab.research.google.com/github/frankyeh/Brain-Data/blob/gh-pages/list_repo.ipynb" target="_blank"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

```python
import requests
owners = ["data-hcp", "data-nih", "data-openneuro", "data-indi", "data-others"]
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

## Access from DSI Studio

<img src="https://github.com/user-attachments/assets/55a16e70-09f5-4428-86bb-833e0faa84f9" width="600"/>

To make data access and analysis as seamless as possible, the Fiber Data Hub is fully integrated with DSI Studio, a comprehensive diffusion MRI and tractography software. Through DSI Studio’s graphical interface, researchers can directly download, inspect, and analyze data from the hub without additional preprocessing, saving time and computational resources. This integration allows researchers to jump-start tractography analyses using advanced tracking methods available in DSI Studio, including deterministic, probabilistic, differential, and correlational tracking.

## Quality Control of All Datasets

<img src="https://github.com/frankyeh/FiberDataHub/releases/download/qc-chart/qc_plots.png" width="100%"/>
