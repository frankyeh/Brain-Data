
This dataset provides **structural and diffusion MRI data** of **seven non-human primate species** from the *Primate Brain Bank* at the Netherlands Institute for Neuroscience (Amsterdam).  
It includes **raw data**, **surface reconstructions** generated using FreeSurfer, and **connectome reconstructions** generated with CATO. The dataset supports comparative neuroanatomy and connectomics research across primate species.

---

## License  
Creative Commons Attribution 4.0 International (CC BY 4.0)

---

## Citation  
> Ardesch, D. J., Bryant, K. L., Roumazeilles, L., Scholtens, L. H., Khrapitchev, A. A., Tendler, B. C., Wu, W., Miller, K. L., Sallet, J., van den Heuvel, M. P., & Mars, R. B. (2021).  
> *Primate Brain Bank MRI* (1.0.0) [Data set]. Zenodo.  
> [https://doi.org/10.5281/zenodo.5044936](https://doi.org/10.5281/zenodo.5044936)

---

## Source  
> https://doi.org/10.5281/zenodo.5044936  
> Contact: [d.j.ardesch@nin.knaw.nl](mailto:d.j.ardesch@nin.knaw.nl)  
> Institutions: Netherlands Institute for Neuroscience, University of Oxford, Radboud University, Wellcome Centre for Integrative Neuroimaging  
> Funding: Biotechnology and Biological Sciences Research Council (BBSRC, UK) [BB/N019814/1], Wellcome Trust [203139/Z/16/Z], Netherlands Organization for Scientific Research (NWO) [VIDI-452-16-015, ALW-179]

---

## Dataset Information

| Category | Details |
|-----------|----------|
| **Species** | 7 non-human primate species: night monkey (*Aotus lemurinus*), black-and-white colobus (*Colobus guereza*), Senegal galago (*Galago senegalensis*), woolly monkey (*Lagothrix lagothricha*), grey-cheeked mangabey (*Lophocebus albigena*), white-faced saki (*Pithecia pithecia*), tufted capuchin (*Cebus apella*) |
| **Study Type** | Postmortem structural and diffusion MRI with surface and connectome reconstruction |
| **Data Format** | NIfTI (.nii.gz) and CSV |
| **Processing Tools** | FreeSurfer 6.0, CATO v2.5 |
| **Analysis Outputs** | Cortical surfaces, sulcal anatomy, and tractography-based connectomes |
| **Anatomical Context** | Comparative connectomics and cross-species cortical morphology |
| **Associated Publication** | Bryant, K. L. et al. (2021). *Diffusion MRI data, sulcal anatomy, and tractography for eight species from the Primate Brain Bank.* *Brain Structure and Function*, DOI: [10.1007/s00429-021-02268-x](https://doi.org/10.1007/s00429-021-02268-x) |

---

## Demographics  
Demographic details (age, sex, and Primate Brain Bank sample codes) are provided in the accompanying `demographics.csv` file.

---

## Processing Overview

- **Structural MRI:**  
  Processed with *FreeSurfer 6.0* using a modified non-human primate pipeline  
  ([https://github.com/ardesch/nhp-freesurfer](https://github.com/ardesch/nhp-freesurfer)).

- **Diffusion MRI:**  
  Processed using *CATO v2.5*  
  ([https://github.com/dutchconnectomelab/CATO](https://github.com/dutchconnectomelab/CATO))  
  to reconstruct fiber tracts and connectomes.

- **Data Outputs:**  
  Include preprocessed DWI data, FreeSurfer-derived cortical surfaces, and species-specific connectomes.

---

## Purpose  

This dataset provides a cross-species framework for studying **evolutionary connectomics**, **comparative cortical anatomy**, and **inter-species variation in structural connectivity**.  
It enables quantitative analyses linking **diffusion tractography**, **sulcal morphology**, and **network topology** across multiple primate lineages.

---

## Keywords  

Primate • Diffusion MRI • Tractography • Connectome • FreeSurfer • CATO • Comparative Anatomy • Non-Human Primate • Evolutionary Neuroscience • Sulcal Morphology
## Release Link
https://github.com/data-others/animal/releases/tag/oxford-pbb
