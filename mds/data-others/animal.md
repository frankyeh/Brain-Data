# Animal dMRI Collections

The **Animal dMRI Collections** repository consolidates diffusion MRI (dMRI), tractography-ready derivatives, and curated documentation from a diverse set of **preclinical and non-human primate imaging studies**.
This collection brings together datasets from mice, rats, marmosets, macaques, horses, and other primate species—spanning **in vivo**, **ex vivo**, and **post-mortem** imaging.

The goal of this repository is to provide:

* **Unified access** to high-quality, openly available animal diffusion MRI datasets
* **Standardized derivative files** (`*.gqi.fz`, `*.qsdr.fz`, `*.sz`, `dti.dz`) to accelerate connectomics workflows
* **Concise summaries** of experimental design, acquisition, and metadata
* **Cross-species resources** for algorithm development, validation, and comparative neuroanatomy

All raw data remain hosted by the original publishers (Zenodo, Dryad, institutional portals). Users must follow the licensing and citation requirements specified by each dataset.


## Included Releases

### NYU Mouse Optic Pathways dMRI (`nyu-mouse`)

**Title:** In Vivo Diffusion MRI of Optic Pathways in 18 Healthy Mice  
**DOI:** https://doi.org/10.5281/zenodo.8120834  
**Species:** C57BL/6 mice (n = 18)  

**Modalities**

* Multi-shell diffusion MRI (high angular resolution)
* Manganese-enhanced T1-weighted (MEMRI) for visual pathway tracing
* Bruker raw files and converted NIfTI volumes

**Highlights**

* In vivo mapping of optic nerve, chiasm, and tract at mouse scale
* Combines MEMRI and dMRI to study structure–function of visual pathways
* Acquired at 7T with small-animal hardware
* Suitable for tractography, microstructural modeling, and validation of optic-tract pipelines

**Licensing & Use**

* License: CC BY 4.0 (see Zenodo record)
* Users must cite the Zenodo dataset DOI and associated publication if used in a manuscript.

**Download (macOS / Linux)**

```bash
curl -s https://api.github.com/repos/data-others/animal/releases/tags/nyu-mouse  | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
````

**Download (Windows PowerShell)**

```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-others/animal/releases/tags/nyu-mouse").assets | ForEach-Object { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```

---

### NKI Macaque Multimodal MRI (`nki-macaque`)

