# Adolescent Brain Cognitive Development (ABCD) Study — Diffusion MRI Derivatives

The **Adolescent Brain Cognitive Development℠ (ABCD) Study** is the largest long-term study of brain development and child health in the United States.  
Funded by the **National Institutes of Health (NIH)**, the ABCD Research Consortium includes:

- A **Coordinating Center** (UC San Diego; PIs: Terry Jernigan & Sandra Brown)  
- A **Data Analysis, Informatics & Resource Center (DAIRC)**  
- **21 research sites** across the U.S. that together enrolled **11,880 children (ages 9–10)**

Participants are followed from late childhood into young adulthood with:

- MRI (structural, diffusion, functional)
- Cognitive and behavioral assessments
- Environmental and family-context measures
- Biospecimen-based measures (genetics, etc.)

Using cutting-edge neuroimaging and deep phenotyping, ABCD examines how real-world experiences  
(e.g., **sports, videogames, social media, sleep patterns, substance use**) interact with biology to shape:

- Brain structure and connectivity  
- Social, behavioral, academic, and health outcomes  

The results are intended to inform **families, educators, clinicians, and policymakers** with practical knowledge to support youth well-being and success.

This repository provides **derived diffusion MRI FIB files** for **ABCD sites 01–22**, processed into tractography-ready derivatives for use in **DSI Studio** and related tools.

> **Raw ABCD data are *not* redistributed here.**  
> Access to original data (DICOM / NIfTI / full phenotypes) must follow ABCD’s NDA-based data-sharing policies.

---

## License

The derived FIB files in this repository are shared under the  
**Creative Commons Attribution-ShareAlike 4.0 International License (CC BY-SA 4.0)**.

If you use these data, please acknowledge:

> “This work used XSEDE/ACCESS computing resources: **TG-CIS200026** & **MED230052**.”

You should also follow the ABCD Study’s citation guidance, e.g.:

> “Source: **Adolescent Brain Cognitive Development℠ (ABCD) Study**.”

---

## ABCD Consortium and Study Sites

The ABCD Research Consortium consists of a Coordinating Center, DAIRC, and **21 study sites**, including:

- **Children’s Hospital Los Angeles**  
- **Florida International University**  
- **Laureate Institute for Brain Research (LIBR)**  
- **Medical University of South Carolina**  
- **Oregon Health & Science University**  
- **SRI International**  
- **UC San Diego**  
- **UCLA**  
- **University of Colorado Boulder**  
- **University of Florida**  
- **University of Maryland, Baltimore**  
- **University of Michigan**  
- **University of Minnesota**  
- **University of Pittsburgh**  
- **University of Rochester**  
- **University of Utah**  
- **University of Vermont**  
- **University of Wisconsin–Milwaukee**  
- **Virginia Commonwealth University**  
- **Washington University in St. Louis**  
- **Yale University**

Each site contributes to the nationwide sample with harmonized MRI protocols and coordinated behavioral/clinical assessments.

The **ABCD Study®, Teen Brains. Today’s Science. Brighter Future.®** and related marks are registered or service marks of the  
**U.S. Department of Health & Human Services (HHS)**.

---

## Dataset in This Repository

This repository contains **derived diffusion MRI FIB datasets** organized by site-level tags:

- `abcd-site01`
- `abcd-site02`  
- …  
- `abcd-site22`

Each tag corresponds to one or more ABCD sites or batches of participants, processed with a consistent DSI Studio workflow.

---

## Download All ABCD Site Datasets

The commands below will download **all 22 site releases** (`abcd-site01` … `abcd-site22`) from the GitHub API.

> **Note:**  
> - Make sure `curl` and `jq` are installed for Linux/macOS.  
> - On Windows, use **PowerShell 5.x** or newer.  
> - Run these commands in the directory where you want the files saved.

---

### Linux / macOS — bash

This loop will iterate over `abcd-site01` to `abcd-site22` and download all associated assets:

```bash
for i in $(seq -w 1 22); do
  curl -s "https://api.github.com/repos/data-nih/abcd/releases/tags/abcd-site$i" \
    | jq -r '.assets[].browser_download_url' \
    | xargs -n1 -P4 curl -LO
done
````

* `seq -w 1 22` generates `01 02 ... 22` (zero-padded)
* `jq` extracts each asset’s `browser_download_url`
* `xargs -P4` downloads multiple files in parallel (adjust `-P` if needed)

---

### Windows — PowerShell 5.x

In **File Explorer**, go to your target folder, click the address bar, type `powershell`, and press **Enter**.
Then run:

```powershell
1..22 | ForEach-Object {
  (Invoke-RestMethod ("https://api.github.com/repos/data-nih/abcd/releases/tags/abcd-site{0:D2}" -f $_)).assets |
    ForEach-Object {
      Invoke-WebRequest $_.browser_download_url -OutFile (Split-Path $_.browser_download_url -Leaf)
    }
}
```

This:

* Loops over site indices `1..22`
* Formats each tag as `abcd-site01`, `abcd-site02`, …, `abcd-site22`
* Uses `Invoke-RestMethod` to query the GitHub Release API
* Downloads each asset to the current directory with its original filename

---

## Notes and Responsibilities

* This repository **does not** host original ABCD DICOM or full phenotypic data.

* All analyses must comply with:

  * **ABCD data-use agreements** via NDA
  * **Institutional review board (IRB)** and local data-governance policies
  * **ABCD Study®** citation and trademark guidance

* Derived FIB files are provided to **accelerate tractography and connectomics** research; users remain responsible for:

  * Appropriate QC of diffusion data and derivatives
  * Correct modeling and statistical practices
  * Respecting participant privacy and confidentiality in all outputs

If you build tools, atlases, or publications using these derivatives, consider sharing them back with the community to extend the impact of the **ABCD Study℠**.

