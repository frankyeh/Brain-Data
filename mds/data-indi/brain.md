# International Neuroimaging Data-sharing Initiative (INDI)

The **International Neuroimaging Data-sharing Initiative (INDI)** aims to advance discovery science in human brain function by promoting large-scale, open sharing of resting-state fMRI (R-fMRI) and phenotypic data. INDI builds on the success of the **1000 Functional Connectomes Project (FCP)**, which demonstrated the feasibility and impact of aggregating and openly releasing multi-site imaging datasets.

---

## Background

The 1000 Functional Connectomes Project launched on **December 11, 2009**, aggregating and releasing over **1200 R-fMRI datasets** collected from **33 sites worldwide**. Released through NITRC, the dataset generated immediate and widespread engagement, including:

* **9000+ downloads** within 6 months
* Access from **1,223 cities in 78 countries**
* Coverage in *Nature Medicine*, *Nature Methods*, and the NIMH Director’s blog
* The landmark feasibility paper (Biswal et al., 2010, PNAS), downloaded **1000+ times** in two weeks

The scientific impact was further demonstrated by rapid independent publications using the shared data (e.g., Tomasi & Volkow, 2010).

The response highlighted a clear need: **the neuroimaging community requires large, openly accessible datasets** to overcome barriers to statistical power, reproducibility, and cross-disciplinary involvement.

All raw imaging data remain hosted by **INDI / NITRC** and are subject to the **INDI / CoRR Data Use Agreement**.

---

## XHCUMS — 6-Month Test–Retest Dataset

**Dataset:** Xuanwu Hospital, Capital Medical University (XHCUMS) – 6-Month Test–Retest Dataset
**DOI:** `10.15387/fcp_indi.corr.xhcums1`
**Site:** Xuanwu Hospital, Capital Medical University, Beijing, China
**Sample:** 24 healthy adults, **5 sessions per subject**, **6-month** intervals
**Modalities:** T1-weighted anatomical, resting-state fMRI (EPI), diffusion MRI (DTI)
**Condition:** Rest, **eyes closed**, blank screen, no task

This dataset was designed to evaluate long-term test–retest reliability of structural, functional, and diffusion MRI measures. Each participant was scanned five times over ~2 years, providing dense longitudinal data for:

* Morphometry and cortical thickness
* Intrinsic functional connectivity
* Diffusion-based white-matter mapping

Typical assets in this repo include multi-modal group derivatives such as `corr-xhcums.dti.dz`, `corr-xhcums.gqi.dz`, `participants.tsv`, `qc.tsv`, and subject-level `*_dwi.*.fz` files.

### Download (Linux / macOS — bash)

```bash
curl -s https://api.github.com/repos/data-indi/corr/releases/tags/xhcums | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
```

### Download (Windows PowerShell 5.x)

```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-indi/corr/releases/tags/xhcums").assets | ForEach-Object { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```

---

## SWU1 — Training Effects for Attention Blink Task

**Dataset:** Southwest University (SWU1) – Training Effects for Attention Blink Task
**DOI:** `10.15387/fcp_indi.corr.swu1`
**Site:** Faculty of Psychology, Southwest University, Chongqing, China
**Sample:** 20 healthy adults
**Design:** 2 sessions — **pre-training** and **post-training** on an attention blink paradigm
**Modalities:** T1-weighted structural MRI, resting-state fMRI (two sessions)
**Condition:** Rest, **eyes closed**, no task

Participants completed an **attention blink** training paradigm between scans, enabling:

* Pre/post comparison of resting-state networks
* Evaluation of training-induced plasticity
* Test–retest reliability analysis in a short longitudinal design

Assets in this repo typically include subject-level `*_T1w.nii.gz`, resting-state fMRI derivatives, tractography-ready `.fz` files, and QC tables.

### Download (Linux / macOS — bash)

```bash
curl -s https://api.github.com/repos/data-indi/corr/releases/tags/swu | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
```

### Download (Windows PowerShell 5.x)

```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-indi/corr/releases/tags/swu").assets | ForEach-Object { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```

---

