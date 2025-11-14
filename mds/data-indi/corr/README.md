# Consortium for Reliability and Reproducibility (CoRR)

The **Consortium for Reliability and Reproducibility (CoRR)** was created to provide an open-science resource for **test–retest reliability** and **reproducibility** studies in functional and structural connectomics.

This repository collects and documents CoRR test–retest datasets that have been mirrored and/or processed by the **Pittsburgh Fiber Data Hub**, with helper files to simplify downstream analysis.

> Upstream data are shared via the **International Neuroimaging Data-sharing Initiative (INDI)** and the **1000 Functional Connectomes Project**.

---

## Goals of CoRR

CoRR was established to:

1. **Establish test–retest reliability and reproducibility** for commonly used MR-based connectome metrics.
2. **Characterize variability across sites and designs**, including differences in reliability across imaging centers, scanners, and retest intervals.
3. **Provide benchmark datasets** for evaluating new metrics, preprocessing pipelines, and analysis methods.

Because CoRR is primarily a **retrospective aggregation**, its **phenotypic key** emphasizes variables that are:

* **Core:** Minimal variables necessary to characterize any dataset (e.g., age, sex).
* **Preferred:** Recommended variables that are important and likely to be collected across sites.
* **Optional:** Dataset-specific variables contributed by a subset of sites (e.g., task performance, specialized scales).

---

## CoRR Organization

* **Consortium Founders:** Xi-Nian Zuo, Michael P. Milham
* **Project Coordinator:** Xi-Nian Zuo
* **Data Aggregation & Organization:**
  David O’Connor, Daniel Lurie, Erica Ho, Michael P. Milham, Ting Xu, Xi-Nian Zuo
* **Website:** Daniel Lurie
* **Database Support:** Vince Calhoun, Wil Courtney, Margaret King

More information and global CoRR documentation are available via the INDI/CoRR web pages.

---

## What this repository provides

For each CoRR dataset mirrored under `data-indi/corr`, this repository aims to provide:

* **Short dataset summaries** (site, design, sample size, modalities, DOI).
* **Pointers to upstream downloads** (NITRC / INDI project pages).
* **Helper artifacts** when available, such as:

  * `participants.tsv`
  * `qc.tsv`
  * Tractography-ready files (`*.gqi.fz`, `*.qsdr.fz`, `*.sz`, `*.dti.dz`, `*.gqi.dz`)

All raw imaging data remain hosted by **INDI / NITRC** and are subject to the **INDI / CoRR Data Use Agreement**.

---

## Releases in `data-indi/corr`

### XHCUMS — 6-Month Test–Retest Dataset

**Dataset:** *Xuanwu Hospital, Capital Medical University (XHCUMS) – 6-Month Test–Retest Dataset*
**DOI:** `10.15387/fcp_indi.corr.xhcums1`
**Site:** Xuanwu Hospital, Capital Medical University, Beijing, China
**Sample:** 24 healthy adults, **5 sessions each**, spaced **6 months** apart
**Modalities:** T1-weighted, resting-state fMRI (EPI), DTI
**Condition:** Rest, eyes closed (blank screen, no task)

**Use cases:** Long-term reliability of morphometry, functional connectivity, and diffusion metrics.

**Access:**

* Imaging: `XHCUMS_0025982 – XHCUMS_0026006` via NITRC (INDI group, login required)
* CoRR page: `http://fcon_1000.projects.nitrc.org/indi/CoRR/html/xhcums1.html`

**This repo (examples):**

* `corr-xhcums.dti.dz`, `corr-xhcums.gqi.dz`
* `participants.tsv`, `qc.tsv`, subject-level `*_dwi.*.fz` and `*_T1w.nii.gz`

---

### SWU1 — Training Effects for Attention Blink Task

**Dataset:** *Southwest University (SWU) – Training Effects for Attention Blink Task*
**DOI:** `10.15387/fcp_indi.corr.swu1`
**Site:** Faculty of Psychology, Southwest University, Chongqing, China
**Sample:** 20 healthy adults
**Design:** 2 sessions — **pre-training** and **post-training** on an attention blink paradigm
**Modalities:** T1-weighted, resting-state fMRI (two sessions)
**Condition:** Rest, eyes closed

**Use cases:** Training-induced changes and test–retest reliability of resting-state networks.

**Access:**

* Imaging: `SWU_1_0027203 – SWU_1_0027222` via NITRC (login required)
* Phenotypes: `SWU1_Phenotypic_Data`
* CoRR page: `http://fcon_1000.projects.nitrc.org/indi/CoRR/html/swu1.html`

---

### NKI — Test–Retest Multiband fMRI and DTI

**Dataset:** *Nathan Kline Institute (NKI) – Test–Retest Multiband fMRI and DTI Dataset*
**DOI:** `10.15387/fcp_indi.corr.nki1`
**Site:** Nathan S. Kline Institute for Psychiatric Research, Orangeburg, NY, USA
**Sample:** 24 participants, multi-session design
**Modalities:** Multiband resting-state fMRI (TR 645 ms, 1400 ms, 2500 ms) and DTI (137 directions)
**Condition:** Rest, eyes open (fixation)

This dataset served as a **pilot** for the later **Enhanced NKI–Rockland Sample**, enabling comparison across TRs and modalities.

**Access:**

* Imaging: `NKI_TRT_0021001 – NKI_TRT_9630905` via NITRC (login required)
* Phenotypes: `NKI_TRT_Phenotypic_Data`
* CoRR page: `http://fcon_1000.projects.nitrc.org/indi/CoRR/html/nki1.html`

---

### MRN — Repeat Resting Sample

