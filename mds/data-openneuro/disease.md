## **OpenNeuro Preprocessed Data**

OpenNeuro is a free, open platform and a BRAIN Initiative designated data archive for sharing human and non-human brain imaging data. Hosted by the Stanford Center for Reproducible Neuroscience, it aims to enhance the transparency and reproducibility of scientific research by providing openly available datasets under a Creative Commons CC0 license, which places minimal restrictions on data reuse.
Key features of OpenNeuro include:

Data Types: The archive hosts a broad range of data, including functional and structural MRI, diffusion MRI, EEG, and MEG.
Standardization: All uploaded data must adhere to the community-developed Brain Imaging Data Structure (BIDS) standard, which ensures consistent organization and metadata across datasets, making them easily reusable with various analysis tools.
Accessibility: Datasets can be accessed and downloaded via a web browser, a command-line interface, or the DataLad versioning system.
Integration: OpenNeuro partners with platforms like Brainlife.io to enable cloud-based analysis and visualization of the stored data.

### Download Commmand

Download ds001226 preprocessed DWI data

* **Linux/macOS**

```bash
curl -s https://api.github.com/repos/data-openneuro/disease/releases/tags/ds001226 | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
```

* **Windows PowerShell**

```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-openneuro/disease/releases/tags/ds001226").assets | ForEach-Object { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```

---

### Included DWI Datasets

| DS NUMBER | DWI COUNT |               Original Page            |
|-----------------|-----------------------|-------------------------------|
| ds001226 | 36 | [BTC_preop](https://openneuro.org/datasets/ds001226/) | 
| ds001378 | 50 | [SCA2 Diffusion Tensor Imaging](https://openneuro.org/datasets/ds001378/) | 
| ds001743 | 12 | [Unilateral Glaucoma 3T dMRI](https://openneuro.org/datasets/ds001743/) | 
| ds001907 | 16 | [ANT: Healthy aging and Parkinson's disease](https://openneuro.org/datasets/ds001907/) | 
| ds001928 | 40 | [Functional Connectivity of Music-Induced Analgesia in Fibromyalgia](https://openneuro.org/datasets/ds001928/) | 
| ds002080 | 29 | [BTC_postop](https://openneuro.org/datasets/ds002080/) | 
| ds003037 | 149 | [SUDMEX_TMS: The Mexican dataset of an rTMS clinical trial on cocaine use disorder patients.](https://openneuro.org/datasets/ds003037/) |
| ds003367/ | 49 | [Ascending arousal network connectivity during recovery from traumatic coma](https://openneuro.org/datasets/ds003367/) | 
| ds003346/ | 136 | [SUDMEX_CONN: The Mexican dataset of cocaine use disorder patients.](https://openneuro.org/datasets/ds003346/) | 
| ds003599/ | 133 | [White matter deficits in cocaine use disorder V1.0](https://openneuro.org/datasets/ds003599/) | 
| ds004498/ | 7 | [Perinatal Stroke](https://openneuro.org/datasets/ds004498/) | 
| ds004717/ | 42 | [Utilizing Amide Proton Transfer Technique to Characterise Diffuse Gliomas Based on WHO 2021 Classification of CNS Tumors](https://openneuro.org/datasets/ds004717/) | 
| ds004884/ | 613 | [Aphasia Recovery Cohort (ARC) Dataset](https://openneuro.org/datasets/ds004884/) | 
| ds004889/ | 1715 | [Stroke Outcome Optimization Project (SOOP)](https://openneuro.org/datasets/ds004889/) | 
| ds004910/ | 134 | [An open relaxation-diffusion MRI dataset in neurosurgical studies](https://openneuro.org/datasets/ds004910/) | 
| ds005026/ | 82 | [Hearing loss Connectome](https://openneuro.org/datasets/ds005026/) | 
| ds005063/ | 1 | [CR DBS](https://openneuro.org/datasets/ds005063/) | 


