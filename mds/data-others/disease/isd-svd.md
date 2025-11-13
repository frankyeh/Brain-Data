
This dataset provides **multi-site diffusion MRI data** from **10 patients** diagnosed with the genetically defined small vessel disease **CADASIL**, scanned on two different 3 T Siemens MRI scanners (**Magnetom Prisma** and **Magnetom Skyra**) within 24 hours.  
It enables evaluation of **inter-scanner reproducibility** of diffusion metrics in cerebral small vessel disease (SVD) and supports harmonization studies for **multi-center neuroimaging trials**.

The dataset was used in the publication:  
Konieczny & Dewenter et al., *Neurology*, 2020 — [https://doi.org/10.1212/WNL.0000000000011213](https://doi.org/10.1212/WNL.0000000000011213)

---

## License  
Creative Commons Attribution – NonCommercial 4.0 International (CC BY-NC 4.0)

---

## Citation  
> Dewenter, A., Gesierich, B., & Duering, M. (2020).  
> *3T diffusion MRI inter-site reproducibility dataset for cerebral small vessel disease* [Data set]. Zenodo.  
> [https://doi.org/10.5281/zenodo.16925507](https://doi.org/10.5281/zenodo.16925507)

---

## Source  
> https://doi.org/10.5281/zenodo.16925507  
> Contact: [marco.duering@med.uni-muenchen.de](mailto:marco.duering@med.uni-muenchen.de)  
> Institution: Institute for Stroke and Dementia Research (ISD), LMU Munich, Germany  
> Associated publication: *Neurology*, 96(5), e698–e708 (2020)  

---

## Dataset Information

| Category | Details |
|-----------|----------|
| **Subjects** | 10 patients with CADASIL (genetically confirmed or via skin biopsy) |
| **Age (median [IQR])** | 55.5 years (13.3) |
| **Sex** | 5 female (50 %) |
| **Hypertension / Hypercholesterolemia** | 3 / 5 patients |
| **WMH volume [% ICV] median (IQR)** | 7.67 (2.62) |
| **Lacune count median (IQR)** | 3 (7.75) |
| **Brain volume [% ICV] median (IQR)** | 75.7 (7.03) |
| **Scanner Types** | Siemens 3 T Magnetom Prisma and Skyra |
| **Scan Interval** | < 24 hours |
| **Protocol** | Matched b-values, gradient directions, and resolution between scanners |
| **BIDS-Compliance** | Data organized per subject and session (/sub-XX/ses-prisma, /ses-skyra) |
| **Preprocessing Tools** | dcm2niix, MRtrix (dwidenoise & mrdegibbs), FSL (TOPUP & EDDY) |
| **Anonymization** | Fully de-identified and restricted to diffusion MRI only |

---

## MRI Acquisition Protocol  

| Parameter | Magnetom Skyra | Magnetom Prisma |
|------------|----------------|----------------|
| Coil | 64-channel head/neck | 64-channel head/neck |
| TR (ms) | 3800 | 3200 |
| TE (ms) | 104.8 | 74 |
| Resolution (mm³) | 2×2×2 | 2×2×2 |
| b-values (s/mm²) | 1000 / 2000 | 1000 / 2000 |
| Directions (per b) | 30 / 60 | 30 / 60 |
| b = 0 images | 10 | 10 |
| Multi-band factor | 3 | 3 |
| Acceleration factor | 2 | 2 |

Both scanners were located in **separate hospital buildings** with **independent infrastructure**, establishing a true inter-site condition despite institutional proximity.

---

## Data Structure and Preprocessing  

The dataset follows the **BIDS** organization scheme:  

```
/sub-01
   /ses-prisma
       /dwi_raw
       /dwi_preprocessed
   /ses-skyra
       /dwi_raw
       /dwi_preprocessed
```

- **Raw data** converted from DICOM via *dcm2niix*  
- **Preprocessed data** includes denoising (MRtrix `dwidenoise`), Gibbs correction (`mrdegibbs`), and motion/eddy distortion correction (FSL `TOPUP`, `EDDY`).  

---

## Purpose  

This dataset serves as a benchmark for assessing **inter-scanner reproducibility** and **harmonization** of diffusion MRI measures across 3 T sites.  
It is particularly relevant for researchers working on:  
- **Cross-site calibration** of diffusion metrics in small vessel disease  
- **Methodological validation** of preprocessing and harmonization pipelines  
- **Clinical reproducibility** of DTI/DKI biomarkers in multicenter trials  

---

## Keywords  

Diffusion MRI • DTI • CADASIL • Small Vessel Disease • Inter-site Reproducibility • Siemens Prisma • Siemens Skyra • BIDS • FSL • MRtrix • Neurology 2020  
## Release Link
https://github.com/data-others/disease/releases/tag/isd-svd
