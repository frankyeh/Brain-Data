# Human Population-Averaged Diffusion MRI Template

The population-averaged templates are averaged from a group of subjects. The voxel-wise metrics are stored in NIFTI files, whereas the ready-to-track data are stored in FIB files, which can be opened in DSI Studio to perform fiber tracking.

# HCP-1065 Young Adult Templates

## QSDR-based template

<img src="https://user-images.githubusercontent.com/275569/149358303-47fbd938-a403-4b8d-ad1c-29993ed89c28.png" width="400">

> Yeh, FC. Population-based tract-to-region connectome of the human brain and its hierarchical topology. Nat Commun 13, 4933 (2022). https://doi.org/10.1038/s41467-022-32595-4

The HCP1065 registration is based on the nonlinear ICBM152 2009a space. The template can be used with the T1W images from Montreal Neurological Institute: <http://www.bic.mni.mcgill.ca/~vfonov/icbm/2009/> or histology images from the Big Brain data: <https://bigbrain.loris.ca/main.php?test_name=brainvolumes>\
The HCP 1065 template was constructed from a total of 1065 subjects' diffusion MRI data from the Human Connectome Project (2017 Q4, 1200-subject release). There were 575 female (others male). Age ranges from 22 to 37 with a mean of 28.74, Q1=26, median=29, Q4=32. A multishell diffusion scheme was used, and the b-values were 1000, 2000, 3000 s/mm2. The number of diffusion sampling directions were 90, 90, and 90, respectively. The in-plane resolution was 1.25 mm. The slice thickness was 1.25 mm. The diffusion data were reconstructed in the MNI space using q-space diffeomorphic reconstruction (QSDR)(Yeh et al., Neuroimage, 58(1):91-9, 2011) to obtain the spin distribution function (Yeh et al., IEEE TMI, ;29(9):1626-35, 2010). A diffusion sampling length ratio of 1.7 was used, and the output resolution was 1 mm. The analysis was conducted using DSI Studio (http://dsi-studio.labsolver.org).


## License

The HCP-1065 data are shared under the WU-Minn HCP open access data use term (4) at <https://www.humanconnectome.org/study/hcp-young-adult/document/wu-minn-hcp-consortium-open-access-data-use-terms> Please acknowledge the source to the WU-Minn HCP.

## Download

