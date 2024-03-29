# Diffusion MRI and Tractography Datasets

This website is dedicated to redistributing diffusion MRI and tractography data to facilitate brain research. The shared datasets include population-based templates and pre-processed brain scans.

# What is diffusion MRI?

![diffusion mri](/images/pone.0075747.g004.jpg)

Recently diffusion MRI has arisen as the only non-invasive way to map white matter bundles and assess their structural integrity in the human brain. With fast imaging sequences, diffusion MRI, particularly its high angular resolution variants, can be acquired on standard clinical scanners. This advancement has gained considerable interest because of its role in mapping human connectome and its potential for accessing neuropsychological disorders. A large-scale analysis of diffusion MRI can explore its promising applications in biomedical research as an imaging biomarker of neuropathology. Principled approaches are to be adapted to understanding the structural characteristics of white matter bundles, resolving their associations with measures of cognition, and developing accurate diagnostic/prognostic models that predict neuropsychological disorders.

# What is diffusion MRI fiber tracking?

![connectivity](/images/pone.0080713.g014.png)

Diffusion MRI fiber tracking is a simulated approach that follows the fiber orientation at each imaging voxel to delineate the entire fiber trajectory in the brain tissue. It starts with a "seed" point and propagates along with local fiber directions in a recursive, step-by-step process until the termination criteria are met. The criteria may include an angular threshold, an anisotropy threshold, or an anatomical prior. Fiber tracking using data from the Human Connectome Project has been conducted to elucidate the complex anatomy of the brain pathways. Doctors and scientists investigated the intrinsic structure of the brain with unprecedented detail, which will invariably facilitate a better understanding of brain functioning. Studies using this technique have contributed to elucidate the structure, connectivity, and potential functional role of the major fiber pathways

# How can we use diffusion MRI and tractography?

![connectivity](/images/connectivity.png)

source: https://www.nature.com/articles/s41467-022-32595-4

The diffusion MRI and its derived tractography can be used to reveal the local organization of white matter pathways that are highly specific to individuals. The specific cognitive and personality characteristics that define an individual are encoded by the unique pattern of connections between the billions of neurons in the brain. This complex wiring system, termed the connectome, reflects the necessary connective architecture for the neural dynamics that give rise to nearly all cognitive functions. 

# What tool can I use to process diffusion MRI?

![connectivity](/images/dsistudio.jpg)

All data shared on this website can be analyzed by [DSI Studio](http://dsi-studio.labsolver.org). DSI Studio is a tractography software tool that maps brain connections and correlates findings with neuropsychological disorders. It is a collective implementation of several diffusion MRI methods, including diffusion tensor imaging (DTI), generalized q-sampling imaging (GQI), q-space diffeomorphic reconstruction (QSDR), diffusion MRI connectometry, and generalized deterministic fiber tracking.
