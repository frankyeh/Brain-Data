### **Enhanced Nathan Kline Institute-Rockland Sample (NKI-RS)**

**Multiband Imaging Test-Retest Pilot Dataset**

---

### **Project Overview**

The **Enhanced NKI-RS** builds upon the initial NKI-RS effort to create a **large cross-sectional neuroimaging dataset** spanning **ages 6 to 85 years**. This initiative, funded by the **NIMH (PI: Michael Milham)**, aims to characterize **1,000 community-ascertained participants** using cutting-edge multiband imaging techniques, diffusion tensor imaging (DTI), genetics, and an expanded deep phenotyping protocol.

Designed as an **open-access community resource**, the dataset enables researchers to test existing hypotheses and generate new ones through data exploration. Imaging datasets are shared weekly through the Neuroimaging Tools and Resources Clearinghouse (NITRC), and genetic data will be made available via the NIMH Genetics Repository.

---

### **Key Features**

#### **Imaging Advancements**

* Use of state-of-the-art **Multiband Echo Planar Imaging (EPI)**, enabling rapid full-brain coverage.
* Multiband sequences developed at the **Center for Magnetic Resonance Research (CMRR), University of Minnesota**, under the Human Connectome Project.
* Two advanced resting-state fMRI sequences:

  * **TR = 645 ms**, 3 mm isotropic voxels, 10-minute scan (optimal temporal resolution)
  * **TR = 1400 ms**, 2 mm isotropic voxels, 10-minute scan (optimal spatial resolution)
* Standard EPI sequence:

  * **TR = 2500 ms**, 3 mm isotropic voxels, 5-minute scan
* **DTI Sequence:** 137 directions, 2 mm isotropic voxels

#### **Phenotyping Enhancements**

* Broad assessment of **psychiatric, cognitive, and behavioral variables** across the lifespan.
* Selection of measures informed by experts and aligned with initiatives such as:

  * Brain Genomics Superstruct Project
  * Human Connectome Project
  * Brain Behavior Laboratory at the University of Pennsylvania
* Expanded assessments administered over **two separate days** to minimize participant fatigue.

#### **Neuroinformatics Infrastructure**

* Adoption of the **COllaborative Informatics and Neuroimaging Suite (COINS)** for web-based phenotypic data management.
* Integrated search capabilities for both phenotypic and imaging data.

#### **Community Representation**

* Recruitment modeled after epidemiological studies to ensure **representative sampling across geographic, socioeconomic, ethnic, and racial demographics**.
* Sampling based on zip-code level representation from **Rockland County, NY**, reflective of U.S. population demographics.

---

### **Multiband Test-Retest Pilot Dataset**

Prior to the full launch of the Enhanced NKI-RS, a pilot dataset was collected to assess the **reliability of multiband R-fMRI and DTI scans**. This dataset includes participants from the initial NKI-RS, along with associated psychiatric assessments.

**In addition to R-fMRI and DTI, the following were included:**

* **Visual Checkerboard Stimulation fMRI** (for quality control metrics)
* **Breath Holding Task** (for vascular responsiveness evaluation)
* **Eye Movement Calibration Scans** (to assess motion artifacts in multiband sequences)

---

### **Available Imaging Data**

#### **Repeated Scans:**

* R-mfMRI (TR = 645 ms, 3 mm isotropic, 10 min)
* R-mfMRI (TR = 1400 ms, 2 mm isotropic, 10 min)
* R-fMRI (TR = 2500 ms, 3 mm isotropic, 5 min)
* DTI (137 directions, 2 mm isotropic)

#### **Single Acquisition Scans:**

* Visual Checkerboard Stimulation

  * TR = 645 ms (3 mm isotropic, 2.5 min)
  * TR = 1400 ms (2 mm isotropic, 2.5 min)
* Eye Movement Calibration

  * TR = 645 ms (3 mm isotropic, 2.5 min)
  * TR = 1400 ms (2 mm isotropic, 2.5 min)
* Breath Holding (TR = 1400 ms, 2 mm isotropic, 10 min)

**Stimulus Files and Execution Scripts:**

* Visual Checkerboard Stimulation
* Eye Movement Calibration
* Breath Holding
* Stimulus Execution Scripts (compatible with Vision Egg)

---

### **Important Considerations for Multiband Imaging Analysis**

* Short TRs increase temporal degrees of freedom but alter effective temporal autocorrelation; corrections must be applied in statistical analyses.
* Spatial smoothness may become non-stationary, affecting cluster-based inference methods.
* Slice timing correction requires custom handling due to simultaneous multi-slice acquisition.

---

### **Disclaimer**

All available data are shared **as-is**. Users are responsible for performing their own quality assessments prior to analysis.

---

### **Usage Agreement**

Data is shared under a **Creative Commons License: Attribution – Non-Commercial**.

## Release Link
https://github.com/data-indi/pro/releases/tag/nki-pilot
