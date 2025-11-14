# INDI Prospective Studies

Curated, ready-to-use subsets of **INDI (International Neuroimaging Data-sharing Initiative)** prospective releases, prepared for the **Pittsburgh Fiber Data Hub**. This repository aggregates links, metadata, and selected derived artifacts (e.g., QC tables, tractography-ready files) to simplify reuse in methods and replication studies.

> **Access note:** Source data are hosted on external portals (mostly **NITRC**). Most downloads require a free account and joining the **1000 Functional Connectomes Project (FCP/INDI)** group. Please review each dataset’s license and acknowledgments before use.

---

## What this repository provides

For each dataset mirrored under `data-indi/pro`, this repository aims to provide:

* A short **dataset overview** (scope, modalities, phenotyping, design).
* **Pointers** to upstream NITRC / INDI project pages.
* When available, helper artifacts such as:

  * `participants.tsv`
  * `qc.tsv`
  * Tractography-ready derivatives (`*.gqi.fz`, `*.qsdr.fz`, `.sz`, `.dti.dz`, `.gqi.dz`)

All raw imaging data remain hosted by **INDI / NITRC** and are subject to the corresponding **data use agreements**.

---

## NYU IPN — Adult Resting-State & DTI

**Dataset:** NYU Institute for Pediatric Neuroscience (IPN) – Adult Resting-State and Diffusion MRI
**Institution:** Phyllis Green & Randolph Cōwen IPN, NYU School of Medicine
**Sample:** 49 psychiatrically screened, neurotypical adults (adult subset of a larger 6–55y project)
**Modalities:**

* 6-min resting-state fMRI (1–2 runs per session; Rest_1 always before Rest_2)
* High-resolution T1-weighted MPRAGE (defaced)
* Two 64-direction DTI scans per participant

**Phenotypes:** Age, gender, IQ (WASI verbal / performance / composite)
**License:** Creative Commons Attribution–NonCommercial (CC BY-NC)

The current release represents the adult portion of a larger normative connectivity project. Most subjects have two R-fMRI runs within one visit (< 1 hour apart), making this useful for:

* Short-interval **test–retest** of resting-state measures
* Structure–function analyses combining DTI and R-fMRI
* Method development for motion handling and reliability

> ⚠️ Some participants also appear in **NewYork_a** (FCP classic) and **NYU_Cocaine** (INDI retrospective). De-duplicate before pooling.

