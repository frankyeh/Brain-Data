# **SIMON Dataset – Single Individual Volunteer for Multiple Observations across Networks**
![](https://fcon_1000.projects.nitrc.org/indi/pro/_static/logo_simon.png)

The **SIMON Dataset** is a unique longitudinal neuroimaging dataset from a **single healthy ambidextrous male**, aged **29 to 46 years**, who participated in **73 imaging sessions** across multiple sites and scanner models. This dataset serves as a valuable resource for studying cross-site and cross-protocol variability in neuroimaging data and includes a wide variety of imaging modalities.

Data were partially acquired through the **Canadian Dementia Imaging Protocol (CDIP)**, and new data will continue to be added as the study progresses.

---

### **Available Data**

Each imaging session includes at least a **T1-weighted anatomical scan**. Additional modalities vary across sessions and may include:

* T1-, T2-, and PD-weighted images
* T2\*-weighted images
* Diffusion-weighted imaging (DTI)
* Resting-state fMRI
* Susceptibility imaging
* Arterial spin labeling (ASL)

**Phenotypic Data:**

* Demographic information (age, session number, session date)
* Available in `SIMON_pheno.csv`

---

### **Data Access**

Data are hosted on an **Amazon Web Services (AWS) S3 bucket** and can be accessed using HTTP-based tools:

* [Access SIMON Raw Data](https://fcp-indi.s3.amazonaws.com/data/Projects/INDI/SIMON/rawdata)
* [Access SIMON Preprocessed Functional MRI Data](https://fcp-indi.s3.amazonaws.com/data/Projects/INDI/SIMON/derivatives)

**Instructions for Accessing Data via Cyberduck:**

1. Open Cyberduck and select **Open Connection**.
2. Set the application protocol to **S3 (Amazon Simple Storage Service)**.
3. Server: `s3.amazonaws.com`
4. Check **Anonymous Login**.
5. Expand **More Options** and set the Path to either:

   * `fcp-indi/data/Projects/INDI/SIMON/rawdata`
   * `fcp-indi/data/Projects/INDI/SIMON/derivatives`
6. Click **Connect**.

> *Note: Wildcards cannot be used for batch downloads. Use tools like `wget` or `curl` for direct downloads using exact file names.*

---

### **Personnel**

**Principal Investigator:**

* Simon Duchesne, Ph.D., CERVO Brain Research Centre, Quebec, Canada

**Senior Personnel and Collaborators (Alphabetical):**

* AmanPreet Badhwar, Ph.D., CRIUGM, Quebec, Canada
* Desiree Lussier-Levesque, Ph.D., CRIUGM, Quebec, Canada

*For inquiries, please contact: [info@medics.ulaval.ca](mailto:info@medics.ulaval.ca)*

---

### **Data Sharing License**

* **Attribution-ShareAlike International (CC BY-SA)**

---

### **Funding Acknowledgment**

Please cite the following organizations and publications in any work utilizing this data:

* Duchesne S, Chouinard I, Potvin O et al. *The Canadian Dementia Imaging Protocol: Harmonizing National Cohorts.* J Magn Reson Imaging. 2019; 49:456-465.

The SIMON dataset has been made possible through contributions from the following organizations:

* **CIMA-Q** ([www.cima-q.ca](http://www.cima-q.ca))
* **Canadian Consortium on Neurodegeneration in Aging (CCNA)** ([www.ccna-ccnv.ca](http://www.ccna-ccnv.ca))
* **Ontario Neurodegenerative Disease Research Initiative (ONDRI)** (ondri.ca)
* Alzheimer’s Society of Canada (#13-32)
* Canadian Institutes for Health Research (#117121)
* Fonds de recherche du Québec – Santé / Pfizer-FRQS Innovation Fund (#25262, #27239)
* Ontario Brain Institute

Additional support has been provided by the **Cuban Neuroscience Center** and the **University of Electronic Science and Technology of China** under the Tri-national Axis on Normal and Pathological Aging program.

---

### **Publications Using This Dataset**

1. Duchesne S, Dieumegarde L, Chouinard I, Farokhian F, Potvin O (Submitted). *Multi-contrast magnetic resonance imaging series of a single human volunteer over 15+ years.*
2. Duchesne S, Chouinard I, Potvin O et al. *The Canadian Dementia Imaging Protocol: Harmonizing National Cohorts.* J Magn Reson Imaging. 2019; 49:456-465.

## Release Link
https://github.com/data-indi/retro/releases/tag/simon
