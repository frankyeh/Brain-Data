# **In Vivo Diffusion MRI of Optic Pathways in 18 Healthy Mice**
This dataset contains **manganese-enhanced T1-weighted** and **diffusion-weighted MRI** of the optic pathways in **18 healthy C57BL/6 female mice**.  
The study investigates **white matter organization and manganese transport** in the mouse visual system using in vivo high-field MRI.  
Raw Bruker files and a subset of NIfTI-converted images are included to support both reprocessing and immediate analysis.

---

## License  
Creative Commons Attribution 4.0 International (CC BY 4.0)

---

## Citation  
> Filipiak, P., Sajitha, T. A., Shepherd, T. M., Clarke, K., Goldman, H., Placantonakis, D. G., Zhang, J., Chan, K. C., Boada, F. E., & Baete, S. H. (2023).  
> *In vivo diffusion MRI of optic pathways in 18 healthy mice* [Data set]. Zenodo.  
> [https://doi.org/10.5281/zenodo.8120834](https://doi.org/10.5281/zenodo.8120834)

---

## Source  
> https://doi.org/10.5281/zenodo.8120834  
> Institution: NYU Langone Health, Center for Advanced Imaging Innovation and Research (CAI2R)  
> Contact: [steven.baete@nyulangone.org](mailto:steven.baete@nyulangone.org)  
> Funded by: NIH grants R01 EB028774, R01 EB029306, R01 NS082436, P41 EB017183, and 1S10OD018337-01.

---

## Dataset Information

| Category | Details |
|-----------|----------|
| **Species** | Mouse (*Mus musculus*, C57BL/6 females) |
| **Sample Size** | n = 18 |
| **Age** | 7–8 weeks at imaging |
| **Scanner** | 7 T Bruker BioSpec (wide-bore) |
| **Coil** | 4-channel phased-array cryogenically cooled receive-only coil |
| **Anesthesia** | Isoflurane (3% induction, 1.0–1.5% maintenance) |
| **Imaging Sequences** | T1-weighted FLASH and multi-shell DWI |
| **DWI Parameters** | 200 µm isotropic, TE/TR = 27.6/2781 ms, 60 directions, b = {250, 1000, 2250, 4000} s/mm² |
| **T1-weighted Parameters** | FLASH, 100 µm isotropic, TE/TR = 4.5/30 ms |
| **Acquisition Time** | ~37 min (effective 60–70 min with motion-triggering) |
| **Data Format** | Bruker raw data and converted NIfTI files |
| **Total Dataset Size** | ~26 GB |

---

## Experimental Protocol  

Following baseline imaging, each mouse received **intravitreally administered manganese chloride (MnCl₂)** to enhance the T1-weighted signal along the visual pathways.  
- Injection volume: 1.0 µL (Mice 1–2), reduced to 0.5 µL (Mice 3–18) of 0.1 M MnCl₂  
- Injection side: Left eye (*n* = 8) or right eye (*n* = 10)  
- Follow-up scan: 21 ± 4 hours post-injection using the same FLASH T1-weighted sequence  

To minimize motion artifacts, mice were secured using a **bite bar and ear bars** and monitored via a **breathing pressure pad** coupled to a **TTL-triggered acquisition** system.

---

## Image Processing  

The DWI preprocessing pipeline employed **MRtrix3** and **ANTs** tools:  
- **Denoising:** `dwidenoise` (MP-PCA)  
- **Gibbs artifact removal:** `mrdegibbs`  
- **Bias field correction:** `dwibiascorrect ants`  
- **Resampling:** Interpolation to 100 µm isotropic resolution (matching anatomical scans)  
- **Registration:** `antsRegistrationSyN.sh` (rigid-body transform aligning follow-up MEMRI to b=0 images)

---

## Acknowledgments  

This work was supported by the **NIH Center for Advanced Imaging Innovation and Research (CAI2R)**, a **NIBIB Biomedical Technology Resource Center** (P41 EB017183).  
Special thanks to **Orin Mishkit, Zakia Ben Youss Gironda, Orlando Aristizabal,** and **Youssef Wadghiri** at the NYU Langone Health Preclinical Imaging Laboratory for technical assistance.

---

## Keywords  

Mouse MRI • Diffusion MRI • MEMRI • Optic Pathways • Visual System • MRtrix3 • ANTs • Preclinical Imaging • Bruker BioSpec • Multi-shell DWI • 7 Tesla MRI

## Release Link
https://github.com/data-others/animal/releases/tag/nyu-mouse
