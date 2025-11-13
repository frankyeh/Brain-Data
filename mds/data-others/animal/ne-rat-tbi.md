
This dataset provides **diffusion tensor MRI (DTI)** and supporting materials for a **fluid‑percussion traumatic brain injury (TBI) rat model** comparing **rostral vs. caudal** cortical concussions. Using a **3D segmented and annotated rat brain atlas** (~150 regions), the study quantifies **indices of anisotropy (IA)** across >20,000 voxels to detect **gray‑matter microarchitectural disturbances** in subcortical nuclei.

Findings highlight convergent injury patterns in the **central nucleus of the amygdala**, **laterodorsal thalamus**, and **hippocampal complex**, with immunohistochemistry confirming **neuroinflammation** in these sites.

---

## License  
Public domain (Dryad)

---

## Citation  
> Kulkarni, P., Kenkel, W., Finklestine, S. P., Barchet, T. M., Ren, J. M., Davenport, M., Shenton, M. E., Kikinis, Z., Nedelman, M., & Ferris, C. F. (2015).  
> *Use of anisotropy, 3D segmented atlas, and computational analysis to identify gray matter subcortical lesions common to concussive injury from different sites on the cortex* [Data set]. Dryad.  
> [https://doi.org/10.5061/dryad.58c73](https://doi.org/10.5061/dryad.58c73)

> Primary article: PLOS ONE — https://doi.org/10.1371/journal.pone.0125748

---

## Source  
> https://doi.org/10.5061/dryad.58c73  
> Publisher: Dryad (Published Sep 09, 2015)  
> Affiliations: Northeastern University; Brigham and Women’s Hospital

---

## Dataset Information

| Category | Details |
|---|---|
| **Species / Strain** | Rat (*Rattus norvegicus*, likely Sprague Dawley as per keywords) |
| **Model** | Fluid percussion injury to **right rostral** or **right caudal** cortex |
| **Imaging** | Diffusion tensor MRI; **Index of Anisotropy (IA)** computed across >20,000 voxels |
| **Atlas** | 3D segmented & annotated rat brain atlas (~150 regions) |
| **Key Subcortical Findings** | Central nucleus of the amygdala, laterodorsal thalamus, hippocampal complex |
| **Histology** | Immunohistochemistry indicating **neuroinflammation** in affected nuclei |
| **Files** | `Caudal_TBI.tar.gz`, `Rostral_TBI.tar.gz`, IA comparison spreadsheet, and README files |
| **Total Size** | ~569 MB |

---

## Experimental Overview

- **Question:** Do concussions at different cortical sites produce common **subcortical** lesions?  
- **Approach:** Compute **IA** per voxel, register to an atlas, and compare **left vs. right** hemispheres to identify disturbed gray‑matter nuclei.  
- **Result:** Rostral and caudal injuries yield **strikingly similar** subcortical impact patterns, particularly in emotion‑regulatory structures (e.g., **central amygdala**).

---

## Suggested Uses

- Benchmarking pipelines for **DTI‑derived anisotropy metrics** in gray matter.  
- Atlas‑based **voxel‑wise lesion mapping** in rodent TBI.  
- Cross‑modal validation with **immunohistochemistry** and behavioral assays.  
- Training/testing algorithms for **automated subcortical lesion detection**.

---

## Keywords

Traumatic Brain Injury • DTI • Index of Anisotropy • Rat • 3D Segmented Atlas • Amygdala • Thalamus • Hippocampus • Neuroinflammation • Concussion • Fluid Percussion
## Release Link
https://github.com/data-others/animal/releases/tag/ne-rat-tbi
