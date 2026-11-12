---
layout: home
---

<img src="https://github.com/frankyeh/FiberDataHub/releases/download/qc-chart/qc_counts_combined.png" width="100%"/>

> Yeh, Fang-Cheng. “DSI Studio: An Integrated Tractography Platform and Fiber Data Hub for Accelerating Brain Research.” Nature Methods, July 2025, https://doi.org/10.1038/s41592-025-02762-8.
> 
> Reference: [pdf](https://rdcu.be/exECv), [pubmed](https://pubmed.ncbi.nlm.nih.gov/40707713/)


The **Fiber Data Hub** is a cloud-based platform for openly sharing processed **fiber data** derived from diffusion MRI, built to support scalable and reproducible research in brain connectivity. The Hub currently hosts more than **30,000** fiber datasets (Nature Methods, 2025), each derived from an underlying DWI scan, from major neuroimaging initiatives including OpenNeuro and the International Neuroimaging Data-sharing Initiative (INDI).

Instead of redistributing full raw DWI, the Hub provides compact, standardized **fiber data**—the minimal information needed to run fiber tracking—such as fiber orientation, anisotropy, diffusivities, and other diffusion-derived metrics. A key advantage is size: these derivatives are typically ~50–100× smaller than the original DWI. For example, a compressed HCP DWI dataset is about ~500 MB per subject, while the corresponding **fiber data** at the same resolution is usually ~5–10 MB, making large-scale distribution and access far more practical.

By consolidating curated, preprocessed datasets in a consistent format, the **Fiber Data Hub** reduces computational burden, streamlines analysis workflows, and avoids redundant preprocessing across labs. Researchers can explore the collection through an intuitive web interface with metadata-driven search and built-in quality control, enabling efficient discovery, collaboration, and reliable reuse across studies of neurodevelopment, neurological disorders, and population-level brain organization.


## Repository List

**If you would like to suggest a dataset, please feel free to reach out to me (frank.yeh@gmail.com). We will preprocess the data and distribute them**

- [data-hcp/lifespan](https://github.com/data-hcp/lifespan/releases)
- [data-hcp/disease](https://github.com/data-hcp/disease/releases)
- [data-nih/tcia (brain tumors)](https://github.com/data-nih/tcia/releases)
- [data-openneuro/brain (<ds005000)](https://github.com/data-openneuro/brain/releases) 
- [data-openneuro/brain2 (>ds005000)](https://github.com/data-openneuro/brain2/releases)
- [data-openneuro/disease (<ds005000)](https://github.com/data-openneuro/disease/releases)
- [data-openneuro/disease2 (>ds005000)](https://github.com/data-openneuro/disease2/releases)
- [data-openneuro/animal](https://github.com/data-openneuro/animal/releases)
- [data-openneuro/others (ex-vivo, phantom)](https://github.com/data-openneuro/others/releases)
- [data-indi/brain](https://github.com/data-indi/brain/releases)
- [data-indi/disease](https://github.com/data-indi/disease/releases)
- [data-indi/animal](https://github.com/data-indi/animal/releases)
- [data-dandi/brain](https://github.com/data-dandi/brain/releases)
- [data-dandi/animal](https://github.com/data-dandi/animal/releases)
- [data-others/brain (before 2020)](https://github.com/data-others/brain/releases)
- [data-others/brain2 (after 2020)](https://github.com/data-others/brain2/releases)
- [data-others/disease](https://github.com/data-others/disease/releases)
- [data-others/animal](https://github.com/data-others/animal/releases)
- [data-others/atlas](https://github.com/data-others/atlas/releases)

---

Download instructions, file formats and Python examples are in the [download guide](/download.html).
