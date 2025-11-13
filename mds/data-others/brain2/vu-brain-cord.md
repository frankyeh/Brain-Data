This dataset provides **high-quality structural and diffusion-weighted MRI** data of both the **brain and cervical spinal cord** from **11 healthy participants**, with **test–retest sessions** in 6 of them.  
It is organized in compliance with the **Brain Imaging Data Structure (BIDS v1.9.0)** and supports integrated analyses of the brain and spinal cord within the same imaging framework.

The data include **multi-shell diffusion MRI (dMRI)**, **structural (T1w, T2w, FLAIR)**, and **spinal cord–specific** contrasts (T2w, T2* mFFE), alongside a rich set of derivatives such as **model fits (DTI, NODDI, SMT, SANDI)**, **tissue and spinal cord segmentations**, **template registrations**, and **FreeSurfer reconstructions**.  
The dataset serves as a comprehensive multimodal resource for studying white matter microstructure, neuroanatomy, and cross-region connectivity throughout the central nervous system.

---

## License  
Creative Commons Attribution 4.0 International (CC BY 4.0)

---

## Citation  
> Schilling, K. (2025).  
> *Brain and Spinal Cord Multi-Shell Diffusion MRI Dataset* [Data set].  
> In *Characterization of neurite and soma organization in the brain and spinal cord with diffusion MRI* (v1.0). Zenodo.  
> [https://doi.org/10.5281/zenodo.15512428](https://doi.org/10.5281/zenodo.15512428)

---

## Source  
> https://doi.org/10.5281/zenodo.15512428  
> Contact: [kurt.schilling@vumc.org](mailto:kurt.schilling@vumc.org)  
> Institution: Vanderbilt University Medical Center  
> Project title: *Characterization of neurite and soma organization in the brain and spinal cord with diffusion MRI*  
> Funding: Supported by multiple NIH grants (K01EB030039, R03TR004434, K01EB032898, R01NS109114, R01NS117816, R01NS104149, R01EB017230)

---

## Dataset Information

| Category | Details |
|-----------|----------|
| **Subjects** | 11 healthy volunteers (6 with test–retest) |
| **Study Type** | Multi-shell diffusion MRI of brain and cervical spinal cord |
| **Organization** | BIDS v1.9.0 (brain: `acq-brain`; cord: `acq-cord`) |
| **Imaging Sites** | Brain and cervical spinal cord |
| **Data Modalities** | T1w, T2w, FLAIR, multi-shell DWI, mFFE (T2*) |
| **Reverse PE Scans** | Included for both brain and spinal cord |
| **Spinal Cord DWI Parts** | Provided as part-1, part-2, and part-3 |
| **Derived Data** | Preprocessed DWI, model fits (NODDI, SMT, SANDI, DTI, DKI), tissue/cord segmentations, FreeSurfer outputs |
| **File Structure** | `/rawdata` and `/derivatives` directories |
| **Data Standard** | Fully BIDS-compliant |

---

## Purpose

This dataset aims to support the **development, validation, and benchmarking** of imaging and analysis tools that unify brain and spinal cord studies.  
It is especially useful for research on **neurite and soma density modeling**, **multi-compartment diffusion imaging**, and **comparative neuroanatomy** across central nervous system regions.  
By including both structural and diffusion data for the brain and cord in the same cohort, this dataset enables **cross-modality, cross-region, and test–retest** investigations of tissue microstructure and connectivity.

---

## File Information

| File | Description | Size | Checksum |
|------|--------------|------|-----------|
| **Brain_Cord_MultiShell.zip** | Raw and derivative MRI data for all 11 subjects, organized in BIDS format | 34.4 GB | `md5:00589b8cbf1ed17f4f6e84a62dbf886f` |

---

## Keywords

Diffusion MRI • Multi-shell • Brain • Spinal Cord • SANDI • SMT • NODDI • Microstructure • BIDS • White Matter • Test–Retest
## Release Link
https://github.com/data-others/brain2/releases/tag/vu-brain-cord
