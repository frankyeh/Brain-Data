# Disease dMRI Collections

Curated **disease-focused MRI datasets** (structural & diffusion) for research, benchmarking, and education.
Each release retains its **original license**, **citation**, and **metadata**.
Please **cite the source** when using any dataset.

---

## Included Releases

---

### 1) Alzheimer’s vs Bipolar vs Healthy Controls (`ubc-ad_bd`)

Structural & diffusion MRI with **derived FA, TBSS, VBM** and **clinical CSVs**.

**Download (Linux/macOS)**

```bash
curl -s https://api.github.com/repos/data-hcp/disease/releases/tags/ubc-ad_bd | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
```

**Download (Windows PowerShell)**

```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-hcp/disease/releases/tags/ubc-ad_bd").assets | ForEach-Object { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```

* **Scope:** AD, BD, and healthy controls (anonymized)
* **Analyses:** FSL (DTI/TBSS), SPM (VBM); registration to MNI
* **License:** **CC BY 4.0**
* **Citation/DOI:** Besga, Graña, Chyzhyk (2020). Zenodo. [https://doi.org/10.5281/zenodo.3935636](https://doi.org/10.5281/zenodo.3935636)
* **Use cases:** AD vs BD discrimination, biomarker correlation, CAD modeling

---

### 2) High-Quality DWI of Parkinson’s Disease (`liege-pd`)

Cross-sectional PD dataset with **120 dirs**, **b=1000/2500**, **2.4 mm³** voxels; matched controls.

**Download (Linux/macOS)**

```bash
curl -s https://api.github.com/repos/data-hcp/disease/releases/tags/liege-pd | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
```

**Download (Windows PowerShell)**

```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-hcp/disease/releases/tags/liege-pd").assets | ForEach-Object { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```

* **N:** 27 PD, 26 controls
* **Sequence:** Twice-refocused spin-echo
* **License:** **CC BY-SA**
* **Source:** NITRC “parktdi” (linked in release)
* **Use cases:** PD microstructure, group comparisons, denoising/EDDY benchmarks

---

### 3) Inter-Site Reproducibility in Small Vessel Disease (`isd-svd`)

**CADASIL** patients scanned on **Prisma & Skyra** within 24 hours, BIDS-structured.

**Download (Linux/macOS)**

```bash
curl -s https://api.github.com/repos/data-hcp/disease/releases/tags/isd-svd | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
```

**Download (Windows PowerShell)**

```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-hcp/disease/releases/tags/isd-svd").assets | ForEach-Object { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```

* **N:** 10 CADASIL patients
* **Preproc:** dwidenoise, mrdegibbs, TOPUP, EDDY
* **License:** **CC BY-NC 4.0**
* **Citation/DOI:** [https://doi.org/10.5281/zenodo.16925507](https://doi.org/10.5281/zenodo.16925507)
* **Paper:** Neurology (2020)
* **Use cases:** Harmonization (ComBat/LongCombat), artifact studies, SVD biomarkers

---

## Licensing & Citation

* **ubc-ad_bd:** CC BY 4.0 — cite Besga et al., Zenodo (2020)
* **liege-pd:** CC BY-SA — cite NITRC source
* **isd-svd:** CC BY-NC 4.0 — cite Dewenter et al., Zenodo (2020) & Neurology (2020)

You **must** follow dataset licenses and **cite the original investigators**.

---

## Notes

* Some releases include **preprocessed and raw** data
* CC BY-NC datasets may impose **non-commercial restrictions**
* Defacing/anonymization methods differ—check for your application
