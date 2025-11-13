# **Functional and Structural MRI Data Following Transcranial Static Magnetic Stimulation Over the Motor Cortex**
This dataset provides **multiecho resting-state fMRI**, **diffusion-weighted imaging (DWI)**, and **high-resolution structural T1-weighted MRI** data from **right-handed healthy participants**.  
Each subject participated in two experimental sessions involving **real** and **sham transcranial static-magnetic-field stimulation (tSMS)** over the **right motor cortex (hand area)**.  
The study employs a **double-blind randomized crossover design**, enabling direct comparison between stimulation conditions.

This resource facilitates investigation into **tSMS-induced changes** in **functional connectivity**, **microstructural organization**, and **motor network dynamics**, combining structural, diffusion, and multiecho functional MRI.

---

## License  
Creative Commons Attribution 4.0 International (CC BY 4.0)

---

## Citation  
> Caballero-Insaurriaga, J., Pineda-Pardo, J. Á., & Foffani, G. (2025).  
> *Functional and Structural Magnetic Resonance Imaging Data Following Transcranial Static Magnetic Stimulation Over the Motor Cortex* (1.0.1) [Data set]. Zenodo.  
> [https://doi.org/10.5281/zenodo.15224957](https://doi.org/10.5281/zenodo.15224957)

---

## Source  
> https://doi.org/10.5281/zenodo.15224957  
> Contact: [jaime.caballero@unican.es](mailto:jaime.caballero@unican.es)  
> Institutions: Universidad de Cantabria, Hospital Nacional de Parapléjicos, Universidad Autónoma de Madrid  
> Funding: Supported by institutional research programs in non-invasive brain stimulation (NIBS)  

---

## Dataset Information

| Category | Details |
|-----------|----------|
| **Subjects** | Right-handed healthy adults |
| **Design** | Randomized double-blind crossover (real vs sham tSMS) |
| **Target Site** | Right motor cortex (hand area) |
| **Modalities** | Multiecho resting-state fMRI, diffusion-weighted imaging (DWI), high-resolution T1-weighted MRI |
| **Conditions** | 30-minute real tSMS and sham tSMS sessions |
| **Sessions** | Two sessions per subject, separated by one week, same weekday and time |
| **Data Format** | NIfTI (.nii/.nii.gz) |
| **Correction Notice (v1.0.1)** | Fixed scaling of phase images (now in −π..π range) |

---

## Experimental Details

This dataset includes multiecho resting-state fMRI, Diffusion-Weighted Imaging, and high-resolution structural T1-weighted MRI data acquired from right-handed healthy participants, immediately following 30-minute **real** and **sham** tSMS over the right motor cortex (hand region).  
Each participant underwent **two separate sessions**, one with real and one with sham stimulation, performed on separate days but at the same time of day and weekday.  
The order of stimulation was **randomized and double-blind**, ensuring balanced and unbiased comparisons.

---

## Demographics and Experimental Information

Additional participant details, including demographics (e.g., exact age) and condition-specific experimental notes, are available **upon reasonable request** to the authors.

---

## Conversion to NIfTI

All data were converted from native DICOM to **NIfTI** format using **dcm2niix**.  
File naming corrections and supplemental JSON metadata fields were added using a **custom Python script** to ensure consistency and completeness.

---

## Defacing

High-resolution T1-weighted anatomical scans were **defaced using FSL’s `fsl_deface` command**.  
While this tool reliably removes identifiable facial features, it can slightly reduce the apparent size of the frontal pole (see [Bischoff-Grethe et al., *NeuroImage*, 2021, doi:10.1016/j.neuroimage.2021.117845]).  
To mitigate this, the defacing mask was **expanded** prior to defacing by combining (`binary union`) the default mask with a **dilated brain mask** (7×7×7 voxel kernel).  
The brain mask was extracted using **FreeSurfer’s `mri_synthstrip`**, and dilation and combination were performed using **`fslmaths`**, ensuring full brain coverage for all subjects.

---

## Scaling of Phase Images

Both **multiecho fMRI** and **DWI** were acquired using the **CMRR multiband-accelerated EPI pulse sequences** (no multiband factor applied due to coil constraints).  
Magnitude and phase reconstructions were exported for each dataset.  
Native phase images were scaled in the **−4096..4094** integer range (as discussed in [CMRR Issue #238](https://github.com/CMRR-C2P/MB/issues/238)) and verified by the authors.  
Using **FSL tools**, these were **losslessly rescaled to radians** (−π..π) by adjusting `scl_slope` and `scl_inter` fields in the NIfTI header without altering data type or stored voxel values.

Rescaling formula:  
\[
\text{phase (radians)} = \frac{x}{4096} \times \pi
\]

---

## Software Versions

| Component | Version / Build |
|------------|----------------|
| CMRR Multiband EPI | R016–R017 |
| dcm2niix | v1.0.20230411 (GCC 12.2.0, Linux x86-64) |
| Python | 3.8.17 |
| FSL | 6.0.6.4 |
| FreeSurfer | 7.3.2 |

---

## File Information

| File | Description | Size | Checksum |
|------|--------------|------|-----------|
| **tSMS_M1R_MRI.zip** | MRI data (multi-echo fMRI, DWI, and T1w) for both real and sham stimulation sessions | 35.2 GB | `md5:2d9f8b9c1ca647dac96619442cffa321` |

---

## Keywords

MRI • fMRI • Multi-Echo • Resting-State • Diffusion MRI • DWI • Motor Cortex • tSMS • Transcranial Static Magnetic Field • Non-Invasive Brain Stimulation • NIBS • CMRR • Phase Correction

## Release Link
https://github.com/data-others/brain2/releases/tag/cinac-tsms
