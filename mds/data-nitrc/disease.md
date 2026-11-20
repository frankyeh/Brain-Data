---
title: data-nitrc/disease
---

# data-nitrc/disease

**Repository description:** Clinical/disease human brain diffusion MRI datasets from NITRC distributed through the Fiber Data Hub (`data-nitrc/disease`).

## Access & Download

- **Quality control:** [QC results](/qc.html) · [Search datasets using the QC report](/qc_search.html)
- **Download instructions:** [Download guide](/download.html) — file formats (`*.fz`, `*.sz`, `*.dz`, `qc.tsv`), DSI Studio GUI integration, command-line (`bash` / PowerShell), and Python scripts
- **Secondary direct assets:** [GitHub Releases ↗](https://github.com/data-nitrc/disease/releases)

## Command-Line Listing

List available release tags in `data-nitrc/disease` via the GitHub API (see the [Download guide](/download.html) for batch download commands):

```bash
curl -s https://api.github.com/repos/data-nitrc/disease/releases | jq -r '.[].tag_name'
```