**Dataset:** *Mind Research Network (MRN) – Repeat Resting Sample*
**DOI:** `10.15387/fcp_indi.corr.mrn1`
**Site:** Mind Research Network (MRN), Albuquerque, NM, USA
**Sample:** 56 healthy adults, **2 sessions**, ~4 months apart
**Modalities:** T1-weighted, resting-state fMRI, DTI
**Condition:** Rest, eyes open, fixation cross

**Use cases:** Stability of intrinsic connectivity and diffusion measures across a moderate retest interval.

**Access:**

* Imaging: `MRN_0027010 – MRN_0027419` via NITRC (login required)
* Phenotypes: `MRN_Phenotypic_Data`
* CoRR page: `http://fcon_1000.projects.nitrc.org/indi/CoRR/html/mrn1.html`

---

### IPCAS1 — Time Perception and Estimation Sample

**Dataset:** *Institute of Psychology, Chinese Academy of Sciences (IPCAS 1) – Time Perception and Estimation Sample*
**DOI:** `10.15387/fcp_indi.corr.ipcas1`
**Site:** Institute of Psychology, Chinese Academy of Sciences, Beijing, China
**Sample:** 30 healthy adults, **2 sessions** one week apart
**Modalities:** Resting-state fMRI, T1-weighted, DTI
**Condition:** Rest, eyes open, fixation cross

**Use cases:** Short-term test–retest reliability and studies on time perception and individual differences.

**Access:**

* Imaging: `IPCAS_1_0025485 – IPCAS_1_0025514` via NITRC (login required)
* Phenotypes: `IPCAS_1_Phenotypic_Data`
* CoRR page: `http://fcon_1000.projects.nitrc.org/indi/CoRR/html/ipcas1.html`

---

### HNU1 — One-Month Test–Retest & Dynamical Resting-State

**Dataset:** *Hangzhou Normal University (HNU) – One-Month Test–Retest Reliability and Dynamical Resting-State Study*
**DOI:** `10.15387/fcp_indi.corr.hnu1`
**Site:** Center for Cognition and Brain Disorders, Hangzhou Normal University, Hangzhou, China
**Sample:** 30 healthy adults
**Design:** **10 sessions per subject**, spaced **3 days** apart (≈1 month)
**Modalities (per session):** EPI (resting-state fMRI), ASL, T1-weighted, DTI, T2-weighted
**Condition:** Rest, eyes open, fixation cross, no intentional task

**Use cases:** Dynamic functional connectivity, intra-subject variability, and short-term reliability across multiple modalities.

**Access:**

* Imaging: `HNU_1_0025427 – HNU_1_0025456` via NITRC (login required)
* Phenotypes: `HNU_1_Phenotypic_Data`
* CoRR page: `http://fcon_1000.projects.nitrc.org/indi/CoRR/html/hnu1.html`

---

### BNU1 — C-BIRD, 6-Week Test–Retest

**Dataset:** *Beijing Normal University (BNU) – Connectivity-Based Brain Imaging Research Database (C-BIRD)*
**DOI:** `10.15387/fcp_indi.corr.bnu1`
**Site:** State Key Laboratory of Cognitive Neuroscience and Learning, and IDG/McGovern Institute for Brain Research, BNU, Beijing, China
**Sample:** 57 healthy young adults (30 male / 27 female, age 19–30)
**Design:** 2 sessions **~6 weeks** apart (40.9 ± 4.5 days)
**Modalities:** Resting-state fMRI, T1-weighted, T2-weighted, DTI
**Condition:** Rest, eyes closed

**Use cases:** Reliability and temporal stability of functional and structural connectivity in young adults.

**Access:**

* Imaging: `BNU_1_0025864 – BNU_1_0025920` via NITRC (login required)
* Phenotypes: `BNU_Phenotypic_Data`
* CoRR page: `http://fcon_1000.projects.nitrc.org/indi/CoRR/html/bnu1.html`

---

## How to access the data

1. Create an account on **NITRC**.
2. Request to join the **INDI / 1000 Functional Connectomes Project** group.
3. After approval, navigate to the corresponding **CoRR dataset page** (see links above) and download imaging and phenotypic files.

Some assets in this repository mirror or summarize those datasets (e.g., `participants.tsv`, `qc.tsv`, `.fz/.dz` derivatives) for easier integration into analysis pipelines.

---

## Licensing and data use

Use of CoRR datasets is governed by the **INDI / CoRR Data Use Agreement**:

> `http://fcon_1000.projects.nitrc.org/indi/corr/html/data_citation.html`

In general:

* Datasets are for **research use only**.
* Users must **not attempt re-identification** of participants.
* Users must follow any **site-specific restrictions** and **citation requirements** listed on the dataset page.

Check each project page for the precise license (e.g., site-specific acknowledgments, additional terms).

---

## How to cite

Always:

1. **Cite the original dataset / DOI** and relevant publications (e.g., site-specific reliability papers).
2. Acknowledge **CoRR**, **INDI**, and the contributing site(s) as specified on their citation page.
3. When using derivatives or helper files from this repository, add:

> “Processed artifacts and curation were prepared by the Pittsburgh Fiber Data Hub (`data-indi/corr`) based on INDI/CoRR datasets.”

---

## Disclaimer

* All data originate from **independent sites** and are shared **as-is**.
* Sequence parameters, scanner models, and instructions (eyes open/closed, fixation, etc.) differ across datasets.
* Users are responsible for:

  * Performing appropriate **quality control** (motion, artifacts, etc.).
  * Choosing analysis pipelines that account for **site differences**, **TR differences**, and **multiband acquisition** when applicable.

---

**Repository:** `data-indi/corr` — CoRR Test–Retest Reliability & Reproducibility Datasets curated by the Pittsburgh Fiber Data Hub.
