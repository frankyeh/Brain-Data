# Introduction

The HCP842 template and HCP1065 template are averaged from HCP data of the WU-Minn HCP Consortium (Q1-Q3, 2014) and distributed under the WU-Minn HCP open access data use term.\
To view this template or perform fiber tracking, please download [DSI Studio](http://dsi-studio.labsolver.org/dsi-studio-download) and open it in STEP3 Fiber Tracking.

# License

The HCP-1065 data are shared under the WU-Minn HCP open access data use term (4) at <https://www.humanconnectome.org/study/hcp-young-adult/document/wu-minn-hcp-consortium-open-access-data-use-terms> Please acknowledge the source to the WU-Minn HCP.

The FSL version of the HCP-1065 DTI templates are shared under the FSL license: https://fsl.fmrib.ox.ac.uk/fsl/fslwiki/Licence

# Reference

Please cite the following publications if you are using the HCP1065 or HCP842 FIB files.

***HCP-1065***

Yeh, F. C. (2021) Population-Based Tract-To-Region Connectome of the Human Brain and Its Hierarchical Topology, preprint DOI: 10.21203/rs.3.rs-1083262/v1

***HCP-842***

Yeh, F. C., Panesar, S., Fernandes, D., Meola, A., Yoshino, M., Fernandez-Miranda, J. C., ... & Verstynen, T. (2018). Population-averaged atlas of the macroscale human structural connectome and its network topology. NeuroImage, 178, 57-68. PubMed: https://www.ncbi.nlm.nih.gov/pubmed/29758339

# Download

## HCP-1065 GQI/QSDR template
> Yeh, F. C. (2021) Population-Based Tract-To-Region Connectome of the Human Brain and Its Hierarchical Topology, preprint DOI: 10.21203/rs.3.rs-1083262/v1

- [HCP1065 1-mm FIB file](https://pitt-my.sharepoint.com/:u:/g/personal/yehfc_pitt_edu/EenyiepzWeFEj8bavPNkz84ByQeJAHGW6Hka410uyeUqxA?e=rcS3Lg) (for fiber tracking)
- [HCP1065 2-mm FIB file](https://pitt-my.sharepoint.com/:u:/g/personal/yehfc_pitt_edu/EYbDjxK3HEpNqIo6sYtkY4MBhRkWjJLawmgyTbLrcbho8A?e=Ooy3Ix) (for fiber tracking)
- [HCP1065 2-mm connectometry db](https://pitt-my.sharepoint.com/:u:/g/personal/yehfc_pitt_edu/EbQV0IwTavhOhx_SggUThLkB267eZkJ1eCGzclwk8llKYQ?e=QJl5po) (for connectometry analysis)
- [HCP1065 QA NIFTI file](https://pitt-my.sharepoint.com/:u:/g/personal/yehfc_pitt_edu/EQr_xqaHi-1Cpdk62rKKCuoBIAD6NOTPQ0IX6-s2zNzNSg?e=hAk3UA)
- [HCP1065 nQA NIFTI file](https://pitt-my.sharepoint.com/:u:/g/personal/yehfc_pitt_edu/EXSuHdkM05tPtn1Jf1o3LuQBMiqJjVjmaydX5xHrRqifzQ?e=4z1yz7)
- [HCP1065 GFA NIFTI file](https://pitt-my.sharepoint.com/:u:/g/personal/yehfc_pitt_edu/EdOmAK3VdwJKrRU1OTJwQEIBId7eVO2rRjTS_omTjFHf2Q?e=hMZkuY)
- [HCP1065 ISO NIFTI file](https://pitt-my.sharepoint.com/:u:/g/personal/yehfc_pitt_edu/Ea6MZybx-gVHsjEmKxMIqb4B7fYJKg1snk37BKM4YRXPbw?e=O8nD0M)

GQI is a model-free method to reconstruct diffusion distribution from DWI data. QSDR is the MNI version of GQI. Both methods provide quantitative anisotropy (QA), a model-free anisotropy derived from diffusion distribution, and "ISO" is the isotropy counterpart. The FIB files provides population-averaged fiber orientation that can be used for fiber tracking in the MNI space.

The HCP1065 registration is based on the nonlinear ICBM152 2009a space. The template can be used with the T1W images from Montreal Neurological Institute: <http://www.bic.mni.mcgill.ca/~vfonov/icbm/2009/> or histology images from the Big Brain data: <https://bigbrain.loris.ca/main.php?test_name=brainvolumes>\
The HCP 1065 template was constructed from a total of 1065 subjects' diffusion MRI data from the Human Connectome Project (2017 Q4, 1200-subject release). There were 575 female (others male). Age ranges from 22 to 37 with a mean of 28.74, Q1=26, median=29, Q4=32. A multishell diffusion scheme was used, and the b-values were 1000, 2000, 3000 s/mm2. The number of diffusion sampling directions were 90, 90, and 90, respectively. The in-plane resolution was 1.25 mm. The slice thickness was 1.25 mm. The diffusion data were reconstructed in the MNI space using q-space diffeomorphic reconstruction (Yeh et al., Neuroimage, 58(1):91-9, 2011) to obtain the spin distribution function (Yeh et al., IEEE TMI, ;29(9):1626-35, 2010). A diffusion sampling length ratio of 1.7 was used, and the output resolution was 1 mm. The analysis was conducted using DSI Studio (http://dsi-studio.labsolver.org).

## HCP-1065 DTI template
> (FSL version)

- [FSL-HCP1065-FA NIFTI file](https://pitt-my.sharepoint.com/:u:/g/personal/yehfc_pitt_edu/EV3F_eZvN6NDv-PN4I05dzwBu1kLrqnK_N6VplznsVQv0Q?e=wXGOo7) 
- [FSL-HCP1065-L1 NIFTI file](https://pitt-my.sharepoint.com/:u:/g/personal/yehfc_pitt_edu/EbAIqQWpo0tMmel0FVtjeacBjF9KLRf-_vKaRnWOK_Ef8w?e=PIShEa)
- [FSL-HCP1065-L2 NIFTI file](https://pitt-my.sharepoint.com/:u:/g/personal/yehfc_pitt_edu/EbbouNOBp5dPsZJAuxU3tZoBkt-FSYgdw2Q5ZTweIe0_KA?e=YGXl1V) 
- [FSL-HCP1065-L3 NIFTI file](https://pitt-my.sharepoint.com/:u:/g/personal/yehfc_pitt_edu/EYx7wMxbv_RHh7rNwl8dUzABOzpn0QWLu92VyEUzL-OPjQ?e=XyaUtb) 
- [FSL-HCP1065-MD NIFTI file](https://pitt-my.sharepoint.com/:u:/g/personal/yehfc_pitt_edu/ET4LVhH8yKBEof3pMAio56QBEhSaDTCYR_s84ieukNVyiA?e=cnkgsR) 
- [FSL-HCP1065-MO NIFTI file](https://pitt-my.sharepoint.com/:u:/g/personal/yehfc_pitt_edu/EcPg8Rq-_uJHiiIxgSbUE1gB-TwVY7JBEwpFVap5Y_zckQ?e=g4yj8W) 
- [FSL-HCP1065-tensor NIFTI file](https://pitt-my.sharepoint.com/:u:/g/personal/yehfc_pitt_edu/ERC8xjhG46VKiYd5cGFSJPIBQ04_a10Q9WcgYS4fLyfyDw?e=gbxKov) 
- [FSL-HCP1065-V1 NIFTI file](https://pitt-my.sharepoint.com/:u:/g/personal/yehfc_pitt_edu/EaV0OpFqYDVFtOTp8KHFNTgBh9xMLBe_opFtoK9X-KZ2HA?e=f5CpEO)
- [FSL-HCP1065-V2 NIFTI file](https://pitt-my.sharepoint.com/:u:/g/personal/yehfc_pitt_edu/ERKhajyiyRlOkli5ww9BUX4Bn52Sk1femjFYuS8zyMx-nA?e=dANhRT)
- [FSL-HCP1065-V3 NIFTI file](https://pitt-my.sharepoint.com/:u:/g/personal/yehfc_pitt_edu/EdS1toEEnntIkGwyytqGoB4Bwxht2Slfo1HGV9Sv4AvxgA?e=SgTIKQ)

The HCP1065 DTI template is redistributed from FSL (<https://fsl.fmrib.ox.ac.uk/fsl/fslwiki/Atlases>) under [FSL main license](https://fsl.fmrib.ox.ac.uk/fsl/fslwiki/Licence). These templates were derived from 1065 HCP subjects. Diffusion tensors were fitted using the b=1000 s/mm2 data after gradient non-linearities correction. Each tensor was transformed into MNI space using the HCP subject-specific volumetric transformations, after appropriate re-orientation (Alexander et al, IEEE TMI, 2001). The FA of the arithmetic mean of all MNI-transformed tensors was obtained. The work was carried out by S. Warrington, S. Jbabdi, S. Smith, S. Sotiropoulos. Data were provided by the Human Connectome Project, WU-Minn Consortium (Principal Investigators: David Van Essen and Kamil Ugurbil; 1U54MH091657) funded by the 16 NIH Institutes and Centers that support the NIH Blueprint for Neuroscience Research; and by the McDonnell Center for Systems Neuroscience at Washington University.

## HCP-842
> Yeh FC, Panesar S, Fernandes D, Meola A, Yoshino M, Fernandez-Miranda JC, Vettel JM, Verstynen T. Population-averaged atlas of the macroscale human structural connectome and its network topology. Neuroimage. 2018 Sep 1;178:57-68.

- [HCP842 1-mm FIB file](https://pitt-my.sharepoint.com/:u:/g/personal/yehfc_pitt_edu/EZLF09z_q3hErTHE_-13XjEBqFRvU7rFv0Uy24ulvLPLXQ?e=OUgZIH)
- [HCP842 2-mm FIB file](https://pitt-my.sharepoint.com/:u:/g/personal/yehfc_pitt_edu/Eflb1dpQfJhLum2Vls4DI20BDLhT2ilZZpu-gjc-MIGLwA?e=kBAAqj)

M: 372 F:470 ages: 20~40 (2015 Q4, 900-subject release)

The HCP842 registration is based on the FSL's FA template, which is the old ICBM152 space.

The HCP-842 template was constructed using a total of 842 subjects' diffusion MRI data from the Human Connectome Project (2015 Q3, 900-subject release). The diffusion images were acquired using a multishell diffusion scheme. The b-values were 1000, 2000, and 3000 s/mm2. The number of diffusion sampling directions were 90, 90, and 90. The in-plane resolution was 1.25 mm. The slice thickness was 1.25 mm. The diffusion data were reconstructed in the MNI space using q-space diffeomorphic reconstruction (Yeh et al., Neuroimage, 58(1):91-9, 2011) to obtain the spin distribution function (Yeh et al., IEEE TMI, ;29(9):1626-35, 2010). A diffusion sampling length ratio of 1.25 was used, and the output resolution was 1 mm. The atlas was constructed by averaging the SDFs of the 842 individual subjects.