The templates are averaged from HCP data of the WU-Minn HCP Consortium and distributed under the WU-Minn HCP open access data use term.\
To view this template or perform fiber tracking, please download [DSI Studio](http://dsi-studio.labsolver.org/dsi-studio-download) and open it in STEP3 Fiber Tracking.

HCP Templates from 1065 subjects:

| File Format | Resolution | Modality/Content | Link | Details |
|-------------|---|---|---------|----|
| FIB | 1-mm | fiber orientation maps| [OneDrive](https://pitt-my.sharepoint.com/:u:/g/personal/yehfc_pitt_edu/EVqdp-lm0_NCgsFkSNDZeP0Bb3PpiSJRGpOKFhvVgZihVQ?e=GhUuOc) | 1-mm population=averaged FIB file in the ICBM152 space. The FIB file is ready for DSI Studio to run fiber tracking. |
| FIB | 1.25-mm | fiber orientation maps| [OneDrive](https://pitt-my.sharepoint.com/:u:/g/personal/yehfc_pitt_edu/EfOJxSVJm71IppKBAzlEksoBjL7cFsjtZvAVkiCsgFWQGg?e=q3zoTd) | 1.25-mm population-averaged FIB file in the ICBM152 space. |
| FIB | 1.25-mm with ODF| fiber orientation maps and ODFs | [OneDrive](https://pitt-my.sharepoint.com/:u:/g/personal/yehfc_pitt_edu/EdUKF-NSIWdKhDFrhFcjk_IB83K86YStjg8csgxAKaiLVg?e=ogZokU) | 1.25-mm population-averaged ODFs |
| FIB | 2-mm | fiber orientation maps | [Github](https://github.com/frankyeh/DSI-Studio-atlas/raw/main/ICBM152_adult/ICBM152_adult.fib.gz) | 2-mm population-averaged FIB file in the ICBM152 space. |
| Connectometry DB | 2-mm | anisotropy of 1065 subjects | [Zenodo](https://zenodo.org/record/6324701/files/HCP1065.2mm.db.fib.gz?download=1) | 2-mm anisotropy of 1065 subjects in the ICBM152 space |
| NIFTI | 1-mm | Quantitative anisotropy (QA) | [Github](https://github.com/frankyeh/DSI-Studio-atlas/raw/main/ICBM152_adult/ICBM152_adult.QA.nii.gz) | 1-mm QA map derived from population-averaged ODF |
| NIFTI | 1-mm | generalized fractional anisotropy (GFA) | [Zenodo](https://zenodo.org/record/6324701/files/HCP1065_gfa.nii.gz?download=1) |  1-mm GFA map derived from population-averaged ODF |
| NIFTI | 1-mm | isotropic diffusion (ISO) | [Github](https://github.com/frankyeh/DSI-Studio-atlas/raw/main/ICBM152_adult/ICBM152_adult.ISO.nii.gz) | 1-mm ISO map derived from population-averaged ODF |

## DTI-based template

<img src="https://user-images.githubusercontent.com/275569/149358788-f195df02-a47e-4f7b-a580-cde7bbd505a4.png" width="400">

The DTI templates are redistributed is from the FSL package

### License

The FSL version of the HCP-1065 DTI templates are shared under the FSL license: https://fsl.fmrib.ox.ac.uk/fsl/fslwiki/Licence

### Download

| File Format | Modality/Content | Link |
| --- | --- | --- |
| NIFTI | FSL-HCP1065-FA | <https://pitt-my.sharepoint.com/:u:/g/personal/yehfc_pitt_edu/EV3F_eZvN6NDv-PN4I05dzwBu1kLrqnK_N6VplznsVQv0Q?e=wXGOo7> |
| NIFTI | FSL-HCP1065-L1 | <https://pitt-my.sharepoint.com/:u:/g/personal/yehfc_pitt_edu/EbAIqQWpo0tMmel0FVtjeacBjF9KLRf-_vKaRnWOK_Ef8w?e=PIShEa> |
| NIFTI | FSL-HCP1065-L2 | <https://pitt-my.sharepoint.com/:u:/g/personal/yehfc_pitt_edu/EbbouNOBp5dPsZJAuxU3tZoBkt-FSYgdw2Q5ZTweIe0_KA?e=YGXl1V> |
| NIFTI | FSL-HCP1065-L3 | <https://pitt-my.sharepoint.com/:u:/g/personal/yehfc_pitt_edu/EYx7wMxbv_RHh7rNwl8dUzABOzpn0QWLu92VyEUzL-OPjQ?e=XyaUtb> |
| NIFTI | FSL-HCP1065-MD | <https://pitt-my.sharepoint.com/:u:/g/personal/yehfc_pitt_edu/ET4LVhH8yKBEof3pMAio56QBEhSaDTCYR_s84ieukNVyiA?e=cnkgsR> |
| NIFTI | FSL-HCP1065-MO | <https://pitt-my.sharepoint.com/:u:/g/personal/yehfc_pitt_edu/EcPg8Rq-_uJHiiIxgSbUE1gB-TwVY7JBEwpFVap5Y_zckQ?e=g4yj8W> |
| NIFTI | FSL-HCP1065-tensor | <https://pitt-my.sharepoint.com/:u:/g/personal/yehfc_pitt_edu/ERC8xjhG46VKiYd5cGFSJPIBQ04_a10Q9WcgYS4fLyfyDw?e=gbxKov> |
| NIFTI | FSL-HCP1065-V1 | <https://pitt-my.sharepoint.com/:u:/g/personal/yehfc_pitt_edu/EaV0OpFqYDVFtOTp8KHFNTgBh9xMLBe_opFtoK9X-KZ2HA?e=f5CpEO> |
| NIFTI | FSL-HCP1065-V2 | <https://pitt-my.sharepoint.com/:u:/g/personal/yehfc_pitt_edu/ERKhajyiyRlOkli5ww9BUX4Bn52Sk1femjFYuS8zyMx-nA?e=dANhRT> |
| NIFTI | FSL-HCP1065-V3 | <https://pitt-my.sharepoint.com/:u:/g/personal/yehfc_pitt_edu/EdS1toEEnntIkGwyytqGoB4Bwxht> |



The HCP1065 DTI template is redistributed from FSL (<https://fsl.fmrib.ox.ac.uk/fsl/fslwiki/Atlases>) under [FSL main license](https://fsl.fmrib.ox.ac.uk/fsl/fslwiki/Licence). These templates were derived from 1065 HCP subjects. Diffusion tensors were fitted using the b=1000 s/mm2 data after gradient non-linearities correction. Each tensor was transformed into MNI space using the HCP subject-specific volumetric transformations, after appropriate re-orientation (Alexander et al, IEEE TMI, 2001). The FA of the arithmetic mean of all MNI-transformed tensors was obtained. The work was carried out by S. Warrington, S. Jbabdi, S. Smith, S. Sotiropoulos. Data were provided by the Human Connectome Project, WU-Minn Consortium (Principal Investigators: David Van Essen and Kamil Ugurbil; 1U54MH091657) funded by the 16 NIH Institutes and Centers that support the NIH Blueprint for Neuroscience Research; and by the McDonnell Center for Systems Neuroscience at Washington University.

# HCP-842 Young Adult Template

<img src="https://user-images.githubusercontent.com/275569/149359512-1fba65b7-f3b9-49aa-a5f3-628ca3a14ed9.png" width="400">

> Yeh FC, Panesar S, Fernandes D, Meola A, Yoshino M, Fernandez-Miranda JC, Vettel JM, Verstynen T. Population-averaged atlas of the macroscale human structural connectome and its network topology. Neuroimage. 2018 Sep 1;178:57-68.

The HCP842 registration used FSL's FA template as the template space. It is the old ICBM152 space.

The HCP-842 template was constructed using a total of 842 subjects' diffusion MRI data from the Human Connectome Project (2015 Q3, 900-subject release). The diffusion images were acquired using a multishell diffusion scheme. The b-values were 1000, 2000, and 3000 s/mm2. The number of diffusion sampling directions were 90, 90, and 90. The in-plane resolution was 1.25 mm. The slice thickness was 1.25 mm. The diffusion data were reconstructed in the MNI space using q-space diffeomorphic reconstruction (Yeh et al., Neuroimage, 58(1):91-9, 2011) to obtain the spin distribution function (Yeh et al., IEEE TMI, ;29(9):1626-35, 2010). A diffusion sampling length ratio of 1.25 was used, and the output resolution was 1 mm. The atlas was constructed by averaging the SDFs of the 842 individual subjects.

## License

The HCP-842 data are shared under the WU-Minn HCP open access data use term (4) at <https://www.humanconnectome.org/study/hcp-young-adult/document/wu-minn-hcp-consortium-open-access-data-use-terms> Please acknowledge the source to the WU-Minn HCP.

## Download

The hcp842 templates are averaged from HCP data of the WU-Minn HCP Consortium (Q1-Q3, 2014) and distributed under the WU-Minn HCP open access data use term.\
To view this template or perform fiber tracking, please download [DSI Studio](http://dsi-studio.labsolver.org/dsi-studio-download) and open it in STEP3 Fiber Tracking.

| File Format | Resolution | Modality/Content | Link | Details |
| --- | --- | --- | --- | --- |
| FIB | 1-mm | fiber orientation maps | [Zenodo](https://zenodo.org/record/6324701/files/HCP842.1mm.fib.gz?download=1) | 1-mm population-averaged FIB file in the ICBM152 space. The FIB file is ready for DSI Studio to run fiber tracking. |
| FIB | 2-mm | fiber orientation maps | [Zenodo](https://zenodo.org/record/6324701/files/HCP842.2mm.fib.gz?download=1) | 2-mm population-averaged FIB file in the ICBM152 space. |


M: 372 F:470 ages: 20~40 (2015 Q4, 900-subject release)

# DSI Studio Young Adult Templates

A group average template was constructed from a total of 32 subjects. The diffusion images were acquired on a SIEMENS Prisma_fit scanner using a diffusion sequence (dMRI_dir258_1 ). TE=99.2 ms, and TR=2490 ms. A diffusion spectrum imaging scheme was used, and a total of 257 diffusion sampling were acquired. The maximum b-value was 4010 s/mm². The in-plane resolution was 2 mm. The slice thickness was 2 mm. The accuracy of b-table orientation was examined by comparing fiber orientations with those of a population-averaged template (Yeh et al. Neuroimage, 2018). The diffusion data were reconstructed in the MNI space using q-space diffeomorphic reconstruction (Yeh et al., Neuroimage, 58(1):91-9, 2011) to obtain the spin distribution function (Yeh et al., IEEE TMI, ;29(9):1626-35, 2010).  A diffusion sampling length ratio of 1.25 was used. The output resolution in diffeomorphic reconstruction was 2 mm isotorpic. The restricted diffusion was quantified using restricted diffusion imaging (Yeh et al., MRM, 77:603–612 (2017)). The tensor metrics were calculated.

## Download

The following data were group averages of normal subjects scanned by Grid 258-direction acquisition.

| File Format | Resolution | Modality/Content | Link | Details |
| --- | --- | --- | --- | --- |
| FIB | 2-mm | Fiber Orientation Maps | [GRID 2-mm FIB file](https://zenodo.org/record/6324701/files/Grid258.2mm.fib.gz?download=1) | Population-averaged FIB file in the ICBM152 space ready for fiber tracking using DSI Studio. |
| NII.gz | - | QA Template | [GRID QA template](https://zenodo.org/record/6324701/files/Grid258_qa.nii.gz?download=1) | Quality assurance (QA) template in the NIfTI format. |
| NII.gz | - | NQA Template | [GRID NQA template](https://zenodo.org/record/6324701/files/Grid258_nqa.nii.gz?download=1) | Non-Quality assurance (NQA) template in the NIfTI format. |
| NII.gz | - | RDI Template | [GRID RDI template](https://zenodo.org/record/6324701/files/Grid258_rdi.nii.gz?download=1) | Restricted Diffusion Imaging (RDI) template in the NIfTI format. |
| NII.gz | - | ISO Template | [GRID ISO template](https://zenodo.org/record/6324701/files/Grid258_iso.nii.gz?download=1) | Isotropic template in the NIfTI format. |
| NII.gz | - | GFA Template | [GRID GFA template](https://zenodo.org/record/6324701/files/Grid258_gfa.nii.gz?download=1) | Generalized Fractional Anisotropy (GFA) template in the NIfTI format. |
| NII.gz | - | FA Template | [GRID FA template](https://zenodo.org/record/6324701/files/Grid258_dti_fa.nii.gz?download=1) | Fractional Anisotropy (FA) template in the NIfTI format. |
| NII.gz | - | AD Template | [GRID AD template](https://zenodo.org/record/6324701/files/Grid258_ad.nii.gz?download=1) | Axial Diffusivity (AD) template in the NIfTI format. |
| NII.gz | - | MD Template | [GRID MD template](https://zenodo.org/record/6324701/files/Grid258_md.nii.gz?download=1) | Mean Diffusivity (MD) template in the NIfTI format. |
| NII.gz | - | RD Template | [GRID RD template](https://zenodo.org/record/6324701/files/Grid258_rd.nii.gz?download=1) | Radial Diffusivity (RD) template in the NIfTI format. |
| DB.FIB | - | Connectometry DB  | [QA Connectometry DB](https://pitt-my.sharepoint.com/:u:/g/personal/yehfc_pitt_edu/EeNCSd5Aql9Nv3m_0yhkRhYB4sOy1YpM4JeOS1hYim7lCQ?e=ntESpg) | Quantitative anisotropy of the subjects |
| DB.FIB | - | Connectometry DB  | [FA Connectometry DB](https://pitt-my.sharepoint.com/:u:/g/personal/yehfc_pitt_edu/EU5pNgbm1iJEiC4zLUIO8RMB17JLvWsJ0mFma45TsoalXw?e=v7QGcj) | Fractional anisotropy of the subjects |


# CMU-60 Young Adult Template

The CMU-60 template is an averaged map of reconstructed fiber orientations from a 257-direction diffusion spectrum imaging (DSI) sequence from 60 neurologically healthy volunteers. The files are in DSI Studio format, which is free to download here. This dataset includes the original 30 subjects from the CMU-30 template (found here).
These data sets are free to use for research and education purposes. Please notify Dr. Verstynen should they be used in a conference abstract or publication.

## Participants
> Twenty nine male and thirty one female subjects were recruited from the local Pittsburgh community and the Army Research Laboratory in Aberdeen Maryland. All subjects were neurologically healthy, with no history of either head trauma or neurological or psychiatric illness. Subject ages ranged from 18 to 45 years of age at the time of scanning, with a mean age of 26 years (+/- 6 standard deviation). Six subjects were left handed (3 males, 3 females).

## Methods
> All participants were scanned on a Siemen’s Verio 3T system in the Scientific Imaging & Brain Research (SIBR) Centerat Carnegie Mellon University using a 32-channel head coil. We collected a 50 min, 257-direction DSI scan using a twice-refocused spin-echo EPI sequence and multiple q values (TR = 9,916 ms, TE = 157 ms, voxel size = 2.4 x 2.4 x 2.4 mm, FoV = 231 x 231 mm, b-max = 5,000 s/mm2, 51 slices). Head-movement was minimized during the image acquisition through padding supports and all subjects were confirmed to have minimal head movement during the can prior to inclusion in the template.

> All images were processed using a q-space diffeomorphic reconstruction method described previously (Yeh & Tseng, 2011). Briefly, this approach uses a non-linear coregistration approach (ICBM-152 space template regularization, 16 non-linear iterations) that registers the voxel-coordinate into MNI space while also maintaining distortion of the q-space vector during the normalization process. From here diffusion orientation distribution functions (dODFs) are reconstructed to spatial resolution of 2x2x2 mm. The final template image was created by averaging the ODF maps across all 60 subjects, and the resulting template can be used to obtain the representative tractography of the. The white matter surface is rendered independently from an externally supplied 1×1×1 mm resolution white matter image.


## Download

- [CMU60 2-mm FIB file](https://zenodo.org/record/6324701/files/CMU60.2mm.fib.gz?download=1)
- [CMU60 2-mm Connectometry DB](https://zenodo.org/record/6324701/files/CMU60.db.fib.gz?download=1)
- [CMU60 Demographics CSV](https://zenodo.org/record/6324701/files/CMU60.demo.csv?download=1)


# dHCP Neonate Template

The [dHCP study](https://www.humanconnectome.org/study/lifespan-developing-human-connectome-project) planned to enroll 1500 Subjects at age 20-44 weeks post-conception. The purpose is to link together imaging, clinical, behavioural, and genetic information.

The neonate template was constructed by averaging 584 neonate's dMRI data into a common space.

## License

The template is shared under the [dHCP data sharing agreement](http://www.developingconnectome.org/open-access-dhcp-data-terms-of-use-version-4-0_2019-05-23/). The source of the data are from the [3rd release](https://biomedia.github.io/dHCP-release-notes/index.html).

Users using the files should follow agreement and [cite/acknowledge the source](https://biomedia.github.io/dHCP-release-notes/cite.html).

## Methods

> A multishell diffusion scheme was used, and the b-values were 400 ,1000 and 2600 s/mm². The number of diffusion sampling directions were 64, 88, and 128, respectively. The in-plane resolution was 1.5 mm. The slice thickness was 1.5 mm. The images were denoised and corrected for Gibbs ringing, motion, eddy current, and susceptibility artifact using [the diffusion SHARD pipeline](https://biomedia.github.io/dHCP-release-notes/dwi-shard.html). A quality check was conducted using neighboring DWI correcltion (NDC) (Yeh, Neuroimage. 2019 Nov 15;202:116131). 34 out of 758 scans (including repeated scans) were excluded due to their low NDC values identified by a median value based outlier detector. 

> The dHCP group average template was constructed from a total of 584 subjects. The data were acquired with in-plane resolution of 1.5 mm and  slice thickness of 1.5 mm. The images were resampled to 1 mm isotropic resolution. The diffusion data were reconstructed in the MNI space using q-space diffeomorphic reconstruction (Yeh et al., Neuroimage, 58(1):91-9, 2011) to obtain the spin distribution function (Yeh et al., IEEE TMI, ;29(9):1626-35, 2010). A diffusion sampling length ratio of 1.25 was used. The output resolution in diffeomorphic reconstruction was 1 mm isotorpic. The restricted diffusion was quantified using restricted diffusion imaging (Yeh et al., MRM, 77:603–612 (2017)). The tensor metrics were calculated using DWI with b-value lower than 1750 s/mm².

## Download

- [dHCP population-average 0.5-mm FIB file](https://pitt-my.sharepoint.com/:u:/g/personal/yehfc_pitt_edu/EQ5vRB18kXNJoVitzZybM0MBCcOT70ZFS1qZzMvwNphm3g?e=3y8cqP)

