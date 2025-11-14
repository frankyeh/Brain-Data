# NIMH Data Archive (NDA) Neuroimaging Collections

This repository hosts **derived neuroimaging data (.fz/.dz)** from multiple projects in the **National Institute of Mental Health Data Archive (NDA)**, spanning prenatal development, infancy, childhood/adolescence, and adult psychiatric disorders. All datasets here are **derived files only**; access to raw or restricted-level images and phenotypes requires an approved **Data Use Agreement (DUA)** from NDA.

Derived files in this repository follow a **CC BY-NC-SA** license. Underlying data remain governed by NDA policies and each project’s original terms.

For each collection below:

- `nda-XXXX.gqi.dz` / `nda-XXXX.dti.dz`: group-level diffusion derivatives  
- `*.fz`: subject-level tractography-ready files  
- `qc.tsv`: basic quality control metrics  

---

## Early Brain Development in Twins (Collection ID: 1974)

Twin designs are critical for teasing apart **genetic vs. environmental** influences on early brain development and risk for neurodevelopmental and psychiatric disorders. This project focuses on the **neonatal period**, which has historically been under-sampled in twin imaging work.

**Design & current findings**

- >100 twin pairs with **prenatal ultrasound** and **neonatal MRI**  
- Prenatal brain size discordance is similar in monozygotic (MZ) and dizygotic (DZ) twins  
- By ~1 month of age, MZ twins show **smaller discordance** in total brain volume than DZ twins  
- Global tissue volumes in neonates are **highly heritable**, matching findings in older samples  
- Gray matter heritability is slightly lower at birth, with density correlations dropping across the first year of life  
- White matter **volumes** show strong heritability, but **DTI metrics of specific tracts** are much less heritable

**Next phase**

- Expand the twin cohort and follow children to **age 6** with:
  - Structural MRI  
  - DTI  
  - Developmental assessments  
- Aim: clarify how genes and environment jointly shape early brain organization and early psychiatric risk.

**Investigator:** John Gilmore (UNC Chapel Hill)  
**Assets in this repo:** 459  

**Download (Linux/macOS — bash)**  
```bash
curl -s https://api.github.com/repos/data-nih/nda/releases/tags/nda-1974 | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
````

**Download (Windows PowerShell 5.x)**

```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-nih/nda/releases/tags/nda-1974").assets | % { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```

---

## Longitudinal MRI Study of Infants at Risk for Autism (IBIS; Collection ID: 19)

This dataset comes from the **IBIS Autism Project**, part of the **Autism Centers of Excellence (ACE)** Network, with collaboration across UNC, UW, WU, Yale, and the MNI DCC.

**Design**

* **High-risk infants:** younger siblings of children with ASD
* Longitudinal **MRI/DTI + behavioral assessments** at:

  * 6 months
  * 12 months
  * 24 months
* Multi-site, harmonized protocols across ACE sites

**Goals**

* Characterize how early brain structure and connectivity develop in infants at **elevated genetic risk for ASD**
* Seek early **biomarkers of autism**, supporting earlier detection and intervention
* Link trajectories of structural/white matter development to emerging behavioral phenotypes

**Investigator:** Joe Piven (UNC Chapel Hill)
**Assets in this repo:** 871

**Download (Linux/macOS — bash)**

```bash
curl -s https://api.github.com/repos/data-nih/nda/releases/tags/nda-19 | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
```

**Download (Windows PowerShell 5.x)**

```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-nih/nda/releases/tags/nda-19").assets | % { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```

---

## Fetal Programming of the Newborn and Infant Human Brain (Collection ID: 1890)

A **prospective, longitudinal** follow-up of children whose mothers participated in an NIH pregnancy study focused on biological and behavioral processes.

**Design & focus**

* Population-based cohort followed from **intrauterine life through birth and infancy**
* Serial **maternal–placental–fetal endocrine** and **immune/inflammatory** measures during pregnancy
* Newborn and infant brain imaging linked to these prenatal exposures

**Goals**

* Determine how **prenatal environmental factors** (hormonal, immune, inflammatory) shape early brain development
* Elucidate pathways from **prenatal exposures** to later **neurodevelopmental and psychiatric outcomes**

**Investigators:** Claudia Buss, Pathik D. Wadhwa (UC Irvine)
**Assets in this repo:** 87

**Download (Linux/macOS — bash)**

```bash
curl -s https://api.github.com/repos/data-nih/nda/releases/tags/nda-1890 | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
```

**Download (Windows PowerShell 5.x)**

```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-nih/nda/releases/tags/nda-1890").assets | % { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```

---

## Longitudinal Neuroimaging and Neurocognitive Assessment Across the Schizophrenia Spectrum (Collection ID: 3445)

