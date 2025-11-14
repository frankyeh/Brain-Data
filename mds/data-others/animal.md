# Animal dMRI Collections

The **Animal dMRI Collections** repository consolidates diffusion MRI (dMRI), tractography-ready derivatives, and curated documentation from a diverse set of **preclinical and non-human primate imaging studies**.
This collection brings together datasets from mice, rats, marmosets, macaques, horses, and other primate species—spanning **in vivo**, **ex vivo**, and **post-mortem** imaging.

The goal of this repository is to provide:

* **Unified access** to high-quality, openly available animal diffusion MRI datasets
* **Standardized derivative files** (`*.gqi.fz`, `*.qsdr.fz`, `*.sz`, `dti.dz`) to accelerate connectomics workflows
* **Concise summaries** of experimental design, acquisition, and metadata
* **Cross-species resources** for algorithm development, validation, and comparative neuroanatomy

All raw data remain hosted by the original publishers (Zenodo, Dryad, institutional portals). Users must follow the licensing and citation requirements specified by each dataset.

---

## Table of Contents

* [Overview](#overview)
* [Included Releases](#included-releases)

  * [NYU Mouse Optic Pathways dMRI](#nyu-mouse-optic-pathways-dmri)
  * [NKI Macaque Multimodal MRI](#nki-macaque-multimodal-mri)
  * [Rat TBI Anisotropy & Atlas Dataset](#rat-tbi-anisotropy--atlas-dataset)
  * [Turone Equine Social Brain Dataset (TESBD)](#turone-equine-social-brain-dataset-tesbd)
  * [DRCMR Axon Morphology (Monkey XNH + dMRI)](#drcmr-axon-morphology-monkey-xnh--dmri)
  * [UW Macaque Nigrostriatal DTI Validation](#uw-macaque-nigrostriatal-dti-validation)
  * [Utrecht Rat Cortical Connectome (Post-Mortem)](#utrecht-rat-cortical-connectome-post-mortem)
  * [Weizmann Forepaw Stimulation fMRI+dMRI](#weizmann-forepaw-stimulation-fmridmri)
  * [Brain/MINDS Marmoset MRI (In Vivo & Ex Vivo)](#brainminds-marmoset-mri-in-vivo--ex-vivo)
  * [PRIME-DE Rhesus (Structural T1/T2)](#prime-de-rhesus-structural-t1t2)
  * [PRIME-DE Global Collections](#prime-de-global-collections)
  * [Pittsburgh Marmoset Connectivity Atlas Derivatives](#pittsburgh-marmoset-connectivity-atlas-derivatives)
  * [Oxford WIN Macaque (Post-Mortem)](#oxford-win-macaque-post-mortem)
  * [NIN Primate Brain Bank MRI](#nin-primate-brain-bank-mri)
* [How to Use](#how-to-use)
* [Licensing](#licensing)
* [Citation](#citation)
* [Disclaimer](#disclaimer)

---

## Overview

This repository serves as a **cross-species diffusion MRI hub**, useful for:

* **Algorithm validation** (tractography, microstructure modeling, kurtosis, QSDR, etc.)
* **Cross-species comparative neuroanatomy**
* **Structure–function modeling** across mammals
* **Ex vivo vs. in vivo contrast comparisons**
* **Deep-learning training** for segmentation, registration, and connectome prediction
* **Benchmarking pipelines** in small-animal and NHP MRI

Where feasible, we host:

* Participant/session tables (`participants.tsv`)
* Quality-control summaries (`qc.tsv`)
* Tractography-ready compressed derivatives

Each dataset retains its original metadata and licensing.

---

## Included Releases

### NYU Mouse – In Vivo Optic Pathways dMRI

**DOI:** [https://doi.org/10.5281/zenodo.8120834](https://doi.org/10.5281/zenodo.8120834)
**Species:** C57BL/6 mice (n=18)
**Modalities:** Multi-shell DWI, MEMRI T1w
**Highlights:** Manganese tracing of visual pathways; Bruker raw + NIfTI; 7T mouse MRI
**License:** CC BY 4.0

---

### NKI Macaque – Multimodal MRI

**DOI:** [https://doi.org/10.5281/zenodo.1303400](https://doi.org/10.5281/zenodo.1303400)
**Species:** Rhesus macaque (n=3)
**Modalities:** MION-fMRI, T1/T2, DWI
**Highlights:** Resting-state, somatosensory stimulation, movie-watching paradigms
**License:** CC BY 4.0

---

### Rat TBI – Anisotropy & 3D Segmented Atlas

**DOI:** [https://doi.org/10.5061/dryad.58c73](https://doi.org/10.5061/dryad.58c73)
**Species:** Rat (TBI model)
**Modalities:** DTI + voxel-wise Index of Anisotropy (IA)
**Highlights:** Rostral vs. caudal TBI comparison; atlas (~150 regions)
**License:** Public domain (Dryad)

---

### Turone Equine Social Brain Dataset (TESBD)

**DOI:** [https://doi.org/10.5281/zenodo.13969827](https://doi.org/10.5281/zenodo.13969827)
**Species:** Horses (n=23, Welsh foals)
**Modalities:** Structural MRI, fMRI, dMRI
**Highlights:** First large-scale equine social-brain MRI dataset; rich behavioral metadata
**License:** CC BY 4.0

---

### DRCMR Axon Morphology – Monkey XNH + dMRI

**Source:** [https://www.drcmr.dk/axon-morphology-dataset](https://www.drcmr.dk/axon-morphology-dataset)
**Species:** Vervet monkey
**Modalities:** Whole-brain dMRI + X-ray nanoholotomography (XNH)
**Highlights:** Ground-truth axon morphologies; ActiveAx validation dataset
**License:** see original dataset notes

---

### UW Macaque – Nigrostriatal DTI Validation

**DOI:** [https://doi.org/10.5061/dryad.2f8j75d](https://doi.org/10.5061/dryad.2f8j75d)
**Species:** Rhesus macaque (n=16; MPTP model)
**Modalities:** DTI, PET (3 ligands), histology
**Highlights:** Direct validation of DTI biomarkers against TH cell counts
**License:** Public domain (Dryad)

---

### Utrecht Rat – Post-Mortem Cortical Connectome dMRI

**DOI:** [https://doi.org/10.5281/zenodo.11119038](https://doi.org/10.5281/zenodo.11119038)
**Species:** Wistar rats (n=10)
**Modalities:** dMRI (150 µm), BSSFP, SPGR
**Highlights:** High-res connectome mapping; ultra-high-field ex vivo imaging
**License:** CC BY 4.0

---

### Weizmann Forepaw Stimulation – BOLD + Diffusion Time-Dependence

**DOI:** [https://doi.org/10.5281/zenodo.14793797](https://doi.org/10.5281/zenodo.14793797)
**Species:** Female Wistar rats (n=10)
**Modalities:** BOLD fMRI, fast kurtosis dMRI
**Highlights:** Activity-induced MD/MK modulations; 14.1 Tesla
**License:** CC BY 4.0

---

### Brain/MINDS Marmoset – NA216 / eNA91

**DOI:** [https://doi.org/10.24475/bminds.mri.thj.4624](https://doi.org/10.24475/bminds.mri.thj.4624)
**Species:** Marmoset (in vivo 455; ex vivo 91)
**Modalities:** T1/T2, DWI, DTI metrics, rsfMRI
**Highlights:** Largest public marmoset MRI resource; standardized connectomes
**License:** CC BY 4.0

---

### PRIME-DE Rhesus – T1/T2 Collection

**Source:** [https://fcon_1000.projects.nitrc.org/indi/indiPRIME.html](https://fcon_1000.projects.nitrc.org/indi/indiPRIME.html)
**Species:** Rhesus macaque
**Modalities:** Structural MRI
**License:** CC BY-NC-SA
**Highlights:** T1/T2 structural subsets from the PRIME-DE consortium

---

### PRIME-DE Global Collections

**Species:** Multiple macaque sites
**Modalities:** Structural, diffusion, rsfMRI
**Purpose:** Global NHP neuroimaging consortium supporting cross-site studies
**License:** CC BY-NC-SA

---

### Pittsburgh Marmoset Connectivity Atlas Derivatives

**Source:** Marmoset Brain Connectivity Atlas
**Species:** Callithrix jacchus
**Modalities:** Tracer-based connectivity, registered to template
**Highlights:** Cell-level projections, warp fields, per-case metadata
**License:** CC BY 4.0 for imagery; see repository LICENSE for derivatives

---

### Oxford WIN Macaque (Post-Mortem)

**Species:** Rhesus macaque (n=6)
**Modalities:** Post-mortem DWI (0.6 mm @ 7T)
**Highlights:** High-b-value ex vivo macaque dMRI
**License:** CC BY-NC-SA

---

### NIN Primate Brain Bank — Multi-Species MRI

**DOI:** [https://doi.org/10.5281/zenodo.5044936](https://doi.org/10.5281/zenodo.5044936)
**Species:** 7 primate species
**Modalities:** Structural + diffusion MRI; FreeSurfer surfaces and connectomes
**License:** CC BY 4.0
**Highlights:** Cross-species comparative connectomics resource

---

## How to Use

1. **Browse releases** for dataset-specific metadata and derivative files.
2. **Download raw data** from the original Zenodo/Dryad/NITRC portals.
3. Use derivatives such as:

   * `*.gqi.fz` — GQI reconstruction (DSI Studio)
   * `*.qsdr.fz` — QSDR (template-based)
   * `*.sz` — diffusion slices
   * `*.dti.dz` / `*.gqi.dz` — group-level averages
4. Apply your tractography or modeling pipeline directly to the derivative files, or regenerate them from raw data if preferred.

---

## Licensing

Each dataset retains the **license declared by its original authors**, including combinations of:

* **CC BY 4.0** (NYU Mouse, NKI Macaque, TESBD, Utrecht Rat, etc.)
* **Public Domain / Dryad** (Rat TBI, UW Macaque MPTP)
* **CC BY-NC-SA** (PRIME-DE, Oxford WIN Macaque)
* **Custom / Institutional licenses** for specialized datasets

Always review and comply with the dataset-specific license listed in each release.

---

## Citation

When using datasets:

1. Cite the **original dataset DOI and publication**.
2. Cite any **primary research article** linked to the dataset.
3. If using derivatives from this repository, add:

> “Derivative files and curation were provided by the Pittsburgh Fiber Data Hub (`data-others/animal`).”

---

## Disclaimer

* These datasets are **heterogeneous** in acquisition (field strength, coil, anesthesia, stimulus, postmortem preparation).
* Users are responsible for performing appropriate **QC**, **artifact correction**, **species-appropriate preprocessing**, and **interpretation**.
* Some datasets require **special handling** (e.g., Bruker raw, DICOM archives, multi-shell ex vivo data).
* This repository does not host raw data; only curated summaries and derivatives permitted by the original license.

---

**Repository:** `data-others/animal` — Cross-Species Diffusion MRI Collections curated by the Pittsburgh Fiber Data Hub.