## NKI — Test–Retest Multiband fMRI and DTI

**Dataset:** Nathan Kline Institute – Test–Retest Multiband fMRI and DTI Dataset
**DOI:** `10.15387/fcp_indi.corr.nki1`
**Site:** Nathan S. Kline Institute for Psychiatric Research, Orangeburg, NY, USA
**Sample:** 24 participants, multi-session test–retest
**Modalities:** Multiband resting-state fMRI (TR = 645 ms, 1400 ms, 2500 ms), DTI (137 directions)
**Condition:** Resting-state, **eyes open**, fixation

This dataset served as a **pilot** for the Enhanced NKI–Rockland Sample (NKI–RS), enabling:

* Test–retest reliability analysis across **multiple TRs**
* Multimodal comparisons between diffusion and functional measures
* Methods development for multiband fMRI and dynamic connectivity

This repo includes tractography-ready `.dti.dz`, `.gqi.dz`, subject-level `.fz` files, and QC information.

### Download (Linux / macOS — bash)

```bash
curl -s https://api.github.com/repos/data-indi/corr/releases/tags/nki | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
```

### Download (Windows PowerShell 5.x)

```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-indi/corr/releases/tags/nki").assets | ForEach-Object { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```

---

## MRN — Repeat Resting Sample

**Dataset:** Mind Research Network (MRN) – Repeat Resting Sample
**DOI:** `10.15387/fcp_indi.corr.mrn1`
**Site:** Mind Research Network, Albuquerque, NM, USA
**Sample:** 56 healthy adults, **2 sessions**, ~4 months apart
**Modalities:** T1-weighted anatomical MRI, resting-state fMRI, DTI
**Condition:** Rest, **eyes open**, fixation cross

Participants were scanned twice with a ~four-month interval, providing:

* **Reproducibility benchmarks** for resting-state networks
* Stability measures for diffusion-based connectivity
* Data to evaluate intra-individual variability over longer intervals

Data here include group `.dti.dz` / `.gqi.dz` files, subject-level tractography-ready `.fz` data, and QC tables.

### Download (Linux / macOS — bash)

```bash
curl -s https://api.github.com/repos/data-indi/corr/releases/tags/mrn | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
```

### Download (Windows PowerShell 5.x)

```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-indi/corr/releases/tags/mrn").assets | ForEach-Object { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```

---

## IPCAS1 — Time Perception and Estimation Sample

**Dataset:** Institute of Psychology, Chinese Academy of Sciences (IPCAS 1) – Time Perception and Estimation Sample
**DOI:** `10.15387/fcp_indi.corr.ipcas1`
**Site:** Institute of Psychology, Chinese Academy of Sciences, Beijing, China
**Sample:** 30 healthy adults, **2 sessions** one week apart
**Modalities:** Resting-state fMRI, T1-weighted anatomical MRI, DTI
**Condition:** Rest, **eyes open**, fixation cross

This dataset supports work on:

* Neural mechanisms of **time perception and estimation**
* Short-term test–retest reliability (1-week interval)
* Structure–function relationships involving the amygdala and other regions

The repo includes multi-modal group `.dz` files, `participants.tsv`, `qc.tsv`, and subject-level `.fz` derivatives.

### Download (Linux / macOS — bash)

```bash
curl -s https://api.github.com/repos/data-indi/corr/releases/tags/ipcas | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
```

### Download (Windows PowerShell 5.x)

```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-indi/corr/releases/tags/ipcas").assets | ForEach-Object { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```

---

## HNU1 — One-Month Test–Retest & Dynamical Resting-State

**Dataset:** Hangzhou Normal University (HNU) – One-Month Test–Retest Reliability and Dynamical Resting-State Study
**DOI:** `10.15387/fcp_indi.corr.hnu1`
**Site:** Center for Cognition and Brain Disorders, Hangzhou Normal University, Hangzhou, China
**Sample:** 30 healthy adults
**Design:** **10 sessions per participant**, spaced **3 days** apart (~1 month)
**Modalities per session:** EPI (resting-state fMRI), ASL, T1-weighted, DTI, T2-weighted
**Condition:** Rest, **eyes open**, fixation cross, no intentional task