This study uses **Schizotypal Personality Disorder (SPD)** as an intermediate SZ-spectrum phenotype to understand **risk and protective factors** across the schizophrenia spectrum, without the confounds of chronic antipsychotic treatment or hospitalization.

**Participants (18–40 yrs)**

* 80 Healthy Controls (no Axis I or personality disorders)
* 80 SPD (unmedicated, no Axis I disorders)
* 80 early-onset SZ (first 2 years of illness)
* Timepoints: **baseline, 9-month, 18-month**

**Multimodal imaging**

* Structural MRI
* DTI
* Resting-state fMRI
* Task fMRI (nonverbal working memory at baseline and 18 months)

**Assessments & analysis**

* Neurocognitive and clinical assessments at all timepoints
* **Dynamic causal modeling (DCM)** for frontotemporal circuitry
* **Machine learning** to integrate multimodal imaging + cognition + clinical features

**Objectives**

* Map trajectories of **frontotemporal abnormalities** across SZ-spectrum groups
* Track longitudinal evolution of cognition, symptoms, and functioning
* Identify combinations of neural and behavioral factors that confer **risk vs. resilience**

**Investigator:** Erin Hazlett (Icahn School of Medicine at Mount Sinai)
**Assets in this repo:** 211

**Download (Linux/macOS — bash)**

```bash
curl -s https://api.github.com/repos/data-nih/nda/releases/tags/nda-3445 | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
```

**Download (Windows PowerShell 5.x)**

```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-nih/nda/releases/tags/nda-3445").assets | % { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```

---

## Mechanisms Underlying Resilience to Neighborhood Disadvantage (Collection ID: 2818)

Not all youth in **disadvantaged neighborhoods** develop psychopathology. This project focuses on those who show **adaptive competence**, aiming to uncover multilevel pathways that promote resilience.

**Participants**

* 500 adolescent twin pairs (ages 11–16)
* Previously assessed at ages 6–10
* All from modestly-to-severely disadvantaged neighborhoods

**Imaging & constructs**

* Structural MRI
* DTI
* Resting-state and task-based fMRI
* Focus on:

  * **Resilience** (good adaptation, minimal psychopathology)
  * **Protective processes** (family and community supports)

**Goals**

* Identify neural markers and **synergistic networks** associated with resilience
* Use genetically informed (twin) design to dissect **genetic, epigenetic, and environmental** influences
* Test how **positive parenting and community resources** support normative brain architecture under adversity

**Investigator:** S. Burt (Michigan State University)
**Assets in this repo:** 564

**Download (Linux/macOS — bash)**

```bash
curl -s https://api.github.com/repos/data-nih/nda/releases/tags/nda-2818 | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
```

**Download (Windows PowerShell 5.x)**

```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-nih/nda/releases/tags/nda-2818").assets | % { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```

---

## Integration of Neural Networks and Attachment in Human Infants (Collection ID: 2690)

This project links **maternal caregiving**, **attachment security**, and **early brain network development**.

**Longitudinal design**

* Infant scans at **3 and 12 months** during natural sleep:

  * Resting-state fMRI
  * DTI
* Mother–infant interactions at **3, 6, and 9 months**, including:

  * Structured lab tasks
  * Automated naturalistic home-environment capture
* Attachment at **12 months** via the **Strange Situation Procedure**

**Network analysis**

* Intra- and inter-network connectivity
* Dynamic, whole-brain, data-driven analytic approaches

**Goals**

* Trace how caregiving and infant behavior shape evolving brain networks
* Understand pathways from early caregiving to socio-emotional and neural outcomes
* Identify targets for early intervention promoting healthy attachment and network integration

**Investigator:** Nancy McElwain (University of Illinois at Urbana–Champaign)
**Assets in this repo:** 111

**Download (Linux/macOS — bash)**

```bash
curl -s https://api.github.com/repos/data-nih/nda/releases/tags/nda-2690 | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
```

**Download (Windows PowerShell 5.x)**

```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-nih/nda/releases/tags/nda-2690").assets | % { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```

---

## Cincinnati MR Imaging of Neurodevelopment (C-MIND; Collection ID: 2329)

Part of the **Pediatric Functional Neuroimaging Research Network**, led by Cincinnati Children’s Hospital Medical Center with partners at LONI (USC), UCLA, Children’s Hospital of Pittsburgh, and the University of Michigan.

**Aims**

* Standardize recruitment, scanning, and processing protocols across pediatric sites
* Characterize brain development from **infancy through adolescence**

**Imaging**

* 3D T1- and T2-weighted anatomical scans
* BOLD-fMRI
* DTI
* ASL perfusion
* A **concurrent ASL/BOLD-fMRI** dataset for neurovascular coupling

**Cohort**

* > 200 typically developing children (cross-sectional)
* Longitudinal subsets:

  * ~40 infants/toddlers (0–3 years)
  * ~30 children (7–9 years)

**Focus**

