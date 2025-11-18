## **OpenNeuro Preprocessed Data (>ds006000)**

OpenNeuro is a free, open platform and a BRAIN Initiative designated data archive for sharing human and non-human brain imaging data. Hosted by the Stanford Center for Reproducible Neuroscience, it aims to enhance the transparency and reproducibility of scientific research by providing openly available datasets under a Creative Commons CC0 license, which places minimal restrictions on data reuse.
Key features of OpenNeuro include:

Data Types: The archive hosts a broad range of data, including functional and structural MRI, diffusion MRI, EEG, and MEG.
Standardization: All uploaded data must adhere to the community-developed Brain Imaging Data Structure (BIDS) standard, which ensures consistent organization and metadata across datasets, making them easily reusable with various analysis tools.
Accessibility: Datasets can be accessed and downloaded via a web browser, a command-line interface, or the DataLad versioning system.
Integration: OpenNeuro partners with platforms like Brainlife.io to enable cloud-based analysis and visualization of the stored data.

### Download Commmand

Download ds006131 preprocessed DWI data

* **Linux/macOS**

```bash
curl -s https://api.github.com/repos/data-openneuro/disease/releases/tags/ds006131 | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
```

* **Windows PowerShell**

```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-openneuro/disease/releases/tags/ds006131").assets | ForEach-Object { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```

---

### Included DWI Datasets

| DS NUMBER | DWI COUNT |               Original Page            |
|-----------------|-----------------------|-------------------------------|
| ds006131 | 44 | [PAFIN: PennLINC AFfective INstability](https://openneuro.org/datasets/ds006131/) | 
| ds006395 | 182 | [Upper limb dystonia, cervical dystonia and healthy controls dataset](https://openneuro.org/datasets/ds006395/) | 
| ds006592 | 1 | [The First Comprehensive Study of Early-Emerging Prosopometamorphopsia](https://openneuro.org/datasets/ds006592/) | 
| ds006731 | 31 | [Resting state and task based functional connectivity reveal distinct mPFC and hippocampal network alterations in major depressive disorder.](https://openneuro.org/datasets/ds006731/) | 


