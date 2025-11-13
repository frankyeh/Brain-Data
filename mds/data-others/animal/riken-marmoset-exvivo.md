# **Brain/MINDS Marmoset Brain MRI Dataset eNA91 (Ex Vivo)**
The **Brain/MINDS Marmoset MRI NA216 and eNA91 Datasets** represent the **largest publicly available marmoset brain MRI resource** to date, comprising data from **483 individuals**. These datasets offer a comprehensive range of **in vivo and ex vivo MRI data** across various imaging modalities, covering a wide age span of marmoset subjects.

### **License**

This dataset is shared under the **Creative Commons Attribution 4.0 International License (CC BY 4.0)**.
https://dataportal.brainminds.jp/marmoset-mri-na216

### **Dataset Composition**

#### **In Vivo Data (NA216)**

* **Subjects:** 455 individuals
* **Age Range:** 0.6 to 12.7 years (Mean: 3.86 ± 2.63 years)
* **Standard Brain Data:** 216 individuals (Mean age: 4.46 ± 2.62 years)

**Available Modalities:**

* T1-weighted Imaging (T1WI)
* T2-weighted Imaging (T2WI)
* T1WI/T2WI ratio maps
* Diffusion Tensor Imaging (DTI) metrics:

  * Fractional Anisotropy (FA)
  * Corrected FA (FAc)
  * Mean Diffusivity (MD)
  * Radial Diffusivity (RD)
  * Axial Diffusivity (AD)
* Diffusion Weighted Imaging (DWI)
* Resting-State fMRI (rs-fMRI) in **awake and anesthetized states**
* Structural and functional connectome matrices (CSV format)
* Standardized label data (NIfTI .nii.gz files)

#### **Ex Vivo Data (eNA91)**

* **Subjects:** 91 individuals (Mean age: 5.27 ± 2.39 years)

**Available Modalities:**

* Standard Brain Images (NIfTI .nii.gz)
* T2WI
* DTI Metrics: FA, FAc, MD, RD, AD
* DWI
* Standardized label data
* Structural connectome matrices (individual and population average, CSV format)

---

### **Imaging Methods**

For detailed information on imaging protocols, visit the [Imaging Methods Documentation](https://dataplatform.brainminds.jp/).

---

### **Usage Notes**

* Region names for structural and functional connectome matrices can be found [here](https://dataplatform.brainminds.jp/).
* Original data have been preprocessed and optimized for online previews, including:

  * Standardized resolution between in vivo and ex vivo datasets
  * Bit-depth reduction to 8-bits for faster display
  * Contrast enhancements for improved visualization

**Download Tips:**

* On some browsers (e.g., Safari), CSV files may open directly in a new tab. To download, either:

  * Press **\[Command] + S** on the newly opened tab, or
  * **Ctrl + Click** on the download link and choose "Download linked file."

**[Go to Data Download & Preview](https://dataplatform.brainminds.jp/)**

---

### **Citation**

> Hata J., Nakae K., Yoshimaru D., Okano H. *Brain/MINDS Marmoset Brain MRI Dataset NA216 and eNA91 (DataID: 4624).*
> DOI: [https://doi.org/10.24475/bminds.mri.thj.4624](https://doi.org/10.24475/bminds.mri.thj.4624)

## Release Link
https://github.com/data-others/animal/releases/tag/riken-marmoset-exvivo
