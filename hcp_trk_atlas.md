
# HCP Population-Based Tractography Atlases

![image](https://user-images.githubusercontent.com/275569/150540941-9e69f578-29a8-480f-939e-080d6701c0e2.png)

The population-based tractography atlases were constructed using [HCP-YA](/hcp-ya.html) data. The first version was a population-averaged atlas [(Yeh, 2018)](https://www.ncbi.nlm.nih.gov/pubmed/29758339), whereas the more recent version was a population-based atlas [(Yeh 2021)](https://www.researchsquare.com/article/rs-1083262/v1) using [DSI Studio's automatic fiber tracking](https://dsi-studio.labsolver.org/doc/gui_t3_atk.html)

***Population-based atlas***

Yeh, F. C. (2021) Population-Based Tract-To-Region Connectome of the Human Brain and Its Hierarchical Topology, preprint DOI: 10.21203/rs.3.rs-1083262/v1

***Population-averaged atlas***

Yeh FC, Panesar S, Fernandes D, Meola A, Yoshino M, Fernandez-Miranda JC, Vettel JM, Verstynen T. Population-averaged atlas of the macroscale human structural connectome and its network topology. Neuroimage. 2018 Sep 1;178:57-68. PubMed: https://www.ncbi.nlm.nih.gov/pubmed/29758339

# License

This atlas is shared under the [Creative Commons Attribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/).

The atlases are derived data from the Human Connectome Project. Using them requires additional [acknowledgment](https://www.humanconnectome.org/study/hcp-young-adult/document/wu-minn-hcp-consortium-open-access-data-use-terms).

# Download

## HCP1065 tractography database, probabilistic atlas, and tract-to-region connectome

<img src="https://user-images.githubusercontent.com/275569/149355373-399832bb-7a83-486d-ba89-71910a0af9df.png" width="400">

>  Yeh, F. C. (2021) Population-Based Tract-To-Region Connectome of the Human Brain and Its Hierarchical Topology, preprint DOI: 10.21203/rs.3.rs-1083262/v1 

- Probabilistic tractography atlas of white matter pathways [(64 NIFTI files)](https://pitt-my.sharepoint.com/:f:/g/personal/yehfc_pitt_edu/EvhbI5gALiZGvZATK1D8cyUBsH4J_CeRjHw-nJq4fIzoCg?e=dK0y5U) [TIF pictures](https://pitt-my.sharepoint.com/:f:/g/personal/yehfc_pitt_edu/El7FAwrE-9dMj4MGXVmcL5cBpCB5VpvuzoAc7DYyE8AzKg?e=GTGG6F)

  Automatic fiber tracking and augmented fiber tracking (Yeh 2020) were used to map white matter pathways in HCP young adult subjects. These NIFTI volumes record the population probability of each white matter tract aggregated from the tractography of 1065 subjects.

 
- Tractography of 1065 subjects in ICBM152 space [(~1065x64 NIFTI files)](https://pitt-my.sharepoint.com/:f:/g/personal/yehfc_pitt_edu/EhEovDmdDhpEl1s6OhK69ckBBBE7FoXH1psecjDWkqxloA?e=ngchRU) [(TT files)]

  Automatic fiber tracking and augmented fiber tracking (Yeh 2020) was applied to each of the HCP 1065 subjects data to map 64 white matter pathways.
   
  'all_files.zip' contains all NIFTI files.

- Tract-to-region connectome (EXCEL files): 

  Tract-to-region connectome was derived using HCP-MMP, Brodmann, and Kleist atlas.

  - [HCP-MMP parcellation](https://pitt-my.sharepoint.com/:x:/g/personal/yehfc_pitt_edu/Eb-yhDcnGBJHlhED2xAI8YwBJvQu8IqyRQ1L9v-dZkM7wQ?e=aitB08)

  - [BM/KL parcellation](https://pitt-my.sharepoint.com/:x:/g/personal/yehfc_pitt_edu/EVG6NflPIbtIpc3jvruyf7cB2ZegmiAWPgQkHDJKakfQZg?e=awH0LB)

- [Abbreviations](https://pitt-my.sharepoint.com/:x:/g/personal/yehfc_pitt_edu/ETZFzeNe8D5Dul7OYZHj_W4B5xBKgihpgz4C70Knv7YpKQ?e=7j4pwO)


## HCP1065 tractography atlas 

> Yeh FC, Panesar S, Fernandes D, Meola A, Yoshino M, Fernandez-Miranda JC, Vettel JM, Verstynen T. Population-averaged atlas of the macroscale human structural connectome and its network topology. Neuroimage. 2018 Sep 1;178:57-68. (2021 update)

HCP1065 atlas is an updated atlas from HCP842 atlas. The new atlas is baes on "ICBM 2009a Nonlinear Asymmetric" (<https://www.bic.mni.mcgill.ca/ServicesAtlases/ICBM152NLin2009>) space, whereas HCP842 is based on FSL's FA map ( 58 FA images averaged to old MNI152). The new atlas further provides subcomponents for cingulum, SLF, corticopontine track, corticostriatal track, corticothalamic track (renamed as thalamic radiation). Since the atlas is transformed or derived from HCP842, please cite the original HCP842 atlas paper (Yeh, 2018), and mentioned an updated version is used to get tracks in the ICBM152 nonlinear space.


To view these tract files, please download the HCP-1065 template fib file and open it in DSI Studio at [Step T3 Fiber Tracking]. The *.tt.gz files can be loaded using [Tracts][Open Tracts]. The ICBM152 images can be loaded using [Edit][Insert T1W/T2W].

- [Population-averaged tractography atlas (TT)](https://pitt-my.sharepoint.com/:f:/g/personal/yehfc_pitt_edu/EjD1HZDMSnVGuuXm_B5vczQBuvY8WFjtHQR-AnXQc6izvQ?e=JIOLDz)

- [Population-averaged tractography atlas (TRK)](https://pitt-my.sharepoint.com/:f:/g/personal/yehfc_pitt_edu/Ek0DdO67iQ9NvkJUci91lzMBXCVBq926QXTTY7JK6LIjgw?e=jvydcC)

- [Population-averaged tractography atlas (NIFTI)](https://pitt-my.sharepoint.com/:f:/g/personal/yehfc_pitt_edu/EvAcb1QyogFPg206v-FRl2gB6EcDf3TIPG37JyugoL3hdA?e=SuGBZ4)

- [Abbreviation list](https://pitt-my.sharepoint.com/:x:/g/personal/yehfc_pitt_edu/EQcjg3Ignv5CpOlwRu-dc-sBFy790zDaA2zW0qtR19VbJA?e=3iA6Ey) 

## HCP842 tractography atlas

<img src="https://user-images.githubusercontent.com/275569/149355618-5299fdf9-3d6e-4cfc-a434-96794f838052.png" width="400">

> Yeh FC, Panesar S, Fernandes D, Meola A, Yoshino M, Fernandez-Miranda JC, Vettel JM, Verstynen T. Population-averaged atlas of the macroscale human structural connectome and its network topology. Neuroimage. 2018 Sep 1;178:57-68. (original data)

 HCP842 tractography atlas uses FSL's FA map as its reference space (<https://fsl.fmrib.ox.ac.uk/fsl/fslwiki/Atlases>), which averages from 58 FA images in the MNI152 coordinate. 

- [Population-averaged tractography (NIFTI)](https://zenodo.org/record/3627772#.Xi0q02hKiUk) 

- [Population-averaged tractography (TRK)](https://pitt-my.sharepoint.com/:f:/g/personal/yehfc_pitt_edu/EvV49cgSEWpFmJOwtRO28moB7b_yXTDUIx5lnP0opd-waA?e=6w2v4J)

- [Population-averaged tractography (JPG)](https://pitt-my.sharepoint.com/:f:/g/personal/yehfc_pitt_edu/ErvN3WnoP7FHlJjinNVNq3IB753wSm4QGvHgzMACOURP8Q?e=VmySKx)

- [Connectivity matrix (EXCEL) and connectograms in (PNG)](https://pitt-my.sharepoint.com/:f:/g/personal/yehfc_pitt_edu/EmzLbtr_IA9LrKMCfC1aC6cB_ag6Ivwj8DJA5o71_kHm9w?e=QYnZVK)

- [Abbreviation list](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6921501/bin/NIHMS1062874-supplement-1.pdf)

