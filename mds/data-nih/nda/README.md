# **NIMH Data Archive (NDA) Neuroimaging Collections**

This repository hosts **derived neuroimaging data (.fz/.dz)** from multiple projects in the **National Institute of Mental Health Data Archive (NDA)**, focused on brain development and psychiatric risk across the lifespan. The NDA aggregates de-identified human subjects data from hundreds of studies, harmonized to common data standards and made available for qualified researchers. Summary-level information is accessible to all, while individual-level images and phenotypes typically require an approved **Data Use Agreement (DUA)**.

Here, we provide diffusion/tractography-ready derivatives and quality control files for selected NDA collections, together with brief project descriptions and pointers to original NDA resources. These datasets span **prenatal development**, **infancy**, **childhood and adolescence**, and **adult psychiatric spectrum disorders**, enabling cross-study analyses of brain structure, connectivity, and behavior.

---

## Overview of NDA

- **Archive:** National Institute of Mental Health Data Archive (NDA)  
- **Scope:** Human subjects data (imaging, genetics, behavior, clinical) across many domains  
- **Mission:** Accelerate discovery through data sharing, harmonization, and reporting of results  
- **Access:**
  - **Harmonized de-identified data:** via NDA with approved DUA  
  - **Summary data:** publicly available  

**NIMH Common Data Elements** are available through NDA to promote interoperability across projects.

---

## Data Access and Licensing (This Repository)

For the collections mirrored in this repository:

- **`.fz` files** (derived diffusion/tractography outputs)  
  - Shared under **Creative Commons Attribution–NonCommercial–ShareAlike (CC BY-NC-SA)**.  
- **`.sz` files and structural images**  
  - Access requires a **Data Use Agreement (DUA)** approved by the **NDA Data Use Permission Group**.  
  - These data must be requested directly through the **NIMH Data Archive**.

Each release in `data-nih/nda` corresponds to an NDA **Collection ID** and includes:
- Processed diffusion outputs (`*.fz`, `*.dz`)  
- Basic QC tables (`qc.tsv`)  
- Project-specific notes as needed  

---

## Collections Included

### Early Brain Development in Twins (Collection ID: 1974)

Twin studies are key for disentangling **genetic vs. environmental** influences on brain development. This project focuses on **early brain development** in twins, a period previously understudied.

**Design and Findings:**
- >100 twin pairs with **prenatal ultrasound** and **neonatal MRI**.  
- **Prenatal brain size discordance** is similar in monozygotic (MZ) and dizygotic (DZ) twins.  
- By **1 month**, MZ twins show *less* discordance in brain volume than DZ twins.  
- **Global tissue volumes** in neonates are **highly heritable**, consistent with older age groups.  
- **Gray matter heritability** is slightly lower in neonates; gray matter density correlations decrease during the first year of life, likely reflecting rapid growth.  
- **White matter volumes** are highly heritable, but **DTI metrics of specific tracts** are *not* strongly heritable.

**Planned Follow-up:**
- Expansion of the twin cohort and follow-up to **age 6** with:
  - Structural MRI  
  - DTI  
  - Developmental assessments  

**Goal:** Clarify how genes and environment shape early brain development and early risk for psychiatric disorders.

- **Investigator:** John Gilmore  
- **Institution:** University of North Carolina at Chapel Hill  
- **Assets in this repo:** 459  

---

### Longitudinal MRI Study of Infants at Risk for Autism (Collection ID: 19)

This dataset comes from the **IBIS Autism Project**, part of the **Autism Centers of Excellence (ACE)** Network, coordinated across: UNC, UW, WU, Yale, and the DCC at MNI.

**Design:**
- **Longitudinal MRI/DTI + behavioral assessments** at:
  - 6 months  
  - 12 months  
  - 24 months  
- **High-risk infants:** younger siblings of children with ASD.

**Goals:**
- Characterize how **early brain development** differs in infants at increased genetic risk for **ASD**.  
- Track **structural** and **connectivity** changes in the first two years of life.  
- Support identification of **biomarkers** for early detection and targets for early intervention.

