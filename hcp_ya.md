# Introduction

The data are originally from the minimally-preprocessed dMRI data from WU-Minn HCP Consortium and converted to DSI Studio SRC files format. The SRC file stores the minimum information needed for diffusion MRI processing, including the DWI data, image resolution, and the b-table. The SRC file can be converted back to 4D NIFTI in DSI Studio.

# License

The data are shared under the WU-Minn HCP open access data use term (4) at <https://www.humanconnectome.org/study/hcp-young-adult/document/wu-minn-hcp-consortium-open-access-data-use-terms>

Please acknowledge the source to the WU-Minn HCP.

# Download

- [Diffusion MRI SRC Files](https://pitt-my.sharepoint.com/:f:/g/personal/yehfc_pitt_edu/EmL_WkIkt3pFilc6MeqRoX0Bwhvs0Lr7X9LAoIucajLUwQ?e=c0w9xQ)

  ***Methods***
  > The minimally-preprocessed data (Glasser et al., 2013) from Human Connectome Projects (Q1-Q4 release, 2015) were acquired by Washington University in Saint Louis and University of Minnesota (Van Essen et al., 2012). The diffusion MRI scan was conducted on a Siemens 3T Skyra scanner using a 2D spin-echo single-shot multiband EPI sequence with a multi-band factor of 3 and monopolar gradient pulse. The spatial resolution was 1.25 mm isotropic. TR = 5500 ms, TE = 89.50 ms. The b-values were 1000, 2000, and 3000 s/mm2. The total number of diffusion sampling directions was 90, 90, and 90 for each of the shells in addition to 6 b0 images. The preprocessed data were corrected for eddy current and susceptibility artifact.

  The original NIFTI files can be downloaded from the HCP's connectome db website.

- Diffusion MRI FIB Files: [1mm](https://pitt-my.sharepoint.com/:f:/g/personal/yehfc_pitt_edu/EhAofmkwtjlMlSku3_vniFEBkStumkY2i5y2YtoqIAOMBQ?e=qBrXBZ), [2mm](https://pitt-my.sharepoint.com/:f:/g/personal/yehfc_pitt_edu/EvFAkXbKPjVCjuTuWcuyGyYBZRAUi4ytmwi9jDI1kFtguA?e=AeCl0n)
- [T1W](https://pitt-my.sharepoint.com/:f:/g/personal/yehfc_pitt_edu/EkPCanH2hTBEh47ZFHXIHuUBaYhGS5lcz3Hi1lAGoeqMcw?e=vCSidk)
- Demographics at <https://db.humanconnectome.org/>
- [Local connectome fingerprint](https://pitt-my.sharepoint.com/:f:/g/personal/yehfc_pitt_edu/Esw0yxBQM4pCtnjoRLm41kQBejzvhTd6p-XYcDCWMMIhyg?e=X1EKBL) [1]

   * LCF of all 930 subjects: HCP930_fp.mat
   * ID of the subjects: HCP930.QSDR25.db.fib.gz.name.txt
   * Squared difference of 930 subjects: HCP930.QSDR25.db.fib.gz.vec.dif.mat

  **Methods**
  > A group average template was constructed from a total of 930 subjects. A multishell diffusion scheme was used, and the b-values were 1000, 2000, and 3000 s/mm2. The number of diffusion sampling directions were 90, 90, and 90, respectively. The in-plane resolution was 1.25 mm. The slice thickness was 1.25 mm. The diffusion data were reconstructed in the MNI space using q-space diffeomorphic reconstruction (Yeh et al., Neuroimage, 58(1):91-9, 2011) to obtain the spin distribution function (Yeh et al., IEEE TMI, ;29(9):1626-35, 2010). A diffusion sampling length ratio of 2.5 was used, and the output resolution was 1 mm. The analysis was conducted using DSI Studio (http://dsi-studio.labsolver.org).


## Reference

[1] Yeh F-C, Vettel JM, Singh A, Poczos B, Grafton ST, Erickson KI, et al. (2016) Quantifying Differences and Similarities in Whole-Brain White Matter Architecture Using Local Connectome Fingerprints. PLoS Comput Biol 12(11): e1005203. https://doi.org/[10.1371/journal.pcbi.1005203](http://dx.doi.org/10.1371/journal.pcbi.1005203)\
