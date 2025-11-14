# Brain MRI Collections (after 2020)

This repository hosts curated external **human brain diffusion MRI datasets** sourced from publicly available archives (e.g., Zenodo, Dryad, ScienceDB). The collections are provided as-is and are intended for **research, validation, benchmarking, and educational use** in neuroimaging and tractography tool development.

The datasets focus on **multi-shell dMRI**, **advanced microstructural imaging**, **test–retest studies**, and **high-resolution acquisitions** that are valuable for studying structural connectivity and modeling white matter microarchitecture.

All datasets retain their original **license**, **citation**, and **metadata** as required by the data owners.

---

## 📦 Included Releases

### ✅ Brain & Spinal Cord Multi-Shell Diffusion MRI

**11 subjects**, test–retest in 6
BIDS (v1.9.0) brain+cord imaging
📝 License: CC BY 4.0
🔗 DOI: [https://doi.org/10.5281/zenodo.15512428](https://doi.org/10.5281/zenodo.15512428)
Applications: brain–cord connectomics, SANDI/SMT/NODDI evaluation

---

### ✅ EDEN2020 Human Brain MRI (Milan, Italy)

**15 subjects**, multimodal MRI for neurosurgery research
📝 License: CC BY-NC-ND 4.0
🔗 DOI: [https://doi.org/10.5281/zenodo.3994749](https://doi.org/10.5281/zenodo.3994749)
Applications: HARDI tractography, angiography + diffusion integration

---

### ✅ Structural & Functional Basis of Neuronal Plasticity (HC Group)

**40 subjects**, combined **ASL + DWI** motor learning experiment
📝 License: CC BY 4.0
🔗 DOI: [https://zenodo.org/records/15149088](https://zenodo.org/records/15149088)
Applications: CBF/metabolism connectivity, learning-induced plasticity

---

### ✅ Ultra-High-Resolution Human dMRI @ 760 µm

**1 subject**, 9 × 2-h sessions
Connectom scanner (300 mT/m gradients)
📝 License: CC0-1.0
🔗 DOI: [https://doi.org/10.5061/dryad.rjdfn2z8g](https://doi.org/10.5061/dryad.rjdfn2z8g)
Applications: fine-scale tractography method development

---

### ✅ Test–Retest Cross-Scanner dMRI — B-Q Minded Study

Cross-platform harmonization dataset
📝 License: CC BY 4.0
🔗 DOI: [https://doi.org/10.5281/zenodo.6473268](https://doi.org/10.5281/zenodo.6473268)
Applications: reproducibility studies, inter-scanner harmonization

---

## 🔍 Purpose

This repository serves as a **central access point** for:

* Benchmark testing of **tractography and diffusion models**
* Evaluating **brain–spinal cord joint pipelines**
* Cross-scanner harmonization research
* Public test datasets for **DSI Studio** and other tools
* Training and education in connectomics

---

## 📂 Data Format

* Primarily **NIfTI** (.nii/.nii.gz)
* BIDS directory structure when provided
* Derivatives include segmentation, model maps, QC reports, etc.

Each release includes its original documentation and metadata.

---

## 📑 Citations

Users must cite the **original dataset authors** when publishing research.
Citation information is provided inside each release description.

---

## ⚖️ Licensing

Each dataset follows its original license terms:

* **CC BY 4.0**
* **CC BY-NC-ND 4.0**
* **CC0-1.0**
  Please review before usage.