**Title:** NKI Translational Neuroscience Laboratory Macaque MRI Dataset
**DOI:** [https://doi.org/10.5281/zenodo.1303400](https://doi.org/10.5281/zenodo.1303400)
**Species:** Rhesus macaque (n = 3)

**Modalities**

* Structural MRI: T1-weighted, T2-weighted
* Diffusion MRI: multi-direction DWI
* Functional MRI: MION-contrast fMRI with multiple paradigms (rest, somatosensory, movie)

**Highlights**

* Paradigms include resting-state, somatosensory stimulation, and naturalistic movie viewing
* Designed as a translational bridge between NHP and human imaging paradigms
* Enables studies of functional networks, tractography, and structure–function coupling

**Licensing & Use**

* License: CC BY 4.0
* Cite the Zenodo DOI and associated NKI publications when using these data.

**Download (macOS / Linux)**

```bash
curl -s https://api.github.com/repos/data-others/animal/releases/tags/nki-macaque | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
```

**Download (Windows PowerShell)**

```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-others/animal/releases/tags/nki-macaque").assets | ForEach-Object { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```

---

### Rat TBI Anisotropy & Atlas Dataset (`ne-rat-tbi`)

**Title:** Use of Anisotropy, 3D Segmented Atlas, and Computational Analysis to Identify Gray Matter Subcortical Lesions Common to Concussive Injury from Different Cortical Sites (Rat)
**DOI:** [https://doi.org/10.5061/dryad.58c73](https://doi.org/10.5061/dryad.58c73)
**Species:** Rat (traumatic brain injury model)

**Modalities**

* Diffusion Tensor Imaging (DTI)
* Voxel-wise Index of Anisotropy (IA) maps
* 3D segmented brain atlas (~150 labeled regions)

**Highlights**

* Compares rostral vs. caudal cortical impact sites with convergent subcortical lesions
* Combines anisotropy metrics with a detailed 3D rat atlas
* Useful for lesion mapping, connectivity disruption assessment, and TBI modeling

**Licensing & Use**

* License: Public domain (Dryad)
* Users should still acknowledge the dataset DOI and primary paper in derived work.

**Download (macOS / Linux)**

```bash
curl -s https://api.github.com/repos/data-others/animal/releases/tags/ne-rat-tbi | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
```

**Download (Windows PowerShell)**

```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-others/animal/releases/tags/ne-rat-tbi").assets | ForEach-Object { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```

---

### Turone Equine Social Brain Dataset (TESBD) (`ifce-tesbd`)

**Title:** The Turone Equine Social Brain Dataset (TESBD)
**DOI:** [https://doi.org/10.5281/zenodo.13969827](https://doi.org/10.5281/zenodo.13969827)
**Species:** Horses (Welsh foals; n ≈ 23)

**Modalities**

* Structural MRI of the whole brain
* Functional MRI (resting-state and/or task, depending on subseries)
* Diffusion-weighted MRI for white matter pathways

**Highlights**

* First large-scale equine dataset focused on social-brain organization
* Rich ethological and behavioral metadata on social interactions and management
* Enables comparative social neuroscience across species (equine vs. human, NHP, etc.)

**Licensing & Use**

* License: CC BY 4.0
* Cite the Zenodo dataset DOI and associated TESBD publications.

**Download (macOS / Linux)**

```bash
curl -s https://api.github.com/repos/data-others/animal/releases/tags/ifce-tesbd | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
```

**Download (Windows PowerShell)**

```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-others/animal/releases/tags/ifce-tesbd").assets | ForEach-Object { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```

---

### DRCMR Axon Morphology – Monkey XNH + dMRI (`drcmr`)

**Title:** The Danish Research Centre for Magnetic Resonance (DRCMR) Axon Morphology Dataset
**Source:** [https://www.drcmr.dk/axon-morphology-dataset](https://www.drcmr.dk/axon-morphology-dataset)
**Species:** Vervet monkey

**Modalities**

* Whole-brain diffusion MRI
* X-ray nanoholotomography (XNH) of selected white matter blocks
* Histology-based ground truth for axon diameters and orientations

**Highlights**

* Canonical reference dataset for validating microstructural dMRI models (e.g., ActiveAx)
* Provides direct microscopic measurements of axonal morphology for comparison with dMRI estimates
* Supports evaluation of axon diameter mapping, dispersion, and model assumptions

**Licensing & Use**

* License: as specified by DRCMR (see official page)
* Follow DRCMR terms on redistribution and citation.

**Download (macOS / Linux)**

```bash
curl -s https://api.github.com/repos/data-others/animal/releases/tags/drcmr | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
```

**Download (Windows PowerShell)**

```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-others/animal/releases/tags/drcmr").assets | ForEach-Object { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```

---

### UW Macaque Nigrostriatal DTI Validation (`uw-macaque`)

**Title:** Validation of Diffusion Tensor Imaging Measures of Nigrostriatal Neurons in Macaques
**DOI:** [https://doi.org/10.5061/dryad.2f8j75d](https://doi.org/10.5061/dryad.2f8j75d)
**Species:** Rhesus macaque (n = 16; MPTP Parkinsonian model)

**Modalities**

* DTI of the basal ganglia and nigrostriatal pathway
* PET imaging using three ligands
* Histology: tyrosine hydroxylase (TH) cell counts and other markers

**Highlights**

* Directly compares DTI-derived metrics with histological measures of dopaminergic neuron integrity
* Validates diffusion indices as biomarkers for Parkinsonian degeneration
* Useful for biomarker development, tractography validation, and cross-modal correlation

**Licensing & Use**

* License: Public domain (Dryad)
* Cite the DOI and primary validation publication when using the dataset.

**Download (macOS / Linux)**

```bash
curl -s https://api.github.com/repos/data-others/animal/releases/tags/uw-macaque | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
```

**Download (Windows PowerShell)**

```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-others/animal/releases/tags/uw-macaque").assets | ForEach-Object { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```

---

### Utrecht Rat Cortical Connectome (Post-Mortem) (`utrecht-rat`)

**Title:** Diffusion Weighted MR Imaging of Post-Mortem Rat Brain to Allow Reconstruction of the Cortical Connectome
**DOI:** [https://doi.org/10.5281/zenodo.11119038](https://doi.org/10.5281/zenodo.11119038)
**Species:** Wistar rats (n = 10)

**Modalities**

* High-resolution diffusion MRI (~150 µm isotropic)
* Additional structural sequences (e.g., BSSFP, SPGR) depending on subseries
* Post-mortem ex vivo acquisitions at ultra-high field

**Highlights**

* Designed for high-fidelity reconstruction of the rat cortical connectome
* Long scan times and high SNR enable detailed tractography and laminar analysis
* Suitable for atlas building, connectomics, and ex vivo vs. in vivo comparisons

**Licensing & Use**

* License: CC BY 4.0
* Cite the Zenodo record and related methodological paper.

**Download (macOS / Linux)**

```bash
curl -s https://api.github.com/repos/data-others/animal/releases/tags/utrecht-rat | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
```

**Download (Windows PowerShell)**

```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-others/animal/releases/tags/utrecht-rat").assets | ForEach-Object { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```

---

### Weizmann / UNIL Forepaw Stimulation – BOLD + Diffusion (`unil-forpaw`)

**Title:** Forepaw Electrical Stimulation: MD and MK Time-Dependence vs. BOLD-fMRI
**DOI:** [https://doi.org/10.5281/zenodo.14793797](https://doi.org/10.5281/zenodo.14793797)
**Species:** Female Wistar rats (n ≈ 10)

**Modalities**

* BOLD functional MRI during forepaw electrical stimulation
* Fast kurtosis diffusion MRI across multiple diffusion times
* High-field acquisitions at 14.1 T

**Highlights**

* Joint analysis of MD (mean diffusivity), MK (kurtosis), and BOLD responses to stimulation
* Enables study of microstructural correlates of functional activation
* Useful for modeling diffusion time-dependence and neurovascular coupling

**Licensing & Use**

* License: CC BY 4.0
* Cite the DOI and associated methods paper.

**Download (macOS / Linux)**

```bash
curl -s https://api.github.com/repos/data-others/animal/releases/tags/unil-forpaw | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
```

**Download (Windows PowerShell)**

```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-others/animal/releases/tags/unil-forpaw").assets | ForEach-Object { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```

---

### Brain/MINDS Marmoset MRI – In Vivo (`riken-marmoset`)

**Title:** Brain/MINDS Marmoset Brain MRI Dataset (In Vivo, NA216)
**DOI:** [https://doi.org/10.24475/bminds.mri.thj.4624](https://doi.org/10.24475/bminds.mri.thj.4624)
**Species:** Common marmoset (Callithrix jacchus; n ≈ 455 in vivo)

**Modalities**

* Structural MRI: T1-weighted, T2-weighted
* Diffusion MRI: multi-shell dMRI and derived DTI metrics
* Resting-state fMRI (subset of animals)

**Highlights**

* Largest in vivo marmoset MRI resource available to date
* Standardized acquisition and preprocessing across a large cohort
* Supports connectome construction, lifespan analysis, and cross-species comparisons

**Licensing & Use**

* License: CC BY 4.0
* Cite the Brain/MINDS MRI data descriptor and DOI when using the resource.

**Download (macOS / Linux)**

```bash
curl -s https://api.github.com/repos/data-others/animal/releases/tags/riken-marmoset | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
```

**Download (Windows PowerShell)**

```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-others/animal/releases/tags/riken-marmoset").assets | ForEach-Object { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```

---

### Brain/MINDS Marmoset MRI – Ex Vivo (`riken-marmoset-exvivo`)

**Title:** Brain/MINDS Marmoset Brain MRI Dataset eNA91 (Ex Vivo)
**DOI:** [https://doi.org/10.24475/bminds.mri.thj.4624](https://doi.org/10.24475/bminds.mri.thj.4624) (ex vivo subset)
**Species:** Common marmoset (Callithrix jacchus; n ≈ 91 ex vivo)

**Modalities**

* High-resolution ex vivo structural MRI
* Ex vivo diffusion MRI for fine-scale tractography
* Derived DTI/ODF metrics and template registrations (depending on release)

**Highlights**

* Mesoscale mapping of marmoset connectivity with long ex vivo acquisitions
* Ideal for building high-resolution templates and tract atlases
* Complements the NA216 in vivo cohort for multi-contrast studies

**Licensing & Use**

* License: CC BY 4.0
* Cite the Brain/MINDS ex vivo subset and associated publications.

**Download (macOS / Linux)**

```bash
curl -s https://api.github.com/repos/data-others/animal/releases/tags/riken-marmoset-exvivo | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
```

**Download (Windows PowerShell)**

```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-others/animal/releases/tags/riken-marmoset-exvivo").assets | ForEach-Object { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```

---

### PRIME-DE Rhesus – Structural T1/T2 (`prime-de-rhesus-t1t2`)

**Title:** PRIMatE Data Exchange (T1W/T2W Structural Subset)
**Source:** [https://fcon_1000.projects.nitrc.org/indi/indiPRIME.html](https://fcon_1000.projects.nitrc.org/indi/indiPRIME.html)
**Species:** Rhesus macaque across multiple sites

**Modalities**

* T1-weighted structural MRI
* T2-weighted structural MRI
* Site-specific acquisition protocols aggregated under PRIME-DE

**Highlights**

* Structural-only subset useful for morphometry, registration, and atlas work
* Multi-site variability enables harmonization and cross-site evaluation
* Often used as the structural backbone for combining with other NHP datasets

**Licensing & Use**

* License: CC BY-NC-SA (see PRIME-DE terms)
* Users must follow PRIME-DE usage policies and acknowledge contributing sites.

**Download (macOS / Linux)**

```bash
curl -s https://api.github.com/repos/data-others/animal/releases/tags/prime-de-rhesus-t1t2 | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
```

**Download (Windows PowerShell)**

```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-others/animal/releases/tags/prime-de-rhesus-t1t2").assets | ForEach-Object { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```

---

### PRIME-DE Global Collections (`prime-de-rhesus`)

**Title:** PRIMatE Data Exchange (PRIME-DE) – Global NHP Collections
**Source:** [https://fcon_1000.projects.nitrc.org/indi/indiPRIME.html](https://fcon_1000.projects.nitrc.org/indi/indiPRIME.html)
**Species:** Multiple macaque cohorts across international sites

**Modalities**

* Structural MRI (T1/T2)
* Resting-state fMRI
* Diffusion MRI (site-dependent)
* Additional modalities at some sites (task fMRI, etc.)

**Highlights**

* Flagship NHP neuroimaging consortium dataset
* Facilitates large-scale cross-site and cross-cohort analyses
* Widely used for network neuroscience, harmonization, and comparative work

**Licensing & Use**

* License: CC BY-NC-SA
* Follow PRIME-DE data usage agreements and site-specific restrictions.

**Download (macOS / Linux)**

```bash
curl -s https://api.github.com/repos/data-others/animal/releases/tags/prime-de-rhesus | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
```

**Download (Windows PowerShell)**

```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-others/animal/releases/tags/prime-de-rhesus").assets | ForEach-Object { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```

---

### Pittsburgh Marmoset Connectivity Atlas Derivatives (`pitt-marmoset`)

**Title:** University of Pittsburgh Marmoset In Vivo Images and Connectivity Derivatives
**Source:** Marmoset Brain Connectivity Atlas and associated imaging collections
**Species:** Common marmoset (Callithrix jacchus)

**Modalities**

* In vivo structural MRI and diffusion MRI
* Tracer-based connectivity registered into MRI template space
* Warp fields, injection site masks, and projection density maps

**Highlights**

* Bridges tracer-based mesoscale connectivity with MRI templates
* Enables tractography validation and structural–tracer comparisons
* Curated for integration with DSI Studio and other connectomics tools

**Licensing & Use**

* Base imagery and tracer data: CC BY 4.0 (atlas)
* Derived files: see repository LICENSE and atlas terms

**Download (macOS / Linux)**

```bash
curl -s https://api.github.com/repos/data-others/animal/releases/tags/pitt-marmoset | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
```

**Download (Windows PowerShell)**

```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-others/animal/releases/tags/pitt-marmoset").assets | ForEach-Object { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```

---

### Oxford WIN Macaque – Post-Mortem dMRI (`oxford-win-macaque`)

**Title:** University of Oxford WIN Macaque Post-Mortem MRI
**Species:** Rhesus macaque (n ≈ 6)

**Modalities**

* Post-mortem diffusion MRI at ~0.6 mm isotropic resolution (7T)
* High b-value, long diffusion times
* Structural MRI for anatomical reference

**Highlights**

* High-SNR, high-resolution ex vivo dMRI optimized for tractography
* Useful for validating in vivo tractography and building macaque white matter atlases
* Part of the broader Oxford WIN NHP imaging program

**Licensing & Use**

* License: CC BY-NC-SA (see source documentation)
* Cite the relevant Oxford WIN publications and dataset documentation.

**Download (macOS / Linux)**

```bash
curl -s https://api.github.com/repos/data-others/animal/releases/tags/oxford-win-macaque | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
```

**Download (Windows PowerShell)**

```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-others/animal/releases/tags/oxford-win-macaque").assets | ForEach-Object { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```

---

### Primate Brain Bank MRI (`oxford-pbb`)

**Title:** Primate Brain Bank MRI (NIN / Oxford collaboration)
**DOI:** [https://doi.org/10.5281/zenodo.5044936](https://doi.org/10.5281/zenodo.5044936)
**Species:** Seven primate species (e.g., macaque, marmoset, baboon, etc.)

**Modalities**

* Structural MRI for multiple post-mortem primate brains
* Diffusion MRI for selected specimens
* Precomputed cortical surfaces, label maps, and connectomes (depending on species)

**Highlights**

* Cross-species MRI resource enabling evolutionary and comparative connectomics
* Shared processing pipelines across species for homologous comparisons
* Valuable for testing multi-species registration and graph analysis tools

**Licensing & Use**

* License: CC BY 4.0
* Cite the Zenodo DOI and the primate brain bank data descriptor.

**Download (macOS / Linux)**

```bash
curl -s https://api.github.com/repos/data-others/animal/releases/tags/oxford-pbb | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
```

**Download (Windows PowerShell)**

```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-others/animal/releases/tags/oxford-pbb").assets | ForEach-Object { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```