- **Investigator:** Joe Piven  
- **Institution:** University of North Carolina at Chapel Hill  
- **Assets in this repo:** 871  

---

### Fetal Programming of the Newborn and Infant Human Brain (Collection ID: 1890)

This project follows a **population-based cohort** of children born to mothers in an NIH-funded pregnancy study, focusing on **prenatal biological and behavioral processes**.

**Design and Focus:**
- Prospective, longitudinal study from **intrauterine life through birth and infancy**.  
- **Prenatal measures** include:
  - Maternal–placental–fetal **endocrine** markers  
  - **Immune/inflammatory** measures  
- These data are linked to newborn and infant brain development.

**Goals:**
- Determine how **prenatal environmental factors** influence early brain development.  
- Understand biological pathways from **prenatal exposure** to later **neurodevelopmental and psychiatric outcomes**.

- **Investigators:** Claudia Buss, Pathik D. Wadhwa  
- **Institution:** University of California, Irvine  
- **Assets in this repo:** 87  

---

### Longitudinal Neuroimaging and Neurocognitive Assessment Across the Schizophrenia Spectrum (Collection ID: 3445)

This study examines **risk and protective factors** across the schizophrenia spectrum, focusing on **Schizotypal Personality Disorder (SPD)** as an intermediate phenotype between healthy controls and schizophrenia (SZ).

**Participants (18–40 yrs):**
- 80 healthy controls (HC)  
- 80 SPD (unmedicated, no Axis I disorders)  
- 80 early-onset SZ (first 2 years of illness)  

**Design:**
- Timepoints: Baseline, 9-month, and 18-month follow-up.  
- **Imaging:**
  - Structural MRI  
  - DTI  
  - Resting-state fMRI  
  - Task fMRI (nonverbal working memory, baseline and 18 months)  
- **Assessments:** Neurocognitive and clinical at all timepoints.

**Analysis Methods:**
- Dynamic causal modeling (DCM) of **frontotemporal connectivity**.  
- Machine learning to integrate multimodal imaging, cognition, and clinical data.

**Objectives:**
- Map trajectories of **frontotemporal circuitry abnormalities**.  
- Track **neurocognitive and functional outcomes**.  
- Identify **risk vs. protective factors** across the SZ spectrum.

- **Investigator:** Erin Hazlett  
- **Institution:** Icahn School of Medicine at Mount Sinai  
- **Assets in this repo:** 211  

---

### Mechanisms Underlying Resilience to Neighborhood Disadvantage (Collection ID: 2818)

This project investigates how some children maintain **adaptive competence** despite growing up in **disadvantaged neighborhoods**.

**Participants:**
- 500 adolescent twin pairs (ages 11–16)  
- Previously assessed at ages 6–10  
- All from modestly-to-severely disadvantaged neighborhoods  

**Imaging:**
- Structural MRI  
- DTI  
- Resting-state fMRI  
- Task-based fMRI  

**Key Constructs:**
- **Resilience:** adaptive competence, absence of psychopathology  
- **Protective processes:** familial and community-level supports  

**Goals:**
- Identify **neural markers of resilience**.  
- Explore **genetic, epigenetic, and environmental** influences using the twin design.  
- Test how **positive parenting and community factors** support normative neural architecture in adversity.

- **Investigator:** S. Burt  
- **Institution:** Michigan State University  
- **Assets in this repo:** 564  

---

### Integration of Neural Networks and Attachment in Human Infants (Collection ID: 2690)

This project studies how **maternal caregiving** and **attachment security** shape early brain network integration.

**Design:**
- Infant brain scans at **3 and 12 months** during natural sleep:
  - Resting-state fMRI  
  - DTI  
- Mother–infant interactions at **3, 6, and 9 months**, including:
  - Traditional lab paradigms  
  - Naturalistic home capture using automated technology  
- Attachment at **12 months** measured via the **Strange Situation Procedure**.

**Analysis:**
- Intra- and inter-network connectivity  
- Dynamic, whole-brain, data-driven methods to characterize network integration.

**Goals:**
- Link **caregiving**, infant behavior, and **brain network development**.  
- Clarify how early caregiving shapes trajectories of **socio-emotional** and **neural development**.

