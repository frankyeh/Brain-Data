---
title: data-others/atlas
---

# Templates and Atlases (`data-others/atlas`)

Templates and atlases for human and animal brains distributed through the Fiber Data Hub, including the **Common Hierarchical Atlas (CHA)** cross-species gray-matter parcellation spanning rodents, nonhuman primates, and humans.

- **Related Hub documentation:** [HCP-1065 templates](/hcp_template.html) · [Tractography atlas & T2R connectome](/hcp_trk_atlas.html)
- **Quality control & download:** [QC results](/qc.html) · [Download guide](/download.html)
- **Secondary direct assets:** [GitHub Releases ↗](https://github.com/data-others/atlas/releases)

## Overview

The Common Hierarchical Atlas (CHA) provides a unified anatomical framework for cortical and subcortical gray-matter parcellation across multiple species using species-specific minimal deformation templates (MDTs) aligned to the AC-PC axis (except for the human ICBM152 reference).

- **Primary species:** Human, Rhesus macaque, Marmoset, and Mouse (with Rat coverage via MRI-based alignment from mouse).
- **File naming:** Species atlas volumes are distributed as `<species>_CHA.nii.gz`.

## Hierarchical Levels

- **Level 0 — Tissue Compartments:** Gray matter (GM), White matter (WM), Deep gray matter (DGM), Cerebellum (CBL), and Cerebrospinal fluid (CSF).
- **Level 1 — Macro-Regions:** Frontal (FRO), Parietal (PAR), Temporal (TEM), Occipital (OCC), Insular (INS), Cingulate (CIN), Olfactory (OLF), Basal ganglia (BG), and Thalamic / hypothalamic system (THL).
- **Level 2 — Subdivisions:** 26 Level-2 regions in primates and 21 Level-2 regions in rodents (with Parietal lobe and Caudoputamen undivided in rodents). Claustrum, substantia nigra, and subthalamic nuclei are excluded where cross-species MRI boundaries are not reliably separable.

## Species Reference Templates & Source Atlases

- **Human:** ICBM152 Nonlinear Asymmetrical 2009a template (cross-referenced with FreeSurferSeg and Brodmann areas)
- **Rhesus macaque:** MDT generated from PRIME-DE T1-weighted MRI (cross-referenced with CIVM and Inia19 / NeuroMaps)
- **Marmoset:** Brain/MINDS / MBM-derived reference with AC-centered coordinate adjustment (cross-referenced with Brain/MINDS, MBM, and Paxinos atlases)
- **Mouse:** High-resolution diffusion MRI MDT (cross-referenced with Allen Brain Atlas)
- **Rat:** MDT generated from ex vivo diffusion MRI aligned to the common framework
