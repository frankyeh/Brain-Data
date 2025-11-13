
This dataset contains **structural and diffusion MRI data** together with **derived FA, TBSS, and VBM results** for patients diagnosed with **Alzheimer’s Disease (AD)**, **Bipolar Disorder (BD)**, and **healthy controls (HC)**.  
It includes corresponding **clinical and biomarker information** organized in structured `.csv` files, supporting both **neuroimaging** and **clinical correlation** studies.

The dataset has been used in multiple peer-reviewed publications investigating **white matter integrity**, **biomarker correlation**, and **multivariate diagnostic modeling** of neurodegenerative and psychiatric disorders.

---

## License  
Creative Commons Attribution 4.0 International (CC BY 4.0)

---

## Citation  
> Besga, A., Graña, M., & Chyzhyk, D. (2020).  
> *Alzheimer’s Disease versus Bipolar Disorder versus Healthy Control MRI Data and Processed Results* [Data set]. Zenodo.  
> [https://doi.org/10.5281/zenodo.3935636](https://doi.org/10.5281/zenodo.3935636)

---

## Source  
> https://doi.org/10.5281/zenodo.3935636  
> Contact: [ariadna.besga@ehu.eus](mailto:ariadna.besga@ehu.eus)  
> Institutions: University of the Basque Country (UPV/EHU), University of Navarra, University of the Basque Country  
> Funding: European Commission — *CybSPEED: Cyber-Physical Systems for PEdagogical Rehabilitation in Special Education* (Grant No. 777720)

---

## Dataset Information

| Category | Details |
|-----------|----------|
| **Subjects** | Patients diagnosed with Alzheimer’s Disease (EA), Bipolar Disorder (TB), and healthy controls (CRL) |
| **Study Type** | Structural and diffusion MRI with derived FA, TBSS, and VBM analyses |
| **File Format** | NIfTI (.nii/.nii.gz) for imaging, CSV for clinical data |
| **Tools Used** | FSL (DTI, TBSS), SPM (VBM), MATLAB, Python, R |
| **Diagnostic Codes** | `crl` = control, `tb` = bipolar disorder, `ea` = Alzheimer’s disease |
| **Anonymization** | All subjects identified by numerical random keys |
| **Registration** | Nonlinear alignment to MNI space using FSL |
| **Publication Use** | Multiple neuroscience and diagnostic modeling studies |

---

## Clinical Data

The `Clinical_data` folder contains `.csv` files readable in Python, R, MATLAB, or any spreadsheet software.  
Each file corresponds to a specific biomarker.  

Key files include:
- `clinical_data_id_age_gender.csv`: anonymized ID, diagnostic key, age, and gender.  
- `clinical_data_corrected.csv`: deprecated, can be ignored.  

Diagnostic key:  
- `crl` = Healthy control  
- `tb` = Bipolar disorder  
- `ea` = Alzheimer’s disease  

---

## Publications Using This Dataset

1. **Graña et al. (2011)** — *Computer Aided Diagnosis system for Alzheimer’s Disease using DTI features*, *Neuroscience Letters*, 502(3):225–229.  
2. **Besga et al. (2012)** — *Discovering Alzheimer’s disease and bipolar disorder white matter effects using DTI*, *Neuroscience Letters*, 520(1):71–76.  
3. **Termenon et al. (2013)** — *Lattice ICA feature selection on DWI for Alzheimer’s classification*, *Neurocomputing*, 114:132–141.  
4. **Besga et al. (2015)** — *Discrimination between AD and late-onset BD using multivariate analysis*, *Frontiers in Aging Neuroscience*, 7:231.  
5. **Besga-Basterra et al. (2016)** — *Eigenanatomy on FA imaging differentiates AD and BD*, *Current Alzheimer Research*, 13(5):557–565.  
6. **Besga et al. (2017)** — *White matter tract integrity and inflammation in AD vs BD*, *Frontiers in Aging Neuroscience*, 9:179.  

---

## Purpose

This dataset supports research in **neurodegenerative and affective disorder differentiation**, enabling:
- Quantitative analysis of **white matter microstructure** (FA, TBSS).  
- Morphometric evaluation via **SPM-based VBM**.  
- Correlation between **MRI-derived features and clinical biomarkers**.  
- Machine learning model training for **computer-aided diagnosis** (CAD) of AD vs BD.  

---

## Keywords

MRI • Diffusion MRI • FA • TBSS • VBM • Alzheimer’s Disease • Bipolar Disorder • Healthy Control • FSL • SPM • Neurodegeneration • White Matter Integrity • Biomarkers
## Release Link
https://github.com/data-others/disease/releases/tag/ubc-ad_bd