- **Investigator:** Nancy McElwain  
- **Institution:** University of Illinois at Urbana–Champaign  
- **Assets in this repo:** 111  

---

### Cincinnati MR Imaging of Neurodevelopment (C-MIND) (Collection ID: 2329)

Part of the **Pediatric Functional Neuroimaging Research Network**, led by Cincinnati Children’s Hospital.

**Collaborators:**
- CCHMC Pediatric Neuroimaging Research Consortium  
- LONI (USC)  
- UCLA Brain Mapping Center  
- Children’s Hospital of Pittsburgh  
- University of Michigan  

**Imaging:**
- 3D T1- and T2-weighted anatomical scans  
- BOLD-fMRI  
- DTI  
- ASL perfusion  
- Concurrent **ASL/BOLD-fMRI** for neurovascular coupling studies  

**Cohort:**
- >200 typically developing children (cross-sectional)  
- Longitudinal subsets:
  - 40 infants/toddlers (0–3 years)  
  - 30 children (7–9 years)  

**Focus:**
- Normal brain maturation from infancy through adolescence  
- Changes in **white/gray matter**, **connectivity**, **neurovascular coupling**, and behavior.

- **Investigators:** Scott Holland, Jennifer Vannest  
- **Organization:** Cincinnati Children’s Hospital Medical Center  
- **Assets in this repo:** 567  

---

### Integrity and Dynamic Processing Efficiency of Networks in ASD (Collection ID: 2285)

This project integrates **fcMRI, DTI, and MEG** to study network abnormalities in **Autism Spectrum Disorders (ASD)**.

**Participants:**
- 60 adolescents with ASD  
- 60 matched typically developing controls  

**Methods:**
- fMRI during **lexical-semantic decision** to identify nodes in a VLSEM (Visual, Lexico-Semantic, Executive, Motor) circuit.  
- DTI to characterize **white matter connectivity** between VLSEM nodes.  
- MEG to assess **dynamic processing efficiency** and real-time network dynamics.

**Goals:**
- Map functional and structural connectivity in VLSEM circuits.  
- Understand how circuit-level abnormalities relate to cognitive and socio-communicative impairments in ASD.

- **Investigator:** Ralph-Axel Mueller  
- **Institution:** San Diego State University  
- **Assets in this repo:** 145  

---

### Taste Reward Circuits and Prediction Error in Eating Disorders (Collection ID: 2138)

This project studies **anorexia nervosa (AN)** and **bulimia nervosa (BN)** using an **RDoC Prediction Error** framework.

**Participants:**
- Adolescents and young adults (16–29 years) at high risk for severe ED outcomes.

**Aims:**
1. **Functional reward circuits (fMRI):**
   - Taste-reward **prediction error** responses in:
     - Anteroventral striatum  
     - Insula  
     - Anterior cingulate cortex (ACC)  
   - Hypothesis: lower BMI → heightened ACC activation to reward-predicting stimuli.
2. **Structural MRI and DTI:**
   - Gray/white matter volumes and integrity.  
   - Severe ED behaviors expected to relate to lower caudate/insula volumes.
3. **RDoC-based clustering:**
   - Cluster patients by **prediction error profiles**, comparing to DSM categories.  
   - Hypothesis: prediction-error clustering better captures ED-relevant behaviors.

- **Investigator:** Joel Stoddard  
- **Institution:** University of Colorado  
- **Assets in this repo:** 67  

---

### Effects of Poverty on Affective Development (Collection ID: 2106)

A multi-level, longitudinal study of how **poverty-related stress** shapes affective development and psychopathology risk.

**Sample:**
- Teens from the **Fragile Families and Child Wellbeing Study (FFCWS)**: a national birth cohort largely from low-income families.  
- Longitudinal data from birth to age 15, with follow-up at age 17.

**Assessments (age 15):**
- fMRI (emotional faces; amygdala–vmPFC circuitry)  
- DTI (structural connectivity)  
- HPA axis measures (cortisol, DHEA response to stress)  
- Attention bias tasks  
- Self- and parent-report of negative affect, anxiety, depression  

