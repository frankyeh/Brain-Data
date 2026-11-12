---
title: data-dandi/brain
---

# data-dandi/brain

**Repository description:** Human brain data distributed through the Fiber Data Hub (`data-dandi/brain`).

## Access & Download

- **Quality control:** [QC results](/qc.html) · [Search datasets using the QC report](/qc_search.html)
- **Download instructions:** [Download guide](/download.html) — file formats (`*.fz`, `*.sz`, `*.dz`, `qc.tsv`), DSI Studio GUI integration, command-line (`bash` / PowerShell), and Python scripts
- **Secondary direct assets:** [GitHub Releases ↗](https://github.com/data-dandi/brain/releases)

## Command-Line Listing

List available release tags in `data-dandi/brain` via the GitHub API (see the [Download guide](/download.html) for batch download commands):

```bash
curl -s https://api.github.com/repos/data-dandi/brain/releases | jq -r '.[].tag_name'
```
