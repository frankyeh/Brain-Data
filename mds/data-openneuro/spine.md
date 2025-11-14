## **OpenNeuro Preprocessed Data**

OpenNeuro is a free, open platform and a BRAIN Initiative designated data archive for sharing human and non-human brain imaging data. Hosted by the Stanford Center for Reproducible Neuroscience, it aims to enhance the transparency and reproducibility of scientific research by providing openly available datasets under a Creative Commons CC0 license, which places minimal restrictions on data reuse.
Key features of OpenNeuro include:

Data Types: The archive hosts a broad range of data, including functional and structural MRI, diffusion MRI, EEG, and MEG.
Standardization: All uploaded data must adhere to the community-developed Brain Imaging Data Structure (BIDS) standard, which ensures consistent organization and metadata across datasets, making them easily reusable with various analysis tools.
Accessibility: Datasets can be accessed and downloaded via a web browser, a command-line interface, or the DataLad versioning system.
Integration: OpenNeuro partners with platforms like Brainlife.io to enable cloud-based analysis and visualization of the stored data.

### Download Commmand

Download ds0001919 preprocessed DWI data

* **Linux/macOS**

```bash
curl -s https://api.github.com/repos/data-openneuro/disease/releases/tags/ds001919 | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
```

* **Windows PowerShell**

```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-openneuro/disease/releases/tags/ds001919").assets | ForEach-Object { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```

---

### Included DWI Datasets

| DS NUMBER | DWI COUNT |               Original Page            |
|-----------------|-----------------------|-------------------------------|
| ds001919 | 236 | [Spinal Cord MRI Public Database (Multi-subjects)](https://openneuro.org/datasets/ds001919/) | 
| ds002393 | 19 | [Spinal Cord MRI Public Database (Single-subject)](https://openneuro.org/datasets/ds002393/) | 