* Maturation of **white/gray matter**, structural/functional connectivity
* Neurovascular coupling and its relationship to cognition and behavior

**Investigators:** Scott Holland, Jennifer Vannest (CCHMC)
**Assets in this repo:** 567

**Download (Linux/macOS — bash)**

```bash
curl -s https://api.github.com/repos/data-nih/nda/releases/tags/nda-2329 | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
```

**Download (Windows PowerShell 5.x)**

```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-nih/nda/releases/tags/nda-2329").assets | % { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```

---

## Integrity and Dynamic Processing Efficiency of Networks in ASD (Collection ID: 2285)

This study integrates **fcMRI**, **DTI**, and **MEG** to understand network-level abnormalities in **Autism Spectrum Disorders (ASD)**.

**Participants**

* 60 adolescents with ASD
* 60 matched typically developing controls

**Methods**

* **fMRI** during lexical-semantic decision to define nodes in a VLSEM circuit:

  * Visual, Lexico-Semantic, Executive, Motor components
* **DTI** to measure structural connections among VLSEM nodes
* **MEG** to examine temporal dynamics and processing efficiency

**Goals**

* Identify and characterize the VLSEM network in ASD
* Combine structural, functional, and dynamic measures to map how circuit-level disruptions relate to cognitive and socio-communicative impairments

**Investigator:** Ralph-Axel Mueller (San Diego State University)
**Assets in this repo:** 145

**Download (Linux/macOS — bash)**

```bash
curl -s https://api.github.com/repos/data-nih/nda/releases/tags/nda-2285 | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
```

**Download (Windows PowerShell 5.x)**

```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-nih/nda/releases/tags/nda-2285").assets | % { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```

---

## Taste Reward Circuits and Prediction Error in Eating Disorders (Collection ID: 2138)

An RDoC-inspired study of **anorexia nervosa (AN)** and **bulimia nervosa (BN)** using **Prediction Error** as the organizing construct.

**Participants**

* Adolescents and young adults (16–29 years), at high risk for severe ED outcomes

**Aims**

1. **Functional reward circuits (fMRI)**

   * Taste-reward prediction error responses in:

     * Anteroventral striatum
     * Insula
     * Anterior cingulate cortex (ACC)
   * Hypothesis: lower BMI associates with heightened ACC responses to reward-predicting cues.
2. **Structural MRI & DTI**

   * Quantify gray/white matter volumes and white matter integrity
   * Hypothesis: severe ED behaviors relate to reduced caudate/insula volumes and altered connectivity.
3. **RDoC-based clustering**

   * Cluster individuals by prediction-error signatures, comparing to DSM categories
   * Hypothesis: prediction-error profiles better organize ED-relevant behaviors than diagnoses alone.

**Investigator:** Joel Stoddard (University of Colorado)
**Assets in this repo:** 67

**Download (Linux/macOS — bash)**

```bash
curl -s https://api.github.com/repos/data-nih/nda/releases/tags/nda-2138 | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
```

**Download (Windows PowerShell 5.x)**

```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-nih/nda/releases/tags/nda-2138").assets | % { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```

---

## Effects of Poverty on Affective Development (Collection ID: 2106)

A multi-level, longitudinal study of how **poverty-related stress** becomes biologically embedded and increases risk for anxiety and depression.

**Sample**

* Teens drawn from the **Fragile Families and Child Wellbeing Study (FFCWS)**
* Rich developmental data from birth to age 15, with follow-up at age 17
* Predominantly low-income families

**Assessments at age 15**

* **fMRI**: emotional faces tasks targeting amygdala–vmPFC circuitry
* **DTI**: structural connectivity
* **HPA axis**: cortisol and DHEA responses to stress
* Cognitive/behavioral tasks (attention bias, etc.)
* Self- and parent-report measures of negative affect, anxiety, and depression

**Goals**

* Understand how chronic exposure to danger, conflict, instability, and neglect alters:

  * HPA axis regulation
  * Amygdala reactivity and prefrontal regulation
* Map pathways from poverty to affective psychopathology, using the rich FFCWS context.

**Investigator:** Christopher Monk (University of Michigan)
**Assets in this repo:** 385

**Download (Linux/macOS — bash)**

```bash
curl -s https://api.github.com/repos/data-nih/nda/releases/tags/nda-2106 | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
```

**Download (Windows PowerShell 5.x)**

```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-nih/nda/releases/tags/nda-2106").assets | % { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```

---

## Multidimensional Investigation of Cognitive Control Deficits in Psychopathology (Collection ID: 2102)

This project investigates **psychotic spectrum disorders (PSD)**—schizophrenia, schizoaffective disorder, bipolar disorder with psychotic features—through the lens of **cognitive control** impairments, which strongly predict real-world functioning yet remain hard to treat.

**Participants**

