---
title: data-dandi/animal
---

# data-dandi/animal

**Repository description:** Animal brain data from DANDI distributed through the Fiber Data Hub (`data-dandi/animal`).

## Access & Download

- **Quality control:** [QC results](/qc.html) · [Search datasets using the QC report](/qc_search.html)
- **Download instructions:** [Download guide](/download.html) — file formats (`*.fz`, `*.sz`, `*.dz`, `qc.tsv`), DSI Studio GUI integration, command-line (`bash` / PowerShell), and Python scripts
- **Secondary direct assets:** [GitHub Releases ↗](https://github.com/data-dandi/animal/releases)

## Command-Line Listing

List available release tags in `data-dandi/animal` via the GitHub API (see the [Download guide](/download.html) for batch download commands):

```bash
curl -s https://api.github.com/repos/data-dandi/animal/releases | jq -r '.[].tag_name'
```
