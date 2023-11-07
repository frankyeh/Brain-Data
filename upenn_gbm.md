# UPenn GBM

<img src="https://github.com/frankyeh/Brain-Data/assets/275569/254e976c-2acb-4878-9c8a-b70a468c8321" width=600 />


This dataset from the University of Pennsylvania Health System consists of multi-parametric magnetic resonance imaging (mpMRI) scans of de novo Glioblastoma (GBM) patients, along with patient information, clinical outcomes, genomic data, and tumor progression. The collection includes computer-aided and manually-corrected segmentation labels of various tumor sub-regions, as well as the whole brain, in NIfTI format. The scans underwent skull-stripping and co-registration, with the tumor segmentation labels revised and approved by neuroradiologists. The dataset provides a range of radiomic features, allowing for comprehensive computational and clinical studies, and can be used as gold standard labels for performance evaluation in computational challenges. Additionally, the dataset includes H&E-stained digitized tissue sections from resected tumor specimens.

# License

[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)

Reference: Bakas S, Sako C, Akbari H, Bilello M, Sotiras A, Shukla G, Rudie JD, Santamaría NF, Kazerooni AF, Pati S, Rathore S. The University of Pennsylvania glioblastoma (UPenn-GBM) cohort: Advanced MRI, clinical, genomics, & radiomics. Scientific data. 2022 Jul 29;9(1):453.

Data source: (https://wiki.cancerimagingarchive.net/pages/viewpage.action?pageId=70225642)

# Download

- [FIB files (n=531)](https://pitt-my.sharepoint.com/:f:/g/personal/yehfc_pitt_edu/ErTB_g-GlCFAjehZac0LFOcBO6_4fzMADNK_rLhwb68UiA?e=J7pfEF) (Ready-to-track using [DSI Studio](https://dsi-studio.labsolver.org))
- [T1w,T1w-GD, T2w, T2FLAIR (n=671)](https://pitt-my.sharepoint.com/:f:/g/personal/yehfc_pitt_edu/EhWEXMOF06BGgOo2pTngdagBx4r8mVOMlZRJ3WFb5k_Igw?e=5lepMh)
- [Tumor segmentation (n=147)](https://pitt-my.sharepoint.com/:f:/g/personal/yehfc_pitt_edu/EhDguTTifyJDjhQHmm1zkjYBs5KvegY0aFvrXMFQcbHBKA?e=rxnFlY)
  
  1: necrotic tissue, 2: peritumoral edema, 3: enhancing tumor. The segmentation was the original expert segmentation provided by UPennGBM
  
- [Tumor and brain tissue segmentation (n=147)](https://pitt-my.sharepoint.com/:f:/g/personal/yehfc_pitt_edu/Eju3Ox1acX9MrqdoLbeNzM4BHAnTro5_VZL-uHS4YadlXg?e=N3lAuQ)
  
  1: white matter 2: cerebral gray matter 3: cerebellar gray matter 4: thalamus and basal ganglion 5: ventricle 6: necrotic tissue, 7: peritumoral edema, 8: enhancing tumor. The tumor segmentation was the same as above, whereas the brain tissue segmentation was generated using [U-Net Studio](https://unet-studio.labsolver.org/).
  
- Data quality control: [pre-eddy](https://pitt-my.sharepoint.com/:t:/g/personal/yehfc_pitt_edu/Ea60Z0sosudOnNYJ9wxeab0BGSmCjjrqA5lFGh8ntdq5Ug?e=lexYxD), [post-eddy](https://pitt-my.sharepoint.com/:t:/g/personal/yehfc_pitt_edu/EQDimHxxrK5Etgu3EhpXBxQB0-CM_7HckqYA9l7pXcVDjQ?e=sBOeIr)
- [Demographics](https://pitt-my.sharepoint.com/:x:/g/personal/yehfc_pitt_edu/ET6yAsuDD6lOrkWzncWhmpYBpcXGiFhVxxNLGLBhUDO6vQ?e=xUc1qb)


# Methods

*Some DWI were acquired at a different protocol. Please check each FIB file for details*
The diffusion images were acquired on a SIEMENS TrioTim scanner using a 2D EPI diffusion sequence (ep2d_DTI_30dir). TE=91 ms, and TR=5400 ms. A DTI diffusion scheme was used, and a total of 90 diffusion sampling directions were acquired. The b-value was 1000 s/mm². The in-plane resolution was 1.71875 mm. The slice thickness was 3 mm. FSL eddy was used to correct for eddy current distortion. The correction was conducted through the integrated interface in DSI Studio ("Chen" release)(http://dsi-studio.labsolver.org). The diffusion MRI data were rotated to align with the AC-PC line at an isotropic resolution of 2mm. The restricted diffusion was quantified using restricted diffusion imaging (Yeh et al., MRM, 77:603–612 (2017)). The diffusion data were reconstructed using generalized q-sampling imaging (Yeh et al., IEEE TMI, ;29(9):1626-35, 2010) with a diffusion sampling length ratio of 1.25.

# Processing Scripts

**1. Rename DICOM**
This was done using DSI Studio GUI interface [Step B1b]

**2. DICOM to SRC**
This was done using DSI Studio GUI interface [Step B2b]

**3. EDDY**
```
#!/bin/bash
subs=$(ls -Lr *.src.gz | grep -v 'corrected')

subs=(${subs// /})

if [ -f "${subs[$1]}.corrected.src.gz" ]; then
    echo "File ${subs[$1]}.corrected.src.gz already exists."
else
    singularity exec /ocean/projects/cis200024p/shared/scripts/dsistudio_latest.sif dsi_studio --action=rec --source=${subs[$1]} --cmd="[Step T2][Corrections][EDDY]" --align_acpc=2 --save_src="${subs[$1]}.corrected.src.gz"
fi
```

**4. Align AC-PC and GQI recon**

```
#!/bin/bash
subs=$(ls -L *.src.gz)
subs=(${subs// /})
echo "processing ${subs[$1]}"
singularity exec dsistudio_latest.sif dsi_studio --action=rec --source=${subs[$1]} --align_acpc=2
```
