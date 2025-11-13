# **Enhanced Nathan Kline Institute–Rockland Sample (NKI-RS) – Multiband Imaging Test–Retest Pilot Dataset**
The **Enhanced NKI-Rockland Sample (NKI-RS)** represents an expanded, community-based neuroimaging initiative designed to map **brain development, maturation, and aging** across the human lifespan (ages 6–85 years). Building upon the original NKI-RS project, this enhanced version combines **state-of-the-art multiband imaging**, **deep phenotyping**, and **open-access data sharing** to provide one of the most comprehensive resources for studying individual differences in brain structure and function.

The **Multiband Imaging Test–Retest Pilot Dataset** served as the preliminary phase for the enhanced NKI-RS project. It was specifically designed to evaluate the **reliability and reproducibility** of advanced multiband resting-state fMRI (R-fMRI) and diffusion tensor imaging (DTI) protocols before their implementation in the full-scale 1,000-participant study. Participants were primarily drawn from the original NKI-RS cohort, with corresponding psychiatric and phenotypic data available (individuals were not excluded for clinical history).

The pilot dataset includes **repeated R-fMRI and DTI sessions**, as well as **task-based calibration scans** for assessing image quality, vascular reactivity, and motion effects:
- **Visual checkerboard stimulation** (contrast-to-noise calibration)  
- **Breath-holding task** (vascular responsiveness)  
- **Eye-movement calibration** (motion-related artifact detection)

---

## Overview

- **Dataset name:** Enhanced NKI-RS – Multiband Imaging Test–Retest Pilot Dataset  
- **Institution:** Nathan Kline Institute for Psychiatric Research (NKI), Orangeburg, NY, USA  
- **Principal Investigator:** Michael Milham  
- **DOI:** [10.15387/fcp_indi.corr.nki1](http://dx.doi.org/10.15387/fcp_indi.corr.nki1)  
- **Sample:** Adults from the original NKI-RS cohort  
- **Modalities:** R-fMRI, multiband R-fMRI, DTI, task-based fMRI (checkerboard, breath-hold, eye-movement)  
- **Purpose:** Evaluate test–retest reliability of multiband imaging protocols  

---

## Imaging Protocol

**Repeated scans (test–retest):**
| Sequence | TR | Voxel Size | Duration | Purpose |
|-----------|----|-------------|-----------|----------|
| R-mfMRI | 645 ms | 3 mm isotropic | 10 min | High temporal resolution |
| R-mfMRI | 1400 ms | 2 mm isotropic | 10 min | High spatial resolution |
| R-fMRI | 2500 ms | 3 mm isotropic | 5 min | Standard EPI reference |
| DTI | 137 directions | 2 mm isotropic | — | White matter microstructure |

**Single-acquisition scans:**
| Task | TR | Voxel Size | Duration |
|------|----|-------------|-----------|
| Visual Checkerboard | 645 ms / 1400 ms | 3 mm / 2 mm | 2.5 min |
| Eye-Movement Calibration | 645 ms / 1400 ms | 3 mm / 2 mm | 2.5 min |
| Breath Holding | 1400 ms | 2 mm isotropic | 10 min |

Each task includes **stimulus design files** and **execution scripts** (Vision Egg format) to reproduce acquisition conditions.

---

## Important Notes for Multiband Data Users

- The **short TR** in multiband fMRI increases temporal resolution but changes **temporal autocorrelation** properties, which must be corrected during analysis.  
- **Spatial smoothness** can vary non-uniformly; standard Gaussian Random Field–based cluster corrections may be unsuitable.  
- **Slice timing correction** requires custom timing information due to simultaneous multi-slice excitation.  

Researchers should consult preprocessing recommendations from **Christian Beckmann** and **Steve Smith (HCP collaboration)** when analyzing these data.

---

## Phenotyping and Data Infrastructure

The enhanced NKI-RS includes extensive behavioral, cognitive, and clinical phenotyping, coordinated through the **COllaborative Informatics and Neuroimaging Suite (COINS)** platform. This system integrates all phenotypic and imaging data into a unified, queryable database.  
To ensure representative sampling, the project employs **community-ascertained recruitment** from Rockland County, NY, using demographic stratification to mirror U.S. census distributions.

---

## Downloads

Data are distributed via the **Neuroimaging Tools and Resources Clearinghouse (NITRC)**.

| Data Type | Description | Access |
|------------|--------------|--------|
| Imaging Data | Multiband R-fMRI, DTI, and task-based scans | [NITRC Download Page](https://www.nitrc.org/frs/?group_id=284) *(login required)* |
| Phenotypic Data | Demographic, psychiatric, and cognitive measures | Included in dataset package |

---

## Usage Agreement

This dataset is made available under the **Creative Commons Attribution–NonCommercial License (CC BY-NC)**.  
Users may share and adapt the material for non-commercial research with proper attribution.

**Disclaimer:**  
All scans are provided as-is. It is the user’s responsibility to perform appropriate quality control and determine inclusion for analysis.

---

## Funding and Acknowledgments

**Primary Funding:**  
- NIMH BRAINS R01MH094639-01 (PI Milham)  
- New York State Office of Mental Health and Research Foundation for Mental Hygiene  
- Child Mind Institute (1FDN2012-1)  
- Center for the Developing Brain, Child Mind Institute  
- NIMH R01MH081218, R01MH083246, R21MH084126  
- NKI Center for Advanced Brain Imaging (CABI)  
- Brain Research Foundation, Chicago  
- Stavros Niarchos Foundation  

**Core Team Leadership:**  
Michael Milham, Bennett Leventhal, F. Xavier Castellanos, Kate Nooner, Russ Tobe, Stan Colcombe  

**Technical & Imaging Support:**  
Cathy Hu, Raj Sangoi, Steve Zavitz, Cameron Craddock, Qingyang Li, Brian Cheung, Ranjit Khanuja, David Lewis, Chao-Gan Yan  

**Collaborations:**  
Special thanks to **CMRR, University of Minnesota** (Kamil Ugurbil, Eddie Auerbach, Junquian Gordon Xu, Steen Moeller) for providing multiband EPI sequences and reconstruction algorithms.  

---

## Citation

> Milham M., Colcombe S., Castellanos F.X., et al.  
> *Enhanced Nathan Kline Institute–Rockland Sample (NKI-RS) – Multiband Imaging Test–Retest Pilot Dataset.*  
> Nathan Kline Institute for Psychiatric Research, Orangeburg, NY, USA.  
> DOI: [10.15387/fcp_indi.corr.nki1](http://dx.doi.org/10.15387/fcp_indi.corr.nki1)

---

## Source

- Dataset page:  
  [http://fcon_1000.projects.nitrc.org/indi/enhanced/nki_rs.html](http://fcon_1000.projects.nitrc.org/indi/enhanced/nki_rs.html)  
- INDI / 1000 Functional Connectomes Project:  
  [https://www.nitrc.org/projects/fcon_1000/](https://www.nitrc.org/projects/fcon_1000/)

---

© Nathan Kline Institute for Psychiatric Research.  
Prepared for redistribution under **data-indi/nki-rs** by the **Pittsburgh Fiber Data Hub**.

## Release Link
https://github.com/data-indi/pro/releases/tag/nki-pilot
