# Disease dMRI Collections

Curated **disease-focused MRI datasets** (structural & diffusion) for research, benchmarking, and education.
Each release retains its **original license**, **citation**, and **metadata**. Please **cite the source** when using any dataset.

---

## Included Releases

### 1) Alzheimer’s vs Bipolar vs Healthy Controls (`ubc-ad_bd`)

Structural & diffusion MRI with **derived FA, TBSS, VBM** and **clinical CSVs**.

* **Scope:** AD, BD, and healthy controls (anonymized)
* **Analyses:** FSL (DTI/TBSS), SPM (VBM); registration to MNI
* **License:** **CC BY 4.0**
* **Citation/DOI:** Besga, Graña, Chyzhyk (2020). Zenodo. [https://doi.org/10.5281/zenodo.3935636](https://doi.org/10.5281/zenodo.3935636)
* **Use cases:** AD vs BD discrimination, biomarker correlation, CAD modeling

---

### 2) High-Quality DWI of Parkinson’s Disease (`liege-pd`)

Cross-sectional PD dataset with **120 dirs**, **b=1000/2500 s/mm²**, **2.4 mm³** voxels; matched controls.

* **N:** 27 PD, 26 controls
* **Sequence:** Twice-refocused spin-echo (reduced eddy currents)
* **License:** **CC BY-SA**
* **Source:** NITRC “parktdi” (see release for link)
* **Use cases:** PD microstructure, group comparisons, denoising/EDDY benchmarks

---

### 3) Inter-Site Reproducibility in Small Vessel Disease (`isd-svd`)

**CADASIL** patients scanned on **Siemens Prisma & Skyra** within 24 h; BIDS, raw+preprocessed DWI.

* **N:** 10 CADASIL patients; matched protocols across sites
* **Preproc:** dcm2niix → MRtrix (dwidenoise/mrdegibbs) → FSL (TOPUP/EDDY)
* **Artifacts control:** Multiband=3; reverse-PE; harmonized resolution & directions
* **License:** **CC BY-NC 4.0**
* **Citation/DOI:** Dewenter, Gesierich, Duering (2020). Zenodo. [https://doi.org/10.5281/zenodo.16925507](https://doi.org/10.5281/zenodo.16925507)
* **Assoc. paper:** Neurology 96(5): e698–e708 (2020)
* **Use cases:** Inter-scanner reproducibility, harmonization (e.g., ComBat/LongCombat), SVD biomarkers

---

## Quick Start

### Download

Use the **Releases** tab to fetch archives and per-subject assets (e.g., `*.nii.gz`, `.bval`, `.bvec`, clinical `*.csv`, QC `qc.tsv`, and DSI Studio `*.sz/*.fz` derivatives when available).

### Open in DSI Studio (examples)

* **From NIfTI:** Reconstruct with GQI/DTI using `.nii.gz + .bval + .bvec`.
* **From `*.sz`:** Load prebuilt SRC; reconstruct to FIB (`*.fz`) with chosen model (GQI/DTI/QSDR).
* **Tractography/QC:** Verify b-table, inspect reverse-PE pairs, and review `qc.tsv` where provided.

> Keep a record of **software versions** and **parameters** for reproducibility.

---

## Suggested Analyses

* **Group comparisons:** AD vs BD vs HC; PD vs control; CADASIL inter-site agreement
* **Biomarker links:** FA/TBSS/VBM vs clinical/biochemical measures
* **Harmonization:** Inter-scanner/site harmonization (e.g., NeuroCombat/LongCombat)
* **CAD modeling:** Train/test pipelines for disease classification (respect license/DUA limits)

---

## Data Format & Structure

* **Images:** NIfTI (`.nii/.nii.gz`), with accompanying `.bval/.bvec`
* **Derivatives:** TBSS/FA maps, VBM, and DSI Studio reconstructions (`*.gqi.fz`, `*.qsdr.fz`, `*.sz`) where available
* **Organization:** Some releases are **BIDS**; see each release notes for folder layout (e.g., `/sub-XX/ses-prisma` vs `/ses-skyra`)
* **Clinical data:** CSV files with anonymized IDs and diagnostic keys (e.g., `crl`, `tb`, `ea`)

---

## Licensing & Citation

* **ubc-ad_bd:** CC BY 4.0 — cite Besga et al., Zenodo (2020)
* **liege-pd:** CC BY-SA — acknowledge source (NITRC parktdi)
* **isd-svd:** CC BY-NC 4.0 — cite Dewenter et al., Zenodo (2020) + Neurology 2020

You **must** follow the **original license** of each dataset and **cite** the listed sources in publications.

---

## Caveats

* Some releases include **preprocessed** and **raw** data—verify pipelines before mixing.
* **Non-commercial** clauses (e.g., CC BY-NC) may restrict downstream use.
* Anonymization/defacing methods vary—confirm suitability for face-sensitive analyses.