HNU1 is one of the most comprehensive CoRR resources for:

* **Dynamic functional connectivity**
* Intra-subject variability across many sessions
* Short-term reliability across multiple MRI modalities

This repo provides group `.dti.dz` / `.gqi.dz`, session-level `.fz` files, and QC/participants tables to facilitate longitudinal analyses.

### Download (Linux / macOS — bash)

```bash
curl -s https://api.github.com/repos/data-indi/corr/releases/tags/hnu | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
```

### Download (Windows PowerShell 5.x)

```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-indi/corr/releases/tags/hnu").assets | ForEach-Object { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```

---

## BNU1 — Connectivity-Based Brain Imaging Research Database (C-BIRD)

**Dataset:** Beijing Normal University (BNU) – Connectivity-Based Brain Imaging Research Database (C-BIRD)
**DOI:** `10.15387/fcp_indi.corr.bnu1`
**Site:** State Key Laboratory of Cognitive Neuroscience and Learning, and IDG/McGovern Institute for Brain Research, Beijing Normal University, Beijing, China
**Sample:** 57 healthy young adults (30 male / 27 female), ages 19–30
**Design:** 2 sessions **~6 weeks** apart (40.9 ± 4.5 days)
**Modalities:** Resting-state fMRI, T1-weighted, T2-weighted, DTI
**Condition:** Rest, **eyes closed**, no task

BNU1 supports:

* Reliability and temporal stability analyses of **functional and structural connectivity**
* Graph-theoretic connectivity and network topology studies
* Cross-session comparisons of resting-state networks and DTI-based connectomes

This repo includes BNU1 `.dti.dz` / `.gqi.dz`, `participants.tsv`, `qc.tsv`, and subject-level tractography-ready `.fz` files.

### Download (Linux / macOS — bash)

```bash
curl -s https://api.github.com/repos/data-indi/corr/releases/tags/bnu | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
```

### Download (Windows PowerShell 5.x)

```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-indi/corr/releases/tags/bnu").assets | ForEach-Object { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```

---

## How to access original data

To obtain original imaging and phenotypic data from CoRR / INDI (beyond the derivatives mirrored here):

1. Create an account on **NITRC**.
2. Request to join the **INDI / 1000 Functional Connectomes Project** group.
3. Navigate to the corresponding **CoRR dataset page** (e.g., XHCUMS, SWU1, NKI, MRN, IPCAS1, HNU1, BNU1).
4. Download imaging and phenotypic data from NITRC once access is approved.

The derivatives in this repository are intended to complement the official CoRR distributions and to facilitate **diffusion/tractography** and **connectomics** analyses.

---

## Licensing and data use

Use of CoRR datasets is governed by the **INDI / CoRR Data Use Agreement**:

> [http://fcon_1000.projects.nitrc.org/indi/corr/html/data_citation.html](http://fcon_1000.projects.nitrc.org/indi/corr/html/data_citation.html)

In general:

* Datasets are for **research use only**.
* Users must **not attempt re-identification** of participants.
* Users must follow any **site-specific restrictions** and **citation requirements** listed on the dataset page.

Check each project page for precise license terms (including acknowledgements and additional conditions).

---

## How to cite

Always:

1. **Cite the original dataset / DOI** and associated publications (e.g., site-specific reliability papers).
2. Acknowledge **CoRR**, **INDI**, and the contributing site(s) as specified on the CoRR citation page.
3. When using derivatives or helper files from this repository, please add:

> “Processed artifacts and curation were prepared by the Pittsburgh Fiber Data Hub (`data-indi/corr`) based on INDI/CoRR datasets.”

---

## Disclaimer

* All data originate from **independent sites** and are shared **as-is**.
* Sequence parameters, scanner models, and acquisition instructions (eyes open/closed, fixation, etc.) differ across datasets.
* Users are responsible for:

  * Performing appropriate **quality control** (e.g., motion, artifacts).
  * Choosing analysis pipelines that account for **site differences**, **TR differences**, and **multiband acquisition** when applicable.