**Upstream source:**
Project page — [http://fcon_1000.projects.nitrc.org/indi/retro/nyu_ipn.html](http://fcon_1000.projects.nitrc.org/indi/retro/nyu_ipn.html)

### Download (Linux / macOS — bash)

```bash
curl -s https://api.github.com/repos/data-indi/pro/releases/tags/nyu | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
```

### Download (Windows PowerShell 5.x)

```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-indi/pro/releases/tags/nyu").assets | ForEach-Object { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```

---

## Enhanced NKI-RS — Multiband Test–Retest Pilot

**Dataset:** Enhanced Nathan Kline Institute–Rockland Sample (NKI-RS) – Multiband Imaging Test–Retest Pilot
**Institution:** Nathan S. Kline Institute for Psychiatric Research (NKI), Orangeburg, NY, USA
**PI:** Michael Milham
**DOI:** `10.15387/fcp_indi.corr.nki1`
**Sample:** Adults drawn from the original NKI-RS cohort (not excluding clinical history)

**Purpose:**
Pilot phase to evaluate the **reliability** and **reproducibility** of advanced multiband R-fMRI and high-direction DTI protocols prior to the full 1,000-participant enhanced NKI-RS rollout.

**Key multiband / test–retest sequences:**

* R-mfMRI: **TR 645 ms**, 3 mm iso, 10 min (high temporal resolution)
* R-mfMRI: **TR 1400 ms**, 2 mm iso, 10 min (high spatial resolution)
* R-fMRI: **TR 2500 ms**, 3 mm iso, 5 min (standard reference)
* DTI: **137 directions**, 2 mm iso

**Tasks:** Visual checkerboard, eye-movement calibration, breath-hold (with stimulus design scripts).

This dataset is well suited for:

* Comparing different **TRs** and sampling regimes
* Evaluating **multiband preprocessing** strategies
* Multimodal test–retest analyses across R-fMRI and DTI

**Upstream source:**
Enhanced NKI-RS page — [http://fcon_1000.projects.nitrc.org/indi/enhanced/nki_rs.html](http://fcon_1000.projects.nitrc.org/indi/enhanced/nki_rs.html)

**Typical assets in this repo:**

* `nki-pilot.dti.dz`, `nki-pilot.gqi.dz`
* `participants.tsv`, `qc.tsv`
* Subject-level `*_dwi.*.fz` and `*_T1w.nii.gz`

### Download (Linux / macOS — bash)

```bash
curl -s https://api.github.com/repos/data-indi/pro/releases/tags/nki-pilot | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
```

### Download (Windows PowerShell 5.x)

```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-indi/pro/releases/tags/nki-pilot").assets | ForEach-Object { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```

---

## NKI / Rockland Sample

**Dataset:** Nathan Kline Institute (NKI) / Rockland Sample
**Institution:** NKI, Orangeburg, NY, USA
**PIs:** F. Xavier Castellanos, Bennett Leventhal, Michael Milham
**Coordinator:** Kate Nooner
**Sample:** Community-ascertained 4–85-year-olds, prospectively released; **207** participants total

The NKI/Rockland Sample is a large, phenotypically rich resource for **lifespan** and **psychiatric** connectomics, with deep behavioral and clinical characterization.

**Core imaging protocol per participant:**

* 10-min resting-state fMRI (R-fMRI)
* 6-direction DTI
* 64-direction DTI (2 mm iso)
* High-resolution MPRAGE (structural T1)
* Short-sequence MPRAGE
* T2-weighted structural scan

All participants undergo semi-structured psychiatric interviews plus a comprehensive neuropsychological and behavioral battery, enabling:

* Brain–behavior modeling across the lifespan
* Dimensional analyses of psychopathology
* Method development in large, heterogeneous samples

**Upstream source:**
Enhanced NKI-RS main page — [http://fcon_1000.projects.nitrc.org/indi/enhanced/nki_rs.html](http://fcon_1000.projects.nitrc.org/indi/enhanced/nki_rs.html)

**This repo:**
Provides selected derivatives (when available) and helper tables to simplify working with the NKI/Rockland releases.

### Download (Linux / macOS — bash)

```bash
curl -s https://api.github.com/repos/data-indi/pro/releases/tags/nki | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
```

### Download (Windows PowerShell 5.x)

```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-indi/pro/releases/tags/nki").assets | ForEach-Object { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```

---

## Beijing Normal University — Short TR Sample

**Dataset:** Beijing Normal University – Short TR Sample
**Institution:** State Key Laboratory of Cognitive Neuroscience and Learning, Beijing Normal University, Beijing, China
**Sample:** 28 healthy college-aged volunteers
**Design:** Within-subject comparison of **two TR conditions** in R-fMRI

**Imaging protocol:**

* Resting-state fMRI (long TR): **TR = 2.0 s**, 8 min, 240 volumes
* Resting-state fMRI (short TR): **TR = 0.4 s**, 8 min, 1200 volumes
* T1-weighted MPRAGE (defaced)
* 64-direction DTI (2 mm iso)
* Demographics: age, sex

Participants completed both R-fMRI TR conditions in a single session, supporting:

* Direct comparison of **short vs long TR** for connectivity measures
* Evaluation of temporal sampling effects, SNR, and reliability
* Combined structure/function analyses with DTI

**Upstream source:**
Project page — [http://fcon_1000.projects.nitrc.org/indi/retro/BeijingShortTR.html](http://fcon_1000.projects.nitrc.org/indi/retro/BeijingShortTR.html)

**Note:** Data were released in multiple LiteNIFTI batches (BeijingShortTR.001.001 – BeijingShortTR.009.001) totaling 28 subjects.

### Download (Linux / macOS — bash)

```bash
curl -s https://api.github.com/repos/data-indi/pro/releases/tags/bnu | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
```

### Download (Windows PowerShell 5.x)

```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-indi/pro/releases/tags/bnu").assets | ForEach-Object { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```

---

## How to cite

For any analysis using these data:

1. **Cite the original dataset** (and DOI where provided), plus key publications from each project.
2. Include required **funding acknowledgments** from the upstream project pages.
3. When you use derivatives or helper files from this repository, please add:

> “Processed artifacts and curation were prepared by the Pittsburgh Fiber Data Hub (`data-indi/pro`).”

---

## Licensing

Unless otherwise specified on the upstream pages, these datasets are distributed under **Creative Commons Attribution–NonCommercial (CC BY-NC)**:

* You may **share** and **adapt** the material for **non-commercial research**, with proper attribution.
* Always check each dataset’s NITRC / INDI page for **dataset-specific conditions** or additional restrictions.

---

## Known overlaps / deduplication

* **NYU IPN (adult subset)** contains participants who also appear in **NewYork_a** (FCP classic) and **NYU_Cocaine** (INDI retrospective).

  * If you combine these datasets, perform **subject-level deduplication** to avoid double-counting individuals.

Similar overlaps may exist between the NKI/Rockland Sample and related NKI multiband test–retest datasets; check subject IDs if pooling.

---

## Disclaimer

* All data originate from **independent sites** and are redistributed **as-is**.
* Acquisition parameters, scanner models, and instructions (eyes open/closed, fixation, etc.) vary across datasets.
* Users are responsible for:

  * Performing appropriate **quality control** (e.g., motion, artifacts).
  * Choosing preprocessing pipelines suitable for **multiband** and **short-TR** acquisitions.
  * Respecting all **data use agreements** and **licensing terms**.

---

**Repository:** `data-indi/pro` — INDI Prospective Data Sharing Samples curated by the Pittsburgh Fiber Data Hub.
