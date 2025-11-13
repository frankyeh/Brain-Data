# **Validation of Diffusion Tensor Imaging Measures of Nigrostriatal Neurons in Macaques**
This dataset provides **in vivo diffusion MRI (DTI)**, together with companion **PET**, **behavioral**, and **post‑mortem histology** data from **16 non‑human primates (macaques)** subjected to **unilateral MPTP lesions** of the nigrostriatal pathway. It supports validation of diffusion‑based markers of **dopaminergic neuron integrity** against gold‑standard histological and neurochemical measures.

---

## License  
Public domain (Dryad)

---

## Citation  
> Shimony, J. S., Rutlin, J., Karimi, M., Tian, L., Snyder, A. Z., Loftin, S. K., Norris, S. A., & Perlmutter, J. S. (2019).  
> *Validation of diffusion tensor imaging measures of nigrostriatal neurons in macaques* [Data set]. Dryad.  
> [https://doi.org/10.5061/dryad.2f8j75d](https://doi.org/10.5061/dryad.2f8j75d)

> Primary article: PLOS ONE — https://doi.org/10.1371/journal.pone.0202201

---

## Source  
> https://doi.org/10.5061/dryad.2f8j75d  
> Publisher: Dryad (Published Aug 14, 2019)  
> Affiliation: University of Washington School of Medicine

---

## Dataset Information

| Category | Details |
|---|---|
| **Species** | Rhesus macaque / NHP (macaques) |
| **Subjects** | 16 animals |
| **Model** | Unilateral carotid artery infusion of **MPTP** (dopaminergic neurotoxin) |
| **Modalities** | Diffusion MRI (DTI), PET (three presynaptic ligands), video-based motor ratings, histology (TH) & neurochemistry (striatal dopamine) |
| **Outcome Measures** | DTI metrics of the nigrostriatal tract, PET uptake, striatal TH‑positive fiber density, nigral TH‑positive cell counts, striatal dopamine concentration |
| **Key Finding (from abstract)** | DTI metrics correlate with MPTP dose, **nigral TH cell counts**, and **striatal TH fiber density**; PET/terminal field measures show floor effects after >50% nigral loss where DTI continues to correlate |
| **Data Format** | DICOM archives (`*.tar`) plus study notes (`MonkeyDataSharing.txt`) |
| **Total Size** | ~22.6 GB |

---

## Experimental Overview

- **Design:** Each animal received **unilateral** MPTP to induce varying degrees of nigrostriatal injury.  
- **Imaging:** Pre/post **DTI** and **PET** with three presynaptic radioligands; blinded motor ratings.  
- **Endpoints:** Post‑mortem quantification of **striatal dopamine**, **TH‑positive striatal fibers**, and **TH‑positive nigral cell bodies**.  
- **Analysis:** Diffusion measures along the **nigrostriatal tract** compared to PET and histology across injury severities.

---

## Suggested Uses

- Validation of **tract‑specific diffusion biomarkers** for dopaminergic neurodegeneration.  
- Method development for **nigrostriatal tractography** and **ROI quantification** in NHPs.  
- Comparative evaluation of **DTI vs PET** sensitivity across lesion severity.  
- Benchmarking pipelines for **DICOM→NIfTI** conversion and diffusion processing in NHP datasets.

---

## Notes

- Dryad distribution provides **raw DICOM** per subject; users should convert to NIfTI (e.g., **dcm2niix**) and perform species‑appropriate preprocessing.  
- Tract definitions (midbrain↔striatum) and ROI placement should follow the primary article’s methods to reproduce correlations.

---

## Keywords

Diffusion MRI • DTI • Nigrostriatal • MPTP • Macaque • Dopamine • TH immunostaining • PET • Parkinson’s disease • Non‑human primate • Validation

## Release Link
https://github.com/data-others/animal/releases/tag/uw-macaque
