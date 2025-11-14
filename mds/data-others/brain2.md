# Brain MRI Collections (after 2020)

Curated external **human brain diffusion MRI datasets** released after ~2020, sourced from public archives (e.g., Dryad, Zenodo, ScienceDB).  
Datasets are provided **as-is** and intended for:

- Research and method development  
- Tractography benchmarking  
- Diffusion modeling (DTI, HARDI, NODDI, SMT/SANDI)  
- Test–retest studies  
- Educational use  

All datasets retain their original **license**, **citation**, and **usage terms** required by data owners.  
Always cite the original dataset DOIs.

---

## Releases in This Repository

---

### 1) Ex vivo Mesoscale Human Temporal Lobe Dataset (`pitt-hippo`)

Mesoscale ex vivo diffusion MRI of the human **temporal lobe**, emphasizing hippocampal lamellar and fimbria pathways.

**Download command**
```bash
curl -s https://api.github.com/repos/data-hcp/brain-after-2020/releases/tags/pitt-hippo | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
```
```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-hcp/brain-after-2020/releases/tags/pitt-hippo").assets | ForEach-Object { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```

**Summary:**
Ex vivo dMRI at 250 µm isotropic (upsampled to 125 µm). Reconstruction using GQI. Includes hippocampal subfields (CA1–3, DG), head–body–tail regions, fimbria ROIs, and 50+ dissected pathway templates.

**License:** Public domain (Dryad)  
**DOI:** https://doi.org/10.5061/dryad.jh9w0vtnq

---

### 2) Brain and Spinal Cord Multi-Shell Diffusion MRI (`vu-brain-cord`)

Integrated **brain + cervical spinal cord** multi-shell dMRI for 11 subjects (6 with test–retest), fully BIDS-compliant.

**Download command**
```bash
curl -s https://api.github.com/repos/data-hcp/brain-after-2020/releases/tags/vu-brain-cord | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
```
```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-hcp/brain-after-2020/releases/tags/vu-brain-cord").assets | ForEach-Object { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```

Derived datasets include NODDI, SMT, SANDI, and DTI model fits, segmentations, FreeSurfer reconstructions, reverse-PE scans, and BIDS metadata.

**License:** CC BY 4.0  
**DOI:** https://doi.org/10.5281/zenodo.15512428

---

### 3) EDEN2020 Human Brain MRI Datasets (`vssru-eden2020`)

High-resolution multimodal MRI (T1, FLAIR, SWI, DTI, NODDI) from 15 healthy adults, collected to support neurosurgical imaging research.

**Download command**
```bash
curl -s https://api.github.com/repos/data-hcp/brain-after-2020/releases/tags/vssru-eden2020 | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
```
```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-hcp/brain-after-2020/releases/tags/vssru-eden2020").assets | ForEach-Object { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```

Includes angiographic, HARDI, and white matter microstructure imaging; derived DTI/NODDI maps; probabilistic tractography.

**License:** CC BY-NC-ND 4.0  
**DOI:** https://doi.org/10.5281/zenodo.3994749

---

### 4) Structural & Functional Basis of Neuronal Plasticity — Healthy Controls (`vitality`)

Multimodal MRI for studying **CBF, CMRO₂, DWI, task-induced plasticity**, and metabolic responses.

**Download command**
```bash
curl -s https://api.github.com/repos/data-hcp/brain-after-2020/releases/tags/vitality | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
```
```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-hcp/brain-after-2020/releases/tags/vitality").assets | ForEach-Object { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```

Includes MP2RAGE, pCASL DEXI perfusion scans, two DWIs, TRUST/IR-EPI metabolic sequences, task behavioral traces.

**License:** CC BY 4.0  
**Source:** https://zenodo.org/records/15149088

---

### 5) In Vivo Whole-Brain Connectom dMRI at 760 µm (`mgh-760`)

Ultra-high-resolution Connectom dMRI with **1260 directions**, 18 hours of acquisition.

**Download command**
```bash
curl -s https://api.github.com/repos/data-hcp/brain-after-2020/releases/tags/mgh-760 | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
```
```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-hcp/brain-after-2020/releases/tags/mgh-760").assets | ForEach-Object { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```

Includes submillimeter structural MRI, field maps, acquisition logs, and preprocessing scripts.

**License:** CC0  
**DOI:** https://doi.org/10.5061/dryad.rjdfn2z8g

---

### 6) Imaging Chinese Young Brains – CHIMGEN Subset (`icyb`)

Large-sample multimodal dataset of **215 young Chinese adults** with T1, rs-fMRI, DTI, and ASL.

**Download command**
```bash
curl -s https://api.github.com/repos/data-hcp/brain-after-2020/releases/tags/icyb | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
```
```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-hcp/brain-after-2020/releases/tags/icyb").assets | ForEach-Object { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```

Includes BIDS-structured data with defaced anatomical scans and MRI-QC reports.

**License:** CC BY 4.0  
**DOI:** https://doi.org/10.11922/sciencedb.00740

---

### 7) Functional & Structural MRI After tSMS Stimulation (`cinac-tsms`)

Double-blind crossover experiment comparing **real vs sham tSMS** over right M1.

**Download command**
```bash
curl -s https://api.github.com/repos/data-hcp/brain-after-2020/releases/tags/cinac-tsms | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
```
```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-hcp/brain-after-2020/releases/tags/cinac-tsms").assets | ForEach-Object { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```

Includes multiecho resting-state fMRI, DWI, corrected phase images, and defaced anatomy.

**License:** CC BY 4.0  
**DOI:** https://doi.org/10.5281/zenodo.15224957

---

### 8) B-Q Minded Test–Retest Cross-Scanner Dataset (`bqminded`)

Test–retest dataset for **cross-scanner qMRI and diffusion harmonization** (Skyra 3T vs PrismaFit 3T).

**Download command**
```bash
curl -s https://api.github.com/repos/data-hcp/brain-after-2020/releases/tags/bqminded | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
```
```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-hcp/brain-after-2020/releases/tags/bqminded").assets | ForEach-Object { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```

Used in recent harmonization studies (NeuroCombat, LongCombat). Includes anatomical and diffusion MRI.

**License:** CC BY 4.0  
**DOI:** https://doi.org/10.5281/zenodo.6473268

---

## Licensing & Attribution

Each dataset retains its **original license**. Use must comply with:

* CC0 / CC BY
* CC BY-NC / CC BY-NC-ND
* Dataset-specific restrictions

Cite:

1. The dataset DOI
2. The primary research article (if applicable)
3. Optionally:  
   *“Data access facilitated by the `data-hcp/brain-after-2020` repository.”*

---

## Intended Use

* Diffusion modeling (DTI, HARDI, NODDI, SMT/SANDI)
* High-resolution tractography
* Test–retest analyses
* Cross-scanner harmonization
* Educational teaching sets for MRI & connectomics

---

## Notes

* Some datasets include partial acquisitions or subject-specific issues; see their notes.
* Derived files (FIB, SRC, microstructural maps) reflect specific pipelines.
* Some datasets include only derivatives, not original raw DICOM/NIfTI.
