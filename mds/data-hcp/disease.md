# **Human Connectome Project (HCP) — Disease Cohorts**

Preprocessed and derived **diffusion MRI connectomics** resources from Human Connectome Project (HCP)–aligned disease cohorts.  
These datasets provide **derived files only** (e.g., `.fib`, `.gqi.fz`, `.qsdr.fz`) that are ready for tractography and connectome analyses in **DSI Studio** and related tools.

> **NDA note:** Per NDA policy, **raw MRI data are not redistributed here**. After consultation with the NDA program lead, **derived data** (e.g., FIB/FZ) may be shared publicly.  
> For other data types, request access directly through **NDA**. Once you have an approved **Data Use Agreement (DUA)**, contact us and we can provide a link to SRC files where available.

---

## **Overview**

This repository aggregates **HCP-style disease cohorts** processed into DSI Studio–compatible connectomics derivatives.  
Each cohort uses HCP-aligned acquisition and/or processing wherever possible, enabling:

- **Cross-cohort comparisons** with HCP Lifespan and other normative datasets  
- **Disease vs. control connectomics** using compatible pipelines  
- **Tractography, connectometry, and network analyses** without re-doing low-level diffusion preprocessing  

Typical assets include:

- `.gqi.fz` / `.qsdr.fz` tractography-ready volumes  
- Region-wise connectome matrices and metadata (when available)  
- QC tables and basic demographic information (cohort-dependent)  

Raw MRI and detailed clinical data remain under **NDA**, institutional, or project-specific governance.

---

## **Visual Field Loss (VFL)**

**Release tag:** `vfl`  
**Title:** *Changes in Visual Cortical Connectivity Following Central Visual Field Loss*  

Macular degeneration (MD) cohort processed with HCP-compatible pipelines to study **visual cortical plasticity** following central visual field loss.

**Highlights**

- Condition: Age-related macular degeneration (AMD) vs. matched controls  
- Focus: Visual cortical reorganization and peripheral visual field compensation  
- Assets: `.fib` / `.fz` derivatives and related tables  
- License: **CC BY-SA 4.0**  
- Please acknowledge **ACCESS resources: CIS200026 & MED230052**  

### **Download (Linux / macOS — bash)**

```bash
curl -s https://api.github.com/repos/data-hcp/disease/releases/tags/vfl | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
````

### **Download (Windows PowerShell 5.x)**

```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-hcp/disease/releases/tags/vfl").assets | ForEach-Object { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```

---

## **Treatment-Resistant Depression (TRD)**

**Release tag:** `trd`
**Title:** *Perturbation of the Treatment-Resistant Depression (TRD) Connectome by Fast-Acting Therapies*

Longitudinal and cross-sectional TRD cohort with **ECT**, **ketamine**, and **total sleep deprivation** interventions, aligned to HCP normative references.

**Highlights**

* Population: Treatment-Resistant Depression (TRD) + controls
* Interventions: ECT, serial ketamine infusion, total sleep deprivation
* Modalities: Structural MRI, fMRI, dMRI, ASL (pre/post treatments)
* Assets: Derived diffusion/tractography datasets and supporting tables
* License: **CC BY-SA 4.0**
* Please acknowledge **ACCESS CIS200026 & MED230052**
* Investigator: **Katherine Narr**

### **Download (Linux / macOS — bash)**

```bash
curl -s https://api.github.com/repos/data-hcp/disease/releases/tags/trd | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
```

### **Download (Windows PowerShell 5.x)**

```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-hcp/disease/releases/tags/trd").assets | ForEach-Object { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```

---

## **Human Connectome Project for Early Psychosis (EP)**

**Release tag:** `ep`
**Title:** *Human Connectome Project for Early Psychosis*

Early psychosis cohort acquired with **HCP Lifespan Prisma protocols** at Boston and Indianapolis, extending HCP methodology into severe mental illness.

**Highlights**

* Population: Early psychosis (affective and non-affective) + healthy controls
* Sites: Boston & Indianapolis; 3T Prisma scanners
* Modalities: Structural, functional, diffusion MRI; behavioral and clinical data
* Assets: Diffusion-derived FIB/FZ and related metadata
* License: **CC BY-SA 4.0**
* Please acknowledge **ACCESS CIS200026 & MED230052**
* Investigator: **Martha Shenton**

### **Download (Linux / macOS — bash)**

```bash
curl -s https://api.github.com/repos/data-hcp/disease/releases/tags/ep | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
```

### **Download (Windows PowerShell 5.x)**

```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-hcp/disease/releases/tags/ep").assets | ForEach-Object { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```

---

## **Epilepsy Connectome Project (ECP)**

**Release tag:** `ecp`
**Title:** *Epilepsy Connectome Project (ECP)*

