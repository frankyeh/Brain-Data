# **The Danish Research Centre for Magnetic Resonance (DRCMR) Data**
source: https://www.drcmr.dk/axon-morphology-dataset

This dataset was used to extract and analyze the 3D morphologies of axons, against the backdrop of the complex white matter environment, including axons, cells, blood vessels and vacuoles.

## Agreement 
Please make sure to cite the following:

```
XNH data and methods: M. Andersson et al. Axon morphology is modulated by the local environment and impacts the noninvasive investigation of its structure–function relationship. Proceedings of the National Academy of Sciences, 202012533 (2020). DOI: 10.1073/pnas.2012533117

MRI data and methods: T. B. Dyrby, L. V. Sogaard, M. G. Hall, M. Ptito, D. C. Alexander, Contrast and stability of the axon diameter index from microstructure imaging with diffusion MRI. Magn. Reson. Med. 70, 711–721 (2013).
```

## Data

The data can be downloaded from here:

https://resources.drcmr.dk/DIGdata/MAX4Img_AxonMorphology/

The data package includes synchrotron X-ray Nano-Holotomography (XNH) volumes from a sample taken from the splenium of a 32-month old vervet monkey, as well as the corresponding segmentations of axons, cell clusters, blood vessels and vacuoles, as presented in [preliminary Andersson et al. 2020]. Additionally, we share the diffusion MRI datasets of the same brain, including the whole-brain diffusion MRI and mid-sagittal region on which tractography and ActiveAx axon diameter fitting were performed.

In the different directories, the user will find "*_INFO.txt" files further explaining the data and its details.

The data package is divided into two main sections: “Diffusion MRI datasets” and “XNH datasets”.

The XNH volumes are available in two versions – full resolution and a convenience format. The latter version is processed, downsampled and stored in NIfTI format (.nii) to keep data sizes manageable and easily accessible in standard medical viewers.

## Diffusion MRI datasets

This directory includes the sub-directories:

1) "axonDiameterFitting"

Contains the diffusion MRI sub-volumes used for axon diameter fitting in the vervet monkey corpus callosum, and the respective Stesjal-Tanner scheme files.

2) "tractography"

Contains the diffusion MRI volume used for tractography of the interhemispheric V1 connection in the vervet monkey brain, and the Stejskal-Tanner scheme file.

The diffusion MRI data is presented and described in "Orientationally Invariant Indices of Axon Diameter and Density from Diffusion MRI" Alexander et al. (2010) and "Contrast and Stability of the Axon Diameter Index from Microstructure Imaging with Diffusion MRI" Dyrby et al. (2013).

“XNH datasets”

This directory contains the following sub-directories:

1) "axonSegmentations"

This directory contains X-ray Nano-Holotomography volumes of the monkey brain splenium, (referred to as "region 1" or "R1" in the context of other volumes included in this data package), and the segmentations of 54 axons from that volume.

2) "extraAxonalStructures_OverlappingRegions"

This directory contains X-ray Nano-Holotomography volumes of four overlapping regions of the monkey brain splenium, and the segmentation of cell clusters, blood vessels and vacuoles from the "extended" volume.

## Methods
Further details can be found in the "Methods" section of the article. In case of questions, please contact one of the corresponding authors, and we will be happy to assist you.

## Corresponding authors
Mariam Andersson and Tim B. Dyrby

## Funding
The Capital Region Research Foundation and the Swedish Research Council.

## Release Link
https://github.com/data-others/animal/releases/tag/drcmr