**Goals:**
- Understand **biological embedding** of poverty (HPA axis, amygdala–prefrontal circuits).  
- Identify pathways from chronic stress to **anxiety and depression**.

- **Investigator:** Christopher Monk  
- **Institution:** University of Michigan  
- **Assets in this repo:** 385  

---

### Multidimensional Investigation of Cognitive Control Deficits in Psychopathology (Collection ID: 2102)

This study examines **psychotic spectrum disorders (PSD)**—including schizophrenia, schizoaffective disorder, and bipolar disorder with psychotic features—through the lens of **cognitive control**.

**Participants:**
- 175 PSD patients, continuously recruited.

**Data:**
- Extensive clinical and cognitive batteries  
- Multimodal neuroimaging:
  - Task and resting fMRI  
  - DTI for white matter integrity  

**Goals:**
- Identify **circuit-level pathologies** predicting cognitive control deficits across PSD diagnoses.  
- Relate neurophysiological profiles to real-world functioning and symptoms.  
- Incorporate **genetic analyses** (SNPs, CNVs) in dopamine, glutamate, GABA, and synaptic pathways.  
- Use clustering (e.g., k-means) and cross-validation to define biologically meaningful subgroups.

- **Investigator:** Andrew Robert Mayer  
- **Institution:** Mind Research Network  
- **Assets in this repo:** 183  

---

### 2/3 – Social Processes Initiative in Neurobiology of the Schizophrenia(s) (Collection ID: 2098)

This project targets **social cognitive (SCog) impairments** across **Schizophrenia Spectrum Disorders (SSDs)** using an **RDoC-based** framework.

**Approach:**
- Structural MRI for grey matter morphology and network topology.  
- DTI for white matter circuits.  
- Resting and task-based fMRI for circuit function.  
- Multivariate PLS to relate brain structure, function, and behavior.

**Goals:**
- Characterize abnormal brain–behavior relationships in SCog processes.  
- Map SCog constructs across the full spectrum from healthy controls to SSDs.  
- Identify new therapeutic targets for social impairments in SSD.

- **Investigators:** Anil K. Malhotra, Aristotle Voineskos, Robert W. Buchanan  
- **Organization:** The Feinstein Institute for Medical Research  
- **Assets in this repo:** 899  

---

### Multimodal Developmental Neurogenetics of Females with ASD (Collection ID: 2021)

This project focuses on **sex differences** in ASD by deeply phenotyping and genotyping a **sex-balanced cohort**.

**Cohort:**
- 125 ASD participants  
- 125 typically developing controls  
- Unaffected siblings  
- Parental genotyping for family-based analyses

**Data Types:**
- Behavioral phenotyping across multiple domains  
- Imaging:
  - Structural MRI  
  - DTI  
  - Task and resting-state fMRI  
  - EEG  
- Genetics:
  - CNV  
  - SNV  

**Goals:**
- Identify sex-specific differences in **brain structure, function, and connectivity**.  
- Relate CNVs/SNVs to brain phenotypes.  
- Explain heterogeneity in ASD via integrated brain–genetic–behavioral analyses (e.g., iWGCNA).

- **Investigator:** Kevin Pelphrey  
- **Institution:** University of Virginia  
- **Assets in this repo:** 243  

---

## How to Access Original Data in NDA

1. Visit the **NIMH Data Archive** portal.  
2. Search using the **Collection ID** (e.g., 1974, 19, 1890, 3445…).  
3. Submit a **Data Use Agreement (DUA)** for access to individual-level data where required.  
4. After approval, download imaging and phenotypic data directly from NDA.

The derivatives in this GitHub repository are intended to complement the official NDA distributions and to facilitate **diffusion/tractography** and **connectomics** analyses.

---

© 2025 LabSolver / Pittsburgh Fiber Data Hub.  
Source datasets © respective investigators and the National Institute of Mental Health Data Archive (NDA).  
All `.fz` outputs are shared under **CC BY-NC-SA**, and use of underlying NDA data must follow NDA policies and DUAs.
