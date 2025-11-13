# License
Creative Commons Attribution 4.0 International (CC BY 4.0)

## Source  
> https://zenodo.org/records/15149088  
> Contact: [davide.dicenso@unich.it](mailto:davide.dicenso@unich.it)  
> Data from Healthy Controls (HC) group

---

## Overview

This dataset includes imaging data from the Healthy Control (HC) group of the project **“Structural and Functional Basis of Neuronal Plasticity.”**  
It was designed to investigate cerebral blood flow (CBF) and metabolic responses to motor learning using multimodal MRI techniques.

We developed an MRI protocol combining **Diffusion-Weighted Imaging (DWI)** and **pseudo-continuous arterial spin labeling (pCASL)** with pre-saturation, background suppression, and a **dual-excitation (DEXI)** readout.  
This protocol enables mapping of CBF and absolute **CMRO₂** during resting states and after motor task learning within the MRI scanner.

---

## Dataset Information

| Category | Details |
|-----------|----------|
| **Subjects** | 40 healthy controls |
| **Scanner** | Siemens Prisma 3T (Siemens Healthineers, Forchheim, Germany) |
| **Head Coil** | 32-channel receive-only |
| **Anatomical Scan** | T1-weighted MP2RAGE |
| **Functional / Perfusion Scans** | 3 DEXI pCASL acquisitions |
| **Diffusion Scans** | 2 DWI acquisitions |
| **Metabolic Scans** | TRUST and IR-EPI acquisitions for brain metabolic metrics |

---

## Task Description

Participants performed a **visuomotor matching task** inside the MRI scanner:

- A white circle expanded and contracted on a black screen.  
- Participants controlled a **green circle** using an MRI-compatible data glove (Fifth Dimension Technologies, Pretoria, South Africa) to match its size to the white circle.  
- The task included **15 blocks** (7 fixed-sequence, 8 random), each lasting **35.2 s**, followed by **26.4 s** of rest.  
- Stimuli were presented using **PsychoPy**.

---

## Additional Collected Data

Neuropsychological assessments, end-tidal **CO₂** and **O₂** traces, and task performance metrics were also recorded.  
These datasets are currently being converted and analyzed and are **not yet included** in this release.

---

## Known Missing or Partial Data

- **sub-001–010**: No SWI images (SWI introduced starting from sub-011)  
- **sub-011, sub-013**: Fewer DWI directions in second run due to scanner issue  
- **sub-020**: No SWI images  
- **sub-025**: Presence of an arachnoid cyst  
- **sub-027**: Did not complete protocol  
- **sub-030, sub-032, sub-033, sub-039**: Dropouts

## Release Link
https://github.com/data-others/brain2/releases/tag/vitality
