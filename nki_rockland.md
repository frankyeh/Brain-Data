# The NKI Rockland Sample

# Introduction

<img src="https://media.springernature.com/full/springer-static/image/art%3A10.1038%2Fs41597-022-01329-y/MediaObjects/41597_2022_1329_Fig1_HTML.png?as=webp" with=600/>

The NKI Rockland Sample Initiative, funded by the US National Institutes of Health and NY State Office of Mental Health, is a cutting-edge research program mapping the human brain's development and its connections to behavior. With over 1,500 participants from Rockland County and nearby areas, this initiative actively involves individuals of all ages in shaping our understanding of mental health. For researchers, the NKI-Rockland Sample offers a well-supported, rich neuroimaging and phenotypic resource, fostering collaborative efforts to advance knowledge on normative brain-behavior relationships across the lifespan.

# License

NKI-Rockland Sample data are distributed using the [Creative Commons-Attribution-Noncommercial license](https://creativecommons.org/licenses/by-nc/4.0/legalcode). For the high-dimensional phenotypic data, all terms specified by the [DUA](http://fcon_1000.projects.nitrc.org/indi/enhanced/data/DUA.pdf) must be complied with.

Reference: [Tobe, R. H., MacKay-Brandt, A., Lim, R., Kramer, M., Breland, M. M., Tu, L., ... & Milham, M. P. (2022). A longitudinal resource for studying connectome development and its psychiatric associations during childhood. Scientific Data, 9(1), 300.](https://www.nature.com/articles/s41597-022-01329-y)

[official website](https://www.nki.rfmh.org/) [fcon website](https://fcon_1000.projects.nitrc.org/indi/enhanced/index.html) [Original download](https://fcon_1000.projects.nitrc.org/indi/pro/nki.html)

# Participants and Experiments

The enhanced Nathan Kline Institute-Rockland Sample I was an institutionally centered endeavor aimed at creating a large-scale community neuroimaging sample of participants across the lifespan (ages 6-85 years). Measures included a wide array of physiological and behavioral assessments, cognitive and psychiatric characterization, genetic information, and advanced neuroimaging. Anonymized data are publicly shared openly and were released prospectively (i.e., on a quarterly basis) as data were collected. The NKI Rockland Sample I data resource includes N = 1, 500 participants across the first set of NIH funded studies (2011-2020).

# Phenotypic data

Phenotypic data can be accessed at [COINS Data Exchange](https://coins.trendscenter.org/). Except for age, sex, and handedness, which are publicly available, NKI-RS phenotypic data are protected by a Data Usage Agreement (DUA). Investigators must complete the [DUA](http://fcon_1000.projects.nitrc.org/indi/enhanced/data/DUA.pdf) and have it approved by an authorized institutional official before receiving access. 

The NKI-Rockland phenotypic battery primarily focuses on dimensional mental health assessments, particularly psychiatric symptomatology detection (e.g., Conners ADHD Scale, Children's Depression Inventory). However, the reliance on deficit-only measures, common in the field, is questioned for its limitations in distinguishing behaviors among unaffected individuals. Recent efforts highlight this concern, emphasizing the need for measures assessing strengths as well as weaknesses. For ADHD assessment, both Conners (symptoms) and SWAN (strengths and weaknesses) are included, enabling exploration of this issue. While attempts were made to include measures emphasizing strength, standard clinical measures remain central due to the lack of assessments in psychiatric symptom characterization. The recommendation is to incorporate psychometric instruments producing dimensional distributions in non-clinical samples for community sample phenotyping.

# Download

| File Format | Modality/Content | Link | Details |
|-------------|---|---|---------|
| SRC | Eddy corrected DWI | [OneDrive](https://pitt-my.sharepoint.com/:f:/g/personal/yehfc_pitt_edu/EqZQ-MtXjsJIrsSR6NG-UdoBsAbG02mIFjLIhkxYh-9vhQ?e=hxJ4rN) | The SRC files contain raw dMRI signals for modeling. They can be reconstructed in DSI Studio to generate FIB files. The original NIFTI files can be downloaded from the HCP's connectome db website. |
| FIB | Fiber orientation maps in the native space| [OneDrive](https://pitt-my.sharepoint.com/:f:/g/personal/yehfc_pitt_edu/EoBg23PFRJJDhyadw9m6zmcBe9MAk_AmMET936jMdrXTTQ?e=TEwhB0) | GQI reconstructed FIB file in the native space. The FIB files are track-ready files for DSI Studio to run fiber tracking. |
| NIFTI | T1W/T2W | [OneDrive](https://pitt-my.sharepoint.com/:f:/g/personal/yehfc_pitt_edu/EpS8KXagRYxBjw6AO4B6QFkBx9O5xqJiMcnwC-BlfsBzAw?e=5uQKUT) |  |
| Text file | basic demographics (age sex) | [OneDrive](https://pitt-my.sharepoint.com/:u:/g/personal/yehfc_pitt_edu/Ebt-DMl-V-xEt3IbMk_mPB8BMMCteOQIrqm1gu44jM1HBw?e=tibzFF) | |

Download OneDrive data using [OneDrive Linux GUI](https://github.com/bpozdena/OneDriveGUI)

- BAS1: BASELINE1
- BAS2: BASELINE2
- FLU1: FOLLOWUP1 (mid-point follow-up)
- FLU2: FOLLOWUP2 (final follow-up) 
- TRT: RETEST BAS1 (usually acquired within 3 weeks of a baseline or a follow-up)

# Methods
> A total of 128 diffusion sampling directions were acquired. The b-value was 1500 s/mm². The in-plane resolution was 2 mm. The slice thickness was 2 mm. FSL eddy was used to correct for eddy current distortion. The correction was conducted through the integrated interface in DSI Studio ("Chen" release)(http://dsi-studio.labsolver.org). The diffusion MRI data were rotated to align with the AC-PC line. The restricted diffusion was quantified using restricted diffusion imaging (Yeh et al., MRM, 77:603–612 (2017)). The diffusion data were reconstructed using generalized q-sampling imaging (Yeh et al., IEEE TMI, ;29(9):1626-35, 2010) with a diffusion sampling length ratio of 1.25. 