* ~175 PSD patients, continuously recruited

**Data**

* Extensive clinical and cognitive batteries
* Multimodal neuroimaging:

  * Task and resting-state fMRI
  * DTI for white matter integrity/connectivity
* Cognitive control tasks with strong ecological relevance

**Analysis & goals**

* Derive **neurophysiologically based cluster metrics** indexing circuit-level pathology in the cognitive control network (dmPFC, lateral PFC, caudate)
* Use **k-means clustering** and cross-validation to define biologically meaningful PSD subgroups
* Examine relationships between:

  * Neurophysiological profiles
  * Genetic variation (SNPs, CNVs in dopamine, glutamate, GABA, synaptic pathways)
  * Cognitive control and functional outcomes

**Investigator:** Andrew Robert Mayer (Mind Research Network)
**Assets in this repo:** 183

**Download (Linux/macOS — bash)**

```bash
curl -s https://api.github.com/repos/data-nih/nda/releases/tags/nda-2102 | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
```

**Download (Windows PowerShell 5.x)**

```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-nih/nda/releases/tags/nda-2102").assets | % { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```

---

## 2/3 – Social Processes Initiative in Neurobiology of the Schizophrenia(s) (Collection ID: 2098)

An RDoC-driven project targeting **social cognitive (SCog) impairments** across **Schizophrenia Spectrum Disorders (SSDs)**, from healthy controls through full illness.

**Approach**

* Structural MRI to examine gray matter morphology and network topology
* DTI to map white matter circuits supporting SCog processes
* Resting and task-based fMRI to measure circuit function
* **Partial Least Squares (PLS)** and other multivariate tools to relate brain structure, function, and behavior

**Goals**

* Characterize **abnormal brain–behavior relationships** in SCog domains across the SZ spectrum
* Build an RDoC-aligned matrix mapping SCog constructs from normal variation to severe impairment
* Identify neural circuitry that could be targeted to improve social functioning in SSDs

**Investigators:** Anil K. Malhotra, Aristotle Voineskos, Robert W. Buchanan
**Organization:** The Feinstein Institute for Medical Research
**Assets in this repo:** 899

**Download (Linux/macOS — bash)**

```bash
curl -s https://api.github.com/repos/data-nih/nda/releases/tags/nda-2098 | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
```

**Download (Windows PowerShell 5.x)**

```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-nih/nda/releases/tags/nda-2098").assets | % { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```

---

## Multimodal Developmental Neurogenetics of Females with ASD (Collection ID: 2021)

A deep, multimodal investigation of **sex differences in ASD**, addressing the male–female prevalence gap with a **sex-balanced cohort**.

**Cohort**

* 125 ASD participants
* 125 typically developing controls
* Unaffected siblings
* Parental genotyping for family-based analyses

**Data types**

* Behavioral phenotyping across multiple domains
* Brain imaging:

  * Structural MRI
  * DTI
  * Task and resting-state fMRI
  * EEG
* Genetics:

  * CNV
  * SNV

**Goals**

* Identify **sex-specific** differences in brain structure, function, connectivity, and timing
* Relate CNVs/SNVs to brain phenotypes in ASD vs. TD groups
* Use network-based approaches (e.g., iWGCNA) to integrate brain, behavior, and genetics, addressing ASD heterogeneity

**Investigator:** Kevin Pelphrey (University of Virginia)
**Assets in this repo:** 243

**Download (Linux/macOS — bash)**

```bash
curl -s https://api.github.com/repos/data-nih/nda/releases/tags/nda-2021 | jq -r '.assets[].browser_download_url' | xargs -n1 -P4 curl -LO
```

**Download (Windows PowerShell 5.x)**

```powershell
(Invoke-RestMethod "https://api.github.com/repos/data-nih/nda/releases/tags/nda-2021").assets | % { Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf) }
```

---

## Data Access and Licensing Notes

For all collections in `data-nih/nda`:

* **`.fz`/`.dz` files** are shared under **Creative Commons Attribution–NonCommercial–ShareAlike (CC BY-NC-SA)**.
* Access to **`.sz` files and structural images** requires a **Data Use Agreement (DUA)** approved by the **NDA Data Use Permission Group**. These must be requested directly through the **NIMH Data Archive**.
* When publishing work that uses these derivatives, please:

  * Cite the **original NDA Collection** and its primary publications
  * Acknowledge the **NIMH Data Archive (NDA)**
  * Optionally add:

    > “Derived imaging files were curated via the Pittsburgh Fiber Data Hub (`data-nih/nda`).”

---

© 2025 LabSolver / Pittsburgh Fiber Data Hub.
Source datasets © respective investigators and the National Institute of Mental Health Data Archive (NDA).
All `.fz` outputs in this repository follow **CC BY-NC-SA**, and use of underlying NDA data must follow NDA policies and DUAs.

