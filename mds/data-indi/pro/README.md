# INDI Prospective Studies — data-indi/pro

Curated, ready-to-use subsets of **INDI (International Neuroimaging Data-sharing Initiative)** prospective releases, prepared for the Pittsburgh Fiber Data Hub. This repository aggregates links, metadata, and selected derived artifacts (e.g., QC tables, tractography-ready files) to simplify reuse in methods and replication studies.

> **Access note:** These datasets are hosted on external portals (mostly NITRC). Most downloads require a free account and joining the **1000 Functional Connectomes Project (FCP/INDI)** group. Please review each dataset’s license and acknowledgments before use.

---

## Table of contents

* [What’s included](#whats-included)
* [Releases](#releases)

  * [NYU IPN — Adult Resting-State & DTI](#nyu-ipn--adult-resting-state--dti)
  * [Enhanced NKI-RS — Multiband Test–Retest Pilot](#enhanced-nki-rs--multiband-testretest-pilot)
  * [NKI / Rockland Sample](#nki--rockland-sample)
  * [Beijing Normal University — Short TR Sample](#beijing-normal-university--short-tr-sample)
* [How to cite](#how-to-cite)
* [Licensing](#licensing)
* [Known overlaps / deduplication](#known-overlaps--deduplication)
* [Disclaimer](#disclaimer)
* [Contact](#contact)

---

## What’s included

* **Release pages** describing each dataset (scope, modalities, phenotypes, acknowledgments).
* **Pointers to upstream downloads** (NITRC / project pages).
* When available, **helper assets** (e.g., `participants.tsv`, `qc.tsv`, FIB/FZ/SZ derivatives) to speed up analysis.

---

## Releases

### NYU IPN — Adult Resting-State & DTI

**Dataset:** *NYU Institute for Pediatric Neuroscience (IPN) – Adult Resting-State and Diffusion MRI Dataset*
**Institution:** NYU School of Medicine (Phyllis Green & Randolph Cōwen IPN)
**Sample:** 49 psychiatrically screened, neurotypical adults (adult subset of a larger 6–55y project)
**Modalities:** 6-min R-fMRI (1–2 runs/session, Rest_1 before Rest_2), T1-MPRAGE, two 64-direction DTI scans
**Phenotypes:** Age, gender, IQ (WASI verbal/performance/composite)
**License:** CC BY-NC

**Access:** Data are hosted via NITRC under the 1000 Functional Connectomes Project.

* *Imaging:* `NYU.001.001.LiteNIFTI.part1–3` (login required)
* *Phenotypes:* Included within the NITRC package
  **Source:** Project page — [http://fcon_1000.projects.nitrc.org/indi/retro/nyu_ipn.html](http://fcon_1000.projects.nitrc.org/indi/retro/nyu_ipn.html)

**Acknowledgment to include:**

> “Financial support for the data used in this project was partially provided by grants from the NIMH (R01MH083246), Autism Speaks, the Stavros Niarchos Foundation, the Leon Levy Foundation, and the endowment provided by Phyllis Green and Randolph Cōwen.”

**Duplication warning:** Some participants also appear in **NewYork_a** (FCP classic) and **NYU_Cocaine** (INDI retrospective). Avoid combining without deduplication.

---

### Enhanced NKI-RS — Multiband Test–Retest Pilot

**Dataset:** *Enhanced Nathan Kline Institute–Rockland Sample (NKI-RS) – Multiband Imaging Test–Retest Pilot*
**Institution:** Nathan Kline Institute, Orangeburg, NY, USA
**PI:** Michael Milham
**DOI:** `10.15387/fcp_indi.corr.nki1`
**Purpose:** Evaluate test–retest reliability of **multiband** R-fMRI/DTI prior to full 1,000-participant rollout
**Modalities:** R-fMRI (multi-TR, multiband), DTI (137 dirs), task fMRI (checkerboard, breath-hold, eye-movement)
**Phenotyping:** Drawn from original NKI-RS cohort (clinical history not exclusionary)

**Key sequences (test–retest):**

* R-mfMRI **TR 645 ms**, 3 mm iso, 10 min (high temporal resolution)
* R-mfMRI **TR 1400 ms**, 2 mm iso, 10 min (high spatial resolution)
* R-fMRI **TR 2500 ms**, 3 mm iso, 5 min (standard)
* DTI **137 dirs**, 2 mm iso

**Tasks:** visual checkerboard, eye-movement calibration, breath-holding (includes stimulus design/execution scripts).

**Multiband notes:**

* Short TR alters temporal autocorrelation; adjust preprocessing accordingly.
* Spatial smoothness may be non-uniform; GRF cluster corrections may be unsuitable.
* Use correct slice-timing for SMS acquisitions (custom timing files).

**Access:** NITRC (login required).
**Source:** [http://fcon_1000.projects.nitrc.org/indi/enhanced/nki_rs.html](http://fcon_1000.projects.nitrc.org/indi/enhanced/nki_rs.html)

**Included assets (this repo, when present):**

* `participants.tsv`, `qc.tsv`
* Example derivatives: `*.gqi.fz`, `*.qsdr.fz`, `*.sz`

**Funding (abbrev.):** NIMH BRAINS R01MH094639-01, NYS OMH/RFMH, Child Mind Institute, CABI, NIMH R01MH081218/083246/ R21MH084126, Brain Research Foundation, Stavros Niarchos Foundation.
**Core team:** Milham, Leventhal, Castellanos, Nooner, Tobe, Colcombe; technical support incl. Hu, Sangoi, Zavitz, Craddock, Li, Cheung, Khanuja, Lewis, Yan; CMRR collaboration for multiband EPI (Ugurbil, Auerbach, Xu, Moeller).

**Citation:**
Milham M., Colcombe S., Castellanos F.X., *et al.* **Enhanced NKI-RS – Multiband Imaging Test–Retest Pilot**. Nathan Kline Institute. DOI: 10.15387/fcp_indi.corr.nki1.

---

### NKI / Rockland Sample

**Dataset:** *Nathan Kline Institute (NKI) / Rockland Sample*
**Institution:** NKI, Orangeburg, NY, USA
**PIs:** F. X. Castellanos, Bennett Leventhal, Michael Milham
**Coordinator:** Kate Nooner
**Sample:** Ages 4–85, community-ascertained; **prospective** weekly releases with randomized delay
**Modalities:** 10-min R-fMRI; DTI (6-dir and 64-dir 2 mm iso); high-res and short-seq MPRAGE; T2; extensive phenotyping
**Protocol:** Aligned with Brain Genomics Superstruct Project to aid cross-site comparability

**Release cadence (historical):** 5–10 new individuals/week; **total 207** datasets; completed **Aug 15, 2011**.
**Access:** NITRC (DICOM/NIfTI/Lite variants; login required).
**Source:** [http://fcon_1000.projects.nitrc.org/indi/enhanced/nki_rs.html](http://fcon_1000.projects.nitrc.org/indi/enhanced/nki_rs.html)

**Funding (abbrev.):** NYS OMH, RFMH, NIH P50 MH086385-S1, NKI CABI, Brain Research Foundation, Stavros Niarchos Foundation.
**Team members (abbrev.):** Benedict, Biswal, Coffey, Colcombe, Guilfoyle, Gutman, Koplewicz, Hoptman, Javitt, Maayan, Mennes, Nooner, Pomara.

---

### Beijing Normal University — Short TR Sample

**Dataset:** *Beijing Normal University – Short TR Sample*
**Institution:** State Key Laboratory of Cognitive Neuroscience and Learning, BNU, Beijing
**Sample:** 28 healthy college-aged volunteers
**Design:** Within-subject **paired TR** comparison in R-fMRI (TR = 0.4 s vs 2.0 s) plus T1 and 64-dir DTI
**License:** CC BY-NC

**Imaging:**

* R-fMRI **TR 2.0 s** — 8 min, **240** volumes
* R-fMRI **TR 0.4 s** — 8 min, **1200** volumes
* T1-MPRAGE (defaced), DTI **64 dirs** (2 mm iso)
* Demographics: age, sex

**Access:** NITRC under FCP/INDI (login required).
**Source:** [http://fcon_1000.projects.nitrc.org/indi/retro/BeijingShortTR.html](http://fcon_1000.projects.nitrc.org/indi/retro/BeijingShortTR.html)

**Acknowledgment to include:**

> “Financial support for the data used in this project was provided by the National Natural Science Foundation of China (30770594) and the National High Technology Program of China (863) (2008AA02Z405).”

---

## How to cite

Please cite the **original dataset** (and DOI when provided) and acknowledge **funding statements** listed above. When using derivatives or helper assets from this repository, add:

> “Processed artifacts and curation were prepared by the Pittsburgh Fiber Data Hub (data-indi/pro).”

---

## Licensing

Unless noted otherwise on the upstream project pages, these datasets are released under **Creative Commons Attribution–NonCommercial (CC BY-NC)**.
You may share and adapt for **non-commercial research** with proper attribution. Check each dataset’s page for any additional terms.

---

## Known overlaps / deduplication

* **NYU IPN (Adult subset)** contains participants who also appear in **NewYork_a (FCP classic)** and **NYU_Cocaine** retrospective releases. De-duplicate before pooling samples.

---

## Disclaimer

* Datasets are provided **as-is** by their originating institutions.
* Users are responsible for **quality control**, motion assessment, and choosing appropriate preprocessing (especially for **multiband** and **short-TR** data).

---

## Contact

For questions about curation/derivatives in this repo: open an **Issue** on GitHub.
For access problems or upstream metadata, contact the **INDI / NITRC** project maintainers via their portals.

---

**Repository:** `data-indi/pro` — INDI Prospective Data Sharing Samples.
