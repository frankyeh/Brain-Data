# BigBrain Histology Images

![bigbrain](/images/BigBrain.png)

## Download

- [MNI space images in NIFTI files](https://pitt-my.sharepoint.com/:f:/g/personal/yehfc_pitt_edu/EpfUIKeDq0RHiayNGkt2kTEBwN_MsWerxfCxgHM2IWVe2Q?e=LdY3Nj)

## License

BigBrain data are shared by Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International Public License.

## Reference

Amunts, Katrin, Claude Lepage, Louis Borgeat, Hartmut Mohlberg, Timo Dickscheid, Marc-Étienne Rousseau, Sebastian Bludau et al. "BigBrain: an ultrahigh-resolution 3D human brain model." *Science* 340, no. 6139 (2013): 1472-1475.


# A unified 3D map of microscopic architecture and MRI of the human brain

<img src="https://github.com/frankyeh/Brain-Data/assets/275569/4cdd4ec7-0330-41dd-a5ba-d65b259432ed" width=500 />

## Reference

Alkemade A, Bazin PL, Balesar R, Pine K, Kirilina E, Möller HE, Trampel R, Kros JM, Keuken MC, Bleys RL, Swaab DF. A unified 3D map of microscopic architecture and MRI of the human brain. Science advances. 2022 Apr 27;8(17):eabj7892. ([link](https://www.science.org/doi/10.1126/sciadv.abj7892)https://www.science.org/doi/10.1126/sciadv.abj7892)

## Download

| Data | Description | DOI |
| --- | --- | --- |
| Original stains | Archive of .tiff files of the microscopy stains in full resolution and color, including transformation maps to 3D blockface space | [10.21942/uva.16844500](https://doi.org/10.21942/uva.16844500) |
| 3D reconstructions | 3D stacked images of the stains and MRI in ~200-μm-resolution space of the blockface image | [10.21942/uva.16834114](https://doi.org/10.21942/uva.16834114) |
| MNI coregistrations | Stains, blockface, and MRI data in MNI2009B space at 0.5-mm resolution | [10.21942/uva.16834186](https://doi.org/10.21942/uva.16834186) |
| Automated parcellations | Parcellation results from the whole brain, cortical surface, and subcortical labeling algorithms | [10.21942/uva.16834159](https://doi.org/10.21942/uva.16834159) |


# The Visible Human Project

![image](https://github.com/frankyeh/Brain-Data/assets/275569/d766d1f5-18d8-4dc0-b9c5-aa68df798eb5)

[NIH website](https://www.nlm.nih.gov/research/visible/visible_human.html)

The NLM Visible Human Project is a groundbreaking initiative that has produced detailed, three-dimensional representations of a human male and female body. This project, initiated by the National Library of Medicine (NLM), has provided a valuable resource for studying human anatomy, testing medical imaging algorithms, and constructing network-accessible image libraries. The Visible Human data sets, consisting of cross-sectional cryosection, CT, and MRI images obtained from a male and a female cadaver, were publicly released in 1994 and 1995, respectively. These data sets have been widely used in various fields, including education, diagnostics, treatment planning, virtual reality, art, mathematics, and industry. Initially accessible through a licensing system, the NLM made the VHP datasets freely available to the public in 2019. This remarkable project owes its success to the generosity of the individuals who selflessly willed their bodies to science, enabling the creation of these invaluable resources.

## Method

The Visible Human Male data set comprises MRI, CT, and anatomical images. Axial MRI images of the head and neck were obtained at 4mm intervals, while longitudinal sections of the rest of the body were captured as well. The MRI images have a resolution of 256 by 256 pixels, with each pixel representing 12 bits of gray tone. The CT data includes axial scans of the entire body taken at 1mm intervals, with a pixel resolution of 512 by 512 and 12 bits of gray tone per pixel. The anatomical images, measuring approximately 7.5 megabytes, are 2048 pixels by 1216 pixels in size, with each pixel corresponding to 0.33mm and defined by 24 bits of color. The anatomical cross-sections are aligned with the CT images at 1mm intervals, resulting in a total of 1,871 cross-sections for both CT and anatomical images. The complete male data set occupies approximately 15 gigabytes of storage.

## Download

| NIFTI | source | Note|
|------|-----|-----|
|T1W image (1x1x3mm resolution)| [NIH source (DICOM)](https://data.lhncbc.nlm.nih.gov/public/Visible-Human/Male-Images/Visible%20Human%202.0%20-%20Peter%20Ratiu/Seriel%20Head/MR_CT_DICOM/MRI/T1/index.html) | Pixel size:		0.9375 mm/pixel Slice thickness:	3 mm|
|T2W image (1mm isotropic)| [NIH source (DICOM)](https://data.lhncbc.nlm.nih.gov/public/Visible-Human/Male-Images/Visible%20Human%202.0%20-%20Peter%20Ratiu/Seriel%20Head/MR_CT_DICOM/MRI/T2_512/index.html)| Pixel size:		0.46875 mm/pixel 	Slice thickness:	1 mm |
|Crysections in NIFTI (1056x1528x1476xRGB) | [TIFF source](https://data.lhncbc.nlm.nih.gov/public/Visible-Human/Male-Images/Visible%20Human%202.0%20-%20Peter%20Ratiu/Seriel%20Head/cryo/Axial_tiff/index.html)| Pixel size:	0.147 mm 	Spacing:	0.147 mm |
