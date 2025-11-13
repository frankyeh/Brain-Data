
The **Turone Equine Social Brain Dataset (TESBD)** is part of the **EQUISOBRAIN** project, funded by the **European Union’s Horizon 2020 Marie Skłodowska-Curie Actions (MSCA)** (project number **101033271**) and by the **Institut Français du Cheval et de l'Équitation (IFCE)**.  
It provides the first open-access **multimodal MRI dataset** of the **equine brain**, aimed at understanding the **neurobiological basis of social competences** in domestic horses (*Equus caballus*).  

TESBD combines **structural**, **functional**, and **diffusion MRI** data with rich behavioral and physiological measures, enabling translational research on animal social neuroscience.

---

## License  
Creative Commons Attribution 4.0 International (CC BY 4.0)

---

## Citation  
> Valenchon, M., Reigner, F., Lefort, G., Adriaensen, H., Barrière, P., Gesbert, A., Blard, T., Elleboudt, F., Lévy, I., Dupont, J., Uszynski, I., Poupon, C., Calandreau, L., Lansade, L., Keller, M., & Barriere, D. (2024).  
> *The Turone Equine Social Brain Dataset (TESBD)* [Data set]. Zenodo.  
> [https://doi.org/10.5281/zenodo.13969827](https://doi.org/10.5281/zenodo.13969827)

---

## Source  
> https://doi.org/10.5281/zenodo.13969827  
> Project: [EQUISOBRAIN – The Social Brain](https://cordis.europa.eu/project/id/101033271)  
> Related Dataset: [The Turone Equine Brain Templates and Atlases](https://zenodo.org/records/10731031)  
> Workflow Repository: [https://github.com/DavidBarriere/Equisobrain](https://github.com/DavidBarriere/Equisobrain)  
> Contact: [mathilde.valenchon@inrae.fr](mailto:mathilde.valenchon@inrae.fr)  
> Host institutions: INRAE, CNRS, IFCE, and University of Tours (France)

---

## Dataset Information

| Category | Details |
|-----------|----------|
| **Species** | *Equus caballus* (domestic horse) |
| **Subjects** | 23 Welsh foals (12 females, 11 males), ~7 months old |
| **Scanner** | Siemens 3 T MRI (PIXANIM platform, INRAE Val de Loire, France) |
| **Acquisition Period** | January–February 2022 |
| **Modalities** | Structural MRI, functional MRI (fMRI), diffusion MRI (dMRI) |
| **Data Format** | NIfTI, organized in **BIDS** format |
| **Analysis Tools** | FSL, SPM, MRtrix, custom scripts (Equisobrain GitHub) |
| **Behavioral Data** | Social and cognitive measures from 1–7 months of age |
| **Statistical Files** | `Equisobrain_2014.html` and `Equisobrain_2014.qmd` |
| **Project Goal** | To model social cognition and neural organization in horses |

---

## Dataset Description  

### 1. MRI Data  
High-quality **anatomical**, **functional**, and **diffusion MRI** datasets were acquired from 23 young Welsh foals.  
All data are provided in **NIfTI format** and organized according to the **BIDS standard**.  

The MRI acquisitions include:
- **Structural MRI (T1/T2)** for volumetric and morphometric analyses  
- **Functional MRI (fMRI)** for resting-state and task-free neural activity mapping  
- **Diffusion MRI (dMRI)** for white matter tractography and connectome analysis  

These MRI data were used to generate *The Turone Equine Brain Templates and Atlases* (Zenodo: [10.5281/zenodo.10731031](https://doi.org/10.5281/zenodo.10731031)).

### 2. Behavioral and Statistical Data  
The dataset also includes:
- Behavioral, physiological, and weight records collected from the same cohort  
- Statistical analyses associated with the 2025 publication (*Valenchon et al., 2025*)  
- Comprehensive reports (`Equisobrain_2014.html` and `.qmd`) summarizing modeling and regression analyses of social behaviors and MRI metrics.

---

## Purpose  

The TESBD enables cross-species comparisons and modeling of **social brain architecture** across mammals.  
Potential applications include:  
- Developing equine brain templates and atlases  
- Linking behavioral data with neuroimaging metrics  
- Comparative connectomics and interspecies brain evolution studies  
- Training AI models for animal MRI segmentation and registration  

---

## Keywords  

Equine Brain • MRI • fMRI • Diffusion MRI • BIDS • Social Cognition • Animal Neuroscience • Equisobrain • Connectome • Horse MRI • Comparative Neuroanatomy  
## Release Link
https://github.com/data-others/animal/releases/tag/ifce-tesbd