Temporal Lobe Epilepsy (TLE) vs. healthy controls, combining multimodal imaging and MEG for large-scale epilepsy connectomics.

**Highlights**

* Population: ~340 adults (200 idiopathic TLE, 140 controls; ages 18–50)
* Modalities: DWI, resting-state and task fMRI, MEG, behavioral and neuropsychological testing
* Goals: Relate seizure burden and network disruption to cognitive and psychosocial outcomes
* Assets: `.gqi.fz`, `.qsdr.fz`, demographic/behavioral tables, data dictionary
* License: **LGPL-3.0**
* Source: [https://osf.io/exbt4/](https://osf.io/exbt4/)

### **Download (Linux / macOS — bash)**

```bash
curl -s https://api.github.com/repos/data-hcp/disease/releases/tags/ecp | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
```

### **Download (Windows PowerShell 5.x)**

```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-hcp/disease/releases/tags/ecp").assets | ForEach-Object { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```

---

## **BANDA: Connectomes Related to Anxiety & Depression**

**Release tag:** `banda`
**Title:** *BANDA: Connectomes Related to Anxiety & Depression*

Boston Adolescent Neuroimaging of Depression and Anxiety (BANDA) project: adolescent cohort targeting RDoC constructs of **acute threat/fear** and **reward/prediction error**.

**Highlights**

* Population: Adolescents 14–16 years with depression and/or anxiety (N≈180) + healthy controls (N≈45)
* Design: Multi-visit protocol with baseline, 6-month online, and 12-month in-person follow-up
* Modalities: HCP-style 3T imaging (T1, T2, dMRI, resting-state and task fMRI), eye-tracking, extensive behavioral and clinical batteries
* Assets: Diffusion derivatives and supporting tables
* License: **CC BY-SA 4.0**
* Study info: [https://humanconnectome.org/study/connectomes-related-anxiety-depression](https://humanconnectome.org/study/connectomes-related-anxiety-depression)

### **Download (Linux / macOS — bash)**

```bash
curl -s https://api.github.com/repos/data-hcp/disease/releases/tags/banda | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
```

### **Download (Windows PowerShell 5.x)**

```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-hcp/disease/releases/tags/banda").assets | ForEach-Object { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```

---

## **Dimensional Connectomics of Anxious Misery (AM)**

**Release tag:** `am`
**Title:** *Dimensional Connectomics of Anxious Misery*

RDoC-inspired cohort focusing on **Negative Valence System (NVS)** constructs, especially **Loss** and **Sustained Threat**, in adults with “anxious misery” syndromes.

**Highlights**

* Population: 200 individuals with anxious misery + 50 healthy controls
* Site: University of Pennsylvania (single 3T Prisma, HCP-aligned protocol)
* Modalities: Structural MRI, dMRI, fMRI, behavioral and neurocognitive batteries, genetic samples
* Follow-up: 1-year longitudinal outcomes
* Assets: HCP-style diffusion derivatives (e.g., `.gqi.fz`, `.qsdr.fz`) and metadata
* License: **CC BY-SA 4.0**
* Please acknowledge **ACCESS CIS200026 & MED230052**

### **Download (Linux / macOS — bash)**

```bash
curl -s https://api.github.com/repos/data-hcp/disease/releases/tags/am | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
```

### **Download (Windows PowerShell 5.x)**

```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-hcp/disease/releases/tags/am").assets | ForEach-Object { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```

---

## **Licenses**

Licensing follows each cohort’s original terms:

* **VFL / TRD / EP / BANDA / AM**

  * Derived files here are shared under **Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)**.
  * For VFL, TRD, EP, and AM, please acknowledge supercomputing resources **ACCESS CIS200026 & MED230052**.

* **ECP**

  * Shared under **GNU Lesser General Public License (LGPL-3.0)**.
  * Original project page: [https://osf.io/exbt4/](https://osf.io/exbt4/)

Each dataset directory includes license notes and, when applicable, links back to the original project pages.

---

## **Citations**

When using these datasets:

1. Cite the **original disease cohort publications** (VFL, TRD, EP, ECP, BANDA, AM) and their DOIs.
2. Cite **HCP**, **ACCESS**, and supercomputing allocations **CIS200026, MED230052** where applicable.
3. If you use derivatives from this repository, please add:

> “Derived diffusion MRI datasets were prepared by the Pittsburgh Fiber Data Hub (`data-hcp/disease`).”

Check individual dataset documentation for any additional citation or acknowledgment requirements.

---

## **Disclaimer**

* This repository **does not** redistribute raw MRI or identifiable clinical data.
* Users must comply with **NDA**, **IRB**, and source project data-use agreements.
* Derived connectomics products are provided to accelerate research but should undergo independent **quality control, validation, and methodological checks** before publication or clinical interpretation.

