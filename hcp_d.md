# Introduction

The[ Lifespan Human Connectome Project Development (HCP-D) Study](https://www.humanconnectome.org/study/hcp-lifespan-development) planned to enroll 1,300+ healthy children, adolescents, and young adults (ages 5-21). The purpose is to discover how different parts of a child's brain are connected and how these connections (the "connectome") change as the brain develops.

# License

The [NDA ](https://nda.nih.gov/) agreement prohibits me from sharing raw MRI data (e.g. T1W, DWI, and SRC.GZ files) and demographics. After discussion with the NDA program lead, I am allowed to share the "derived" data, including the anisotropy, diffusivities, local fiber orientations, and tractography. This includes the FIB file and the tractography. For other data, you may request access at [NDA](https://nda.nih.gov/).

The FIB files and tractography files are shared using [Creative Commons Attribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/).  For those using FIB and tractography files, I would appreciate your mentioning of the contribution of XSEDE resources: TG-CIS200026.

# Download

- [FIB files](https://pitt-my.sharepoint.com/:f:/g/personal/yehfc_pitt_edu/Esgw2vN45mNJu3gYi2hjqrYBbFTDry10x8KX4u3kmYmjTQ?e=T8PoKA)

  **Methods**
  > A multishell diffusion scheme was used, and the b-values were 1500 and 3000 s/mm². The number of diffusion sampling directions was 93 and 92, respectively. The in-plane resolution was 1.5 mm. The slice thickness was 1.5 mm. The susceptibility artifact was estimated using reversed phase-encoding b0 by TOPUP from the Tiny FSL package (http://github.com/frankyeh/TinyFSL), a re-compilied version of FSL TOPUP (FMRIB, Oxford) with multi-thread support. The correction was conducted through the integrated interface in DSI Studio's ("Chen" release). The diffusion MRI data were rotated to align with the AC-PC line. The accuracy of b-table orientation was examined by comparing fiber orientations with those of a population-averaged template (Yeh et al. Neuroimage, 2018). The restricted diffusion was quantified using restricted diffusion imaging (Yeh et al., MRM, 77:603--612 (2017)). The diffusion data were reconstructed using generalized q-sampling imaging (Yeh et al., IEEE TMI, ;29(9):1626-35, 2010) with a diffusion sampling length ratio of 1.25. The tensor metrics were calculated. The analysis was conducted using the resource allocation (TG-CIS200026) at Extreme Science and Engineering Discovery Environment (XSEDE) resources (Towns, J. et al. Computing in science & engineering 16, 62-74  2014).