# Introduction

The data are originally from the minimally-preprocessed dMRI data from WU-Minn HCP Consortium and converted to DSI Studio SRC files format. The SRC file stores the minimum information needed for diffusion MRI processing, including the DWI data, image resolution, and the b-table. The SRC file can be converted back to 4D NIFTI in DSI Studio.

# License

The data are shared under the WU-Minn HCP open access data use term (4) at <https://www.humanconnectome.org/study/hcp-young-adult/document/wu-minn-hcp-consortium-open-access-data-use-terms>

Please acknowledge the source to the WU-Minn HCP.

# Download

- FIB Files: FIB files are read-to-track and can be opened in [DSI Studio](http://dsi-studio.labsolver.org) to perform fiber tracking.
  - [native-space 1-mm (GQI FIB)(OneDrive)](https://pitt-my.sharepoint.com/:f:/g/personal/yehfc_pitt_edu/EhAofmkwtjlMlSku3_vniFEBkStumkY2i5y2YtoqIAOMBQ?e=US4888)
  - [native-space 2-mm (GQI FIB)(OneDrive)](https://pitt-my.sharepoint.com/:f:/g/personal/yehfc_pitt_edu/EvFAkXbKPjVCjuTuWcuyGyYBZRAUi4ytmwi9jDI1kFtguA?e=8p3AdS)
  - [native-space 2-mm (GQI FIB)(Zenodo)](https://zenodo.org/record/6307812)
  - [MNI-space 1.25-mm (QSDR FIB)(OneDrive)](https://pitt-my.sharepoint.com/:f:/g/personal/yehfc_pitt_edu/EqdBttDkWOREjqlB3Ql1KVkBgAueXUbqIdJWi1RpHSEiyg?e=bDcFTe)

<div style="left: 0; width: 100%; height: 400px; position: relative;"><iframe src="https://drive.google.com/embeddedfolderview?id=1UoJiTX24xJNxFM6AwnJtIda6MdlWeQyv#list" style="top: 0; left: 0; width: 100%; height: 100%; position: absolute; border: 0;" allowfullscreen></iframe></div>

- [SRC Files](https://pitt-my.sharepoint.com/:f:/g/personal/yehfc_pitt_edu/EmL_WkIkt3pFilc6MeqRoX0Bwhvs0Lr7X9LAoIucajLUwQ?e=c0w9xQ)

  The SRC files contains raw dMRI signals for modeling. They can be reconstructed to generate FIB files. The original NIFTI files can be downloaded from the HCP's connectome db website.
 
- [T1W](https://pitt-my.sharepoint.com/:f:/g/personal/yehfc_pitt_edu/EkPCanH2hTBEh47ZFHXIHuUBaYhGS5lcz3Hi1lAGoeqMcw?e=vCSidk)
- Demographics at <https://db.humanconnectome.org/>
- [Local connectome fingerprint](https://pitt-my.sharepoint.com/:f:/g/personal/yehfc_pitt_edu/Esw0yxBQM4pCtnjoRLm41kQBejzvhTd6p-XYcDCWMMIhyg?e=X1EKBL) [1]

   * LCF of all 930 subjects: HCP930_fp.mat
   * ID of the subjects: HCP930.QSDR25.db.fib.gz.name.txt
   * Squared difference of 930 subjects: HCP930.QSDR25.db.fib.gz.vec.dif.mat

  **Methods**
  > A group average template was constructed from a total of 930 subjects. A multishell diffusion scheme was used, and the b-values were 1000, 2000, and 3000 s/mm2. The number of diffusion sampling directions were 90, 90, and 90, respectively. The in-plane resolution was 1.25 mm. The slice thickness was 1.25 mm. The diffusion data were reconstructed in the MNI space using q-space diffeomorphic reconstruction (Yeh et al., Neuroimage, 58(1):91-9, 2011) to obtain the spin distribution function (Yeh et al., IEEE TMI, ;29(9):1626-35, 2010). A diffusion sampling length ratio of 2.5 was used, and the output resolution was 1 mm. The analysis was conducted using DSI Studio (http://dsi-studio.labsolver.org).

  [1] Yeh F-C, Vettel JM, Singh A, Poczos B, Grafton ST, Erickson KI, et al. (2016) Quantifying Differences and Similarities in Whole-Brain White Matter Architecture Using Local Connectome Fingerprints. PLoS Comput Biol 12(11): e1005203. https://doi.org/[10.1371/journal.pcbi.1005203](http://dx.doi.org/10.1371/journal.pcbi.1005203)


## MGH-USC 

This data set was originally from the connectome db website (https://db.humanconnectome.org/). The MGH HCP team has released diffusion imaging and structural imaging data acquired from 35 young adults using the customized MGH Siemens 3T Connectome scanner, which has 300 mT/m maximum gradient strength for diffusion imaging.

- [NIFTI files for DWI and T1W](https://pitt-my.sharepoint.com/:f:/g/personal/yehfc_pitt_edu/El5HHIaNyD1Hreo5hvZaCjcBjrbfyfiEUG22lvcPHYC_pA?e=wKkjEc)
- SRC files [(OneDrive)](https://pitt-my.sharepoint.com/:f:/g/personal/yehfc_pitt_edu/EiyOUXXxs01FljIc7J1AypABeY3imX_CLfkpPUbBVM0hGg?e=XqhbBt) [(Zenodo)](https://zenodo.org/record/6315871)

  **Methods**
  > A multishell diffusion scheme was used, and the b-values were 1000 ,3000 ,5000 and 10000 s/mm2. The number of diffusion sampling directions were 64, 64, 128, and 256. The in-plane resolution was 1.5 mm. The slice thickness was 1.5 mm.


