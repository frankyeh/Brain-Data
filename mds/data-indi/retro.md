# INDI Retrospective Studies — `data-indi/retro`

Curated, ready-to-use subsets of **INDI (International Neuroimaging Data-sharing Initiative)** *retrospective* releases, prepared for the Pittsburgh Fiber Data Hub. This repo consolidates links, essential metadata, licensing, and selected derived artifacts (e.g., QC tables, tractography-ready files) to streamline reuse and replication.

> **Access note:** Many datasets are hosted on external portals or S3. Review each dataset’s license/acknowledgments before use.

---

## Table of contents

* [What’s included](#whats-included)
* [Releases](#releases)

  * [SIMON — Single Individual Volunteer (73 sessions, multi-site)](#simon--single-individual-volunteer-73-sessions-multi-site)
  * [MPI-Leipzig Mind-Brain-Body (LEMON & N&C)](#mpi-leipzig-mind-brain-body-lemon--nc)
  * [Beijing Normal University — Eyes Open / Eyes Closed](#beijing-normal-university--eyes-open--eyes-closed)
  * [Beijing Normal University — Enhanced](#beijing-normal-university--enhanced)
* [How to cite](#how-to-cite)
* [Licensing](#licensing)
* [Known overlaps / deduplication](#known-overlaps--deduplication)
* [Disclaimer](#disclaimer)
* [Contact](#contact)

---

## What’s included

* **Concise release pages** for each dataset (scope, modalities, phenotypes, funding).
* **Pointers to upstream downloads** (NITRC / S3 / project pages).
* When present, **helper assets** (e.g., `participants.tsv`, `qc.tsv`, `*.fz/*.sz` derivatives) to accelerate analysis.

---

## Releases

### SIMON — Single Individual Volunteer (73 sessions, multi-site)

**Dataset:** *SIMON — Single Individual Volunteer for Multiple Observations across Networks*
**Design:** Longitudinal single healthy, ambidextrous male (age 29–46) across **73 sessions**, multiple scanners/sites; partial acquisition under **Canadian Dementia Imaging Protocol (CDIP)**; continuing additions.
**Modalities per session (vary):** T1/T2/PD, T2*, DWI (DTI), resting-state fMRI, susceptibility, ASL.
**Phenotypes:** Age, session number/date (`SIMON_pheno.csv`).
**License:** **CC BY-SA**

**Access (AWS S3 via HTTPS tools):**

* Raw: `s3://fcp-indi/data/Projects/INDI/SIMON/rawdata`
* Preprocessed fMRI: `s3://fcp-indi/data/Projects/INDI/SIMON/derivatives`

**Cyberduck setup:** Protocol **S3**, server `s3.amazonaws.com`, **Anonymous Login**, Path:

```
fcp-indi/data/Projects/INDI/SIMON/rawdata
fcp-indi/data/Projects/INDI/SIMON/derivatives
```

> Wildcards aren’t supported for batch downloads; use exact paths with `curl`/`wget`.

**Contacts & personnel:**
PI: **Simon Duchesne, Ph.D.** (CERVO, Québec).
Senior personnel (abbr.): **A. Badhwar**, **D. Lussier-Levesque**.
Inquiries: `info@medics.ulaval.ca`

**Funding / references (abbr.):**

* Duchesne *et al.*, **CDIP** harmonization, *JMRI* 2019;49:456–465.
* CIMA-Q, CCNA, ONDRI, Alzheimer’s Society of Canada (#13-32), CIHR (#117121), FRQS/Pfizer (#25262, #27239), Ontario Brain Institute, plus support from Cuban Neuroscience Center & UESTC (Tri-national Axis).

**Source:** INDI / project S3 paths (above).

---

### MPI-Leipzig Mind-Brain-Body (LEMON & N&C)

**Dataset:** *MPI-Leipzig Mind-Brain-Body (LEMON; N&C)* — **318 participants**
**Sessions:**

* **LEMON (ses-01):** Structural focus — MP2RAGE (n≈227), T2 (225), DWI 60-dir (228), 15-min eyes-open rs-fMRI (227); updates include 3D FLAIR (SPACE) and in-house SWI enabling **QSM**.
* **Neuroanatomy & Connectivity (N&C, ses-02):** Resting-state focus — four × 15-min eyes-open rs-fMRI (complete for 194; a few with 1–3 runs). Note: multiband bug → **TE 39.4 ms** (vs 30 ms in LEMON).
  **Forty-five** participants have the complete multimodal set (qT1, T2, 3D FLAIR, DWI, SWI/QSM, **75 min** rs-fMRI).
  **Behavior/physiology:** Extensive questionnaires/tasks; rs-EEG; peripheral physiology (ECG/pulse/respiration/BP); BP, anthropometry, hair samples.

**Included assets (when present):**
`mpi-lemon.dti.dz`, `mpi-lemon.gqi.dz`, `participants.tsv`, `qc.tsv`, `sub-*_dwi.*.fz`, `sub-*_dwi.sz`, structural NIfTIs.

**Source:** INDI / project pages (MPI-LEMON/Mind-Brain-Body).

---

### Beijing Normal University — Eyes Open / Eyes Closed

**Dataset:** *BNU — Eyes Open Eyes Closed (EO/EC)* — **48 healthy controls**
**Per participant:**

* **Three** 6-min R-fMRI runs

  * Run 1: **Eyes closed**
  * Runs 2–3: **Randomized** EO vs EC (counterbalanced; details in demographics)
* T1-MPRAGE (defaced), **64-dir DTI (2 mm iso)**
  **License:** **CC BY-NC**
  **Funding acknowledgment:** NSFC **#30770594**; China 863 Program **2008AA02Z405**.
  **Source:** INDI / BNU EO/EC project page.

---

### Beijing Normal University — Enhanced

**Dataset:** *BNU — Enhanced* — **180 healthy controls**
**Imaging:** 8-min R-fMRI; T1-MPRAGE (defaced); **64-dir DTI** for **all**.
**IQ:** WAIS-R **Verbal/Performance/Full IQ** for a **subset (n = 55)**.
**License:** **CC BY-NC**
**Important:** Overlap with **Beijing_Zang** (FCP Classic). **Do not pool** without deduplication.
**References (abbr.):**

* Yan & Zang (2010) DPARSF, *Front Syst Neurosci* 4:13.
* Tian *et al.* (2010) small-world differences, *NeuroImage* 54:191–202.
* Yan *et al.* (2011) DTI tractography networks, *Cereb Cortex* 21(2):449–458.
  **Funding acknowledgment:** NSFC **#30770594**; China 863 **2008AA02Z405**.
  **Source:** INDI / BNU Enhanced project page.

---

## How to cite

Always cite the **original dataset/manuscripts/DOIs** listed above. When using derivatives or helper assets from this repository, add:

> “Processed artifacts and curation were prepared by the Pittsburgh Fiber Data Hub (`data-indi/retro`).”

---

## Licensing

Unless otherwise noted on the upstream pages:

* **SIMON:** **CC BY-SA**
* **BNU EO/EC & BNU Enhanced:** **CC BY-NC**
* **MPI-Leipzig Mind-Brain-Body:** per INDI project page

You may share/adapt under the specified terms. Always verify the license at the source.

---

## Known overlaps / deduplication

* **BNU Enhanced ↔ Beijing_Zang (FCP Classic):** Participant overlap exists. **Deduplicate** before combining.
* **Cross-session/site (SIMON):** Same individual across many scanners—treat sessions as repeated measures; avoid mislabeling as independent subjects.

---

## Disclaimer

* All datasets are provided **as-is** by originating institutions.
* Users are responsible for **quality control**, motion screening, and appropriate preprocessing (e.g., multiband timing, susceptibility/QSM handling, TE differences in N&C).

---

## Contact

For questions about curation or repo-hosted derivatives, open a **GitHub Issue** here.
For access issues or upstream metadata, contact the corresponding **INDI project maintainers** or the SIMON contact (`info@medics.ulaval.ca`).

---

**Repository:** `data-indi/retro` — INDI Retrospective Data Sharing Samples.
