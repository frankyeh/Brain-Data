# **Diffusion Weighted MR Imaging of Post-Mortem Rat Brain to Allow Reconstruction of the Cortical Connectome**
This dataset provides **diffusion-weighted MRI (dMRI)** and **high-resolution 3D structural MRI** of **post-mortem rat brains**, enabling detailed reconstruction of the **cortical connectome**.  
It accompanies the publication by *Sinke et al. (2018)* and includes 10 perfusion-fixed Wistar rat brains scanned at ultra-high field (9.4 T).  
The dataset contains raw dMRI and balanced SSFP data, along with derived diffusion metrics and anatomical references for connectome analysis.

All experiments were approved by the **Animal Experiments Committee** of the University Medical Center Utrecht and Utrecht University, and conducted in compliance with the **European Communities Council Directive** on animal research.

---

## License  
Creative Commons Attribution 4.0 International (CC BY 4.0)

---

## Citation  
> Sinke, M. R. T., Otte, W. M., van der Toorn, A., Dijkhuizen, R., & Sarabdjitsingh, R. A. (2024).  
> *Diffusion weighted MR imaging of post-mortem rat brain to allow reconstruction of the cortical connectome* [Data set].  
> *Brain Structure and Function*, 223(5). Zenodo.  
> [https://doi.org/10.5281/zenodo.11119038](https://doi.org/10.5281/zenodo.11119038)

---

## Source  
> https://doi.org/10.5281/zenodo.11119038  
> Contact: [m.r.t.sinke@umcutrecht.nl](mailto:m.r.t.sinke@umcutrecht.nl)  
> Institution: University Medical Center Utrecht  
> Journal: *Brain Structure and Function*, 223(5), 2024  

---

## Dataset Information

| Category | Details |
|-----------|----------|
| **Species** | Rat (*Rattus norvegicus*, Wistar, male, 12–13 weeks old) |
| **Sample Size** | 10 post-mortem brains |
| **Preparation** | Perfusion-fixed via transcardial fixation; skulls intact |
| **Scanner** | Varian 9.4 T horizontal bore system |
| **Coil** | Custom solenoid coil (2.6 cm ID) |
| **Imaging Medium** | Non-magnetic oil (Fomblin, Solvay Solexis) |
| **Ethics Approval** | University Medical Center Utrecht (EU Directive compliant) |
| **Institutions** | UMC Utrecht, Utrecht University |

---

## Purpose

The dataset supports investigation of **rat cortical microstructure and connectivity** using **ex-vivo diffusion MRI**.  
It enables validation of diffusion tractography and modeling of cortical connectivity at high resolution, providing a reference for algorithm development, structural mapping, and interspecies comparison.

---

## MR Acquisition Details

- **Diffusion MRI**  
  - 3D diffusion-weighted spin-echo sequence  
  - Isotropic resolution: 150 μm  
  - TR/TE: 500/32.4 ms  
  - 60 diffusion-weighted directions (b = 1031–7756 s/mm²)  
  - 24 b₀ images  
  - Total: 325 images  

- **Balanced SSFP (BSSFP)**  
  - 4 × 3D acquisitions, isotropic 100 μm  
  - TR/TE: 15.4/7.7 ms, flip angle 40°  
  - Phase shifts: 0°, 90°, 180°, 270°  
  - Combined to reduce banding artifacts  

- **Spoiled Gradient Echo (SPGR)**  
  - Echo times: 5, 10, 15 ms  
  - TR: 20 ms, flip angle 40°  
  - 24 averages  

---

## File Information

| File | Description | Size | Checksum |
|------|--------------|------|-----------|
| **rawdata.zip** | NIfTI volumes for all 10 rats (RCR01–RCR10) including diffusion, BSSFP, and SPGR data | 12.9 GB | `md5:f39aa478e8a8d9990843257d2c451ef6` |
| **derivatives.zip** | DTIfit-derived diffusion maps (FA, MD, etc.) and masks | 621.9 MB | `md5:e45d3395f7affc3788a7824c31eedbe8` |
| **RCR_table.csv** | Acquisition metadata per animal | 830 B | `md5:d0428a879d003d1243789f03b9820059` |
| **Sinke_BrainStructureFunction2018.pdf** | Associated publication | 4.0 MB | `md5:938dac3d4452e5006f6628c3586ec41a` |
| **READ_ME.txt** | Original dataset description | 4.9 kB | `md5:49e5fc005bc47bc6b2ca6bc864ba66bc` |

---

## Keywords

MRI • Diffusion MRI • Rat Brain • Post-mortem • Cortical Connectome • High-field MRI • Ex-vivo Imaging • Tractography

## Release Link
https://github.com/data-others/animal/releases/tag/utrecht-rat
