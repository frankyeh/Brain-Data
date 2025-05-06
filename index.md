# Fiber Data Hub

<img src="https://github.com/frankyeh/FiberDataHub/releases/download/qc-chart/qc_counts.png" width="100%"/>

**Data Overview at Fiber Data Hub**

The Fiber Data Hub is a cloud-based resource providing immediate access to over 40,000+ preprocessed brain fiber datasets derived from diffusion MRI studies. Designed to support and accelerate tractography research, the hub hosts data from major neuroimaging projects, including the Human Connectome Project, Adolescent Brain Cognitive Development (ABCD) study, and all OpenNeuro repositories. 

# Flexible Storage and Accessibility

The Fiber Data Hub stores processed fiber orientations and diffusion metrics. This approach reduces data size by 50- to 100-fold compared to raw diffusion MRI files, allowing researchers to access high-quality, ready-to-use brain fiber data instantly.

# Currently active repositories in the Fiber Data Hub:

**If you would like to suggest a dataset, please feel free to reach out to me (frank.yeh@gmail.com). We will preprocess the data and distribute them**

- [HCP-lifespan](https://github.com/data-hcp/lifespan/releases)
- [HCP-disease](https://github.com/data-hcp/disease/releases)
- [ABCD](https://github.com/data-abcd/abcd/releases)
- [OpenNeuro](https://github.com/data-openneuro/brain/releases)
- [OpenNeuro-disease](https://github.com/data-openneuro/disease/releases)
- [OpenNeuro-spine](https://github.com/data-openneuro/spine/releases)
- [OpenNeuro-animal](https://github.com/data-openneuro/animal/releases)
- [Other major studies](https://github.com/labsolver/brain/releases)
- [Other major studies-disease](https://github.com/labsolver/disease/releases)
- [Other major studies-animal](https://github.com/labsolver/animal/releases)

<img src="https://github.com/frankyeh/FiberDataHub/releases/download/qc-chart/qc_plots.png" width="100%"/>

The Fiber Data Hub utilizes a versatile storage framework, incorporating multiple decentralized storage locations on GitHub repositories to ensure reliable data access and allow for future expansion. As new studies and datasets become available, the hub’s storage can easily scale to accommodate them, offering an ever-growing resource for the neuroimaging community. Additionally, a centralized web portal at brain.labsolver.org provides alternative access to the hub’s resources, giving researchers flexible options for data retrieval.

# Integrated with DSI Studio

<img src="https://github.com/user-attachments/assets/55a16e70-09f5-4428-86bb-833e0faa84f9" width="600"/>

To make data access and analysis as seamless as possible, the Fiber Data Hub is fully integrated with DSI Studio, a comprehensive diffusion MRI and tractography software. Through DSI Studio’s graphical interface, researchers can directly download, inspect, and analyze data from the hub without additional preprocessing, saving time and computational resources. This integration allows researchers to jump-start tractography analyses using advanced tracking methods available in DSI Studio, including deterministic, probabilistic, differential, and correlational tracking.

# Empowering the Neuroscience Community

By consolidating curated and preprocessed fiber datasets from prominent research studies, the Fiber Data Hub enables researchers worldwide to explore brain connectivity without the need for resource-intensive data preparation. Whether studying neurodevelopment, neurological disorders, or population-level brain structure, the Fiber Data Hub offers an invaluable foundation for accelerating discoveries in neuroscience.

# Example python code to search datasets in the Fiber Data Hub


```
import requests, io, pandas as pd

# Config: repo/sub_repo/scan_name. "" disables filter.
repo, sub_repo, scan_name = "data-hcp", "lifespan", ""

# Fetch assets (minimal error handling)
try: assets = requests.get("https://api.github.com/repos/frankyeh/FiberDataHub/releases/tags/qc-data").json().get("assets", [])
except Exception as e: print(f"Err fetching assets: {e}"); assets = []

# Process assets & collect data (errors stop script)
all_data = []
for a in assets:
    name = a["name"]
    # Filename check (sub_repo optional)
    if name.startswith(repo) and (not sub_repo or sub_repo in name) and name.endswith(".tsv"):
        # Download, read, filter, and append conditionally
        resp = requests.get(a["browser_download_url"])
        resp.raise_for_status() # Stops if download fails
        # Read, check, filter, and append if results found (requires Python 3.8+)
        if not (df := pd.read_csv(io.StringIO(resp.text), sep="\t", dtype=str)).empty and len(df.columns) > 0:
            filtered_df = df[df.iloc[:, 0].str.contains(scan_name, case=False, na=False)] if scan_name else df
            if not filtered_df.empty: all_data.append(filtered_df)
# Combine and save results
if all_data: pd.concat(all_data, ignore_index=True).to_csv("result_data.tsv", sep='\t', index=False); print("Saved result_data.tsv")
else: print("No data found.")
```
