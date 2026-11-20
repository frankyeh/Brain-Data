---
title: data-nitrc/brain
---

# data-nitrc/brain

**Repository description:** Healthy human brain diffusion MRI datasets from NITRC distributed through the Fiber Data Hub (`data-nitrc/brain`).

## Access & Download

- **Quality control:** [QC results](/qc.html) · [Search datasets using the QC report](/qc_search.html)
- **Download instructions:** [Download guide](/download.html) — file formats (`*.fz`, `*.sz`, `*.dz`, `qc.tsv`), DSI Studio GUI integration, command-line (`bash` / PowerShell), and Python scripts
- **Secondary direct assets:** [GitHub Releases ↗](https://github.com/data-nitrc/brain/releases)

## Command-Line Listing

List available release tags in `data-nitrc/brain` via the GitHub API (see the [Download guide](/download.html) for batch download commands):

```bash
curl -s https://api.github.com/repos/data-nitrc/brain/releases | jq -r '.[].tag_name'
```
