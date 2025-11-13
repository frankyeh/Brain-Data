# **Forepaw Electrical Stimulation: MD and MK Time-Dependence vs. BOLD-fMRI**
This dataset includes diffusion MRI and BOLD-fMRI data acquired from **female Wistar rats (N = 10)** subjected to **forepaw electrical stimulation** under ultra-high-field MRI.  
The experiment was conducted to investigate how neural activity modulates **mean diffusivity (MD)** and **mean kurtosis (MK)** over multiple diffusion times, and how these changes relate to **BOLD-fMRI activation**.

---

## License  
Creative Commons Attribution 4.0 International (CC BY 4.0)

---

## Citation  
> Hertanu, A. (2025). *Forepaw electrical stimulation: MD and MK time-dependence vs. BOLD-fMRI* [Data set].  
> *Imaging Neuroscience*.  
> Zenodo. [https://doi.org/10.5281/zenodo.14793797](https://doi.org/10.5281/zenodo.14793797)

> Related article: [https://doi.org/10.1162/imag_a_00445](https://doi.org/10.1162/imag_a_00445)

---

## Source  
> https://doi.org/10.5281/zenodo.14793797  
> Publisher: Zenodo (Version v2, February 2025)  
> Associated Journal: *Imaging Neuroscience* (2025)  
> Contact: [andreea.hertanu@weizmann.ac.il](mailto:andreea.hertanu@weizmann.ac.il)  
> Institution: Weizmann Institute of Science, Israel  
> Hardware: Bruker BioSpin 14.1 T MRI system with custom-built surface quadrature transceiver RF coil

---

## Dataset Information

| Category | Details |
|-----------|----------|
| **Species** | Wistar rat (*Rattus norvegicus*) |
| **Sex** | Female |
| **Sample Size** | N = 10 |
| **Stimulation Paradigm** | Electrical forepaw stimulation |
| **Scanner** | 14.1 T Bruker BioSpin MRI |
| **RF Coil** | Home-built surface quadrature transceiver coil |
| **Diffusion Times** | Five diffusion times (fast kurtosis protocol) |
| **BOLD-fMRI TR** | 1 second |
| **Stimulus Runs** | 5 functional runs (4 for rats 000002, 000003) |
| **Data Format** | NIfTI, organized in BIDS-like structure |
| **Total Size** | ~9.1 GB |

---

## Experimental Design

Each rat underwent repeated imaging sessions including diffusion-weighted imaging (DWI) and BOLD-fMRI under forepaw stimulation.  
Both modalities included **reversed EPI phase-encode direction acquisitions** for distortion correction.

### Diffusion-weighted Imaging (DWI)
- 14 images at rest, 14 during stimulation  
- Repeated until 84 total volumes (excluding initial b0)  
- Acquired using **fast kurtosis imaging** (Hansen et al., 2016)

### BOLD-fMRI
- 28 images at rest, 28 during stimulation  
- Repeated until 336 total volumes per run  
- Temporal resolution = 1 s

### Functional Runs
Each session consisted of five runs alternating **rest** and **stimulation** blocks.  
Rats 000002 and 000003 completed four runs due to motion or physiological constraints.

---

## Analysis Focus

The dataset supports multimodal analysis of:
- **Activity-driven microstructural changes** via MD and MK modulations  
- **Diffusion-time dependence** of kurtosis metrics under activation  
- **BOLD-dMRI correlations** in somatosensory cortex  

Region-of-interest analyses were conducted in the **left hemisphere** (contralateral to the right forepaw stimulation).  
Signals were labeled as *contralateral* or *ipsilateral* based on expected somatosensory activation patterns.

---

## Potential Applications

- Joint modeling of **BOLD and diffusion time-dependence**  
- Validation of **microstructural-functional coupling models**  
- Exploration of **neuronal vs. vascular origins** of diffusion changes  
- Preclinical pipeline testing for **multimodal rat fMRI**

---

## Keywords  

Rat fMRI • Diffusion Kurtosis • MD Time-Dependence • Functional MRI • Forepaw Stimulation • BOLD • Fast Kurtosis Imaging • 14.1 Tesla MRI • Bruker BioSpin • Weizmann Institute

## Release Link
https://github.com/data-others/animal/releases/tag/unil-forpaw
