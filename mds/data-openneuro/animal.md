## **OpenNeuro Preprocessed Data**

OpenNeuro is a free, open platform and a BRAIN Initiative designated data archive for sharing human and non-human brain imaging data. Hosted by the Stanford Center for Reproducible Neuroscience, it aims to enhance the transparency and reproducibility of scientific research by providing openly available datasets under a Creative Commons CC0 license, which places minimal restrictions on data reuse.
Key features of OpenNeuro include:

Data Types: The archive hosts a broad range of data, including functional and structural MRI, diffusion MRI, EEG, and MEG.
Standardization: All uploaded data must adhere to the community-developed Brain Imaging Data Structure (BIDS) standard, which ensures consistent organization and metadata across datasets, making them easily reusable with various analysis tools.
Accessibility: Datasets can be accessed and downloaded via a web browser, a command-line interface, or the DataLad versioning system.
Integration: OpenNeuro partners with platforms like Brainlife.io to enable cloud-based analysis and visualization of the stored data.

### Download Commmand

Download ds001875 preprocessed DWI data

* **Linux/macOS**

```bash
curl -s https://api.github.com/repos/data-openneuro/disease/releases/tags/ds001875 | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
```

* **Windows PowerShell**

```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-openneuro/disease/releases/tags/ds001875").assets | ForEach-Object { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```

---

### Included DWI Datasets

| DS NUMBER | DWI COUNT |               Original Page            |
|-----------------|-----------------------|-------------------------------|
| ds001875 | 9 | [TheVirtualBrain Macaque MRI](https://openneuro.org/datasets/ds001875/) | 
| ds002307 | 19 | [individual_dMRI_fMRI](https://openneuro.org/datasets/ds002307/) | 
| ds002374 | 1 | [3AM straight reproducibility phantoms](https://openneuro.org/datasets/ds002374/) | 
| ds003027 | 36 | [plp_nf1_dMRI_fMRI](https://openneuro.org/datasets/ds003027/) | 
| ds003959/ | 12 | [Soma and Neurite Density MRI (SANDI) of the in-vivo mouse brain](https://openneuro.org/datasets/ds003959/) | 
| ds003989/ | 3 | [Structural, diffusion and rs-functional MRI data in Macaque Monkeys](https://openneuro.org/datasets/ds003989/) | 
| ds004161/ | 48 | [Turone Sheep Chronic Stress (TSCS)](https://openneuro.org/datasets/ds004161/) | 
| ds004305/ | 32 | [Mapping neuroinflammation in vivo with diffusion-MRI in rats given a systemic lipopolysaccharide challenge](https://openneuro.org/datasets/ds004305/) | 
| ds004441/ | 28 | [Rat_diffusion_STZ](https://openneuro.org/datasets/ds004441/) | 
| ds004632/ | 27 | [DTI readouts for designing a preclinical stem-cell therapy trial in experimental stroke](https://openneuro.org/datasets/ds004632/) | 
| ds004962/ | 28 | [MRI dataset evaluating the effect of head down tilt 15° on cerebral perfusion in acute ischemic experimental stroke](https://openneuro.org/datasets/ds004962/) | 
| ds005236/ | 59 | [Effects of environmental enrichment on brain microstructure in C58 mice (adult cohort)](https://openneuro.org/datasets/ds005236/) | 
| ds005402/ | 34 | [MPTP mouse](https://openneuro.org/datasets/ds005402/) | 
| ds005186/ | 16 | [Effects of environmental enrichment on brain microstructure in C58 mice (juvenile cohort)](https://openneuro.org/datasets/ds005186/) | 
| ds005431/ | 42 | [Animal Brain Collection Project](https://openneuro.org/datasets/ds005431/) | 
| ds006670/ | 3 | [Adulthood in vivo MRI of C57BL6J mice: T1w, RARE T2w, PDw, MTw, DWI](https://openneuro.org/datasets/ds006670/) | 
| ds006663/ | 3 | [Longitudinal in vivo MRI of C57BL6J mice: T1w, RARE T2w, PDw, MTw, DWI, BOLD rsfMRI](https://openneuro.org/datasets/ds006663/) | 


