# Fiber Data Hub Agent Guide

This repository serves **https://brain.labsolver.org**, the web portal for the Fiber Data Hub.

AI agents may access Fiber Data Hub data through **either of two supported routes**:

1. **Direct web/GitHub access**
2. **DSI Studio Fiber Data Hub commands**

Both routes are valid. Choose the route that best fits the task and the tools currently available. Do not require DSI Studio when ordinary web/GitHub access is sufficient, and do not reimplement DSI Studio analysis when DSI Studio is available and already provides the operation.

## Route 1: Direct web/GitHub access

Use this route for dataset discovery, release metadata, QC lookup, file listing, downloading public files, or external Python workflows.

### Entry points

- Fiber Data Hub portal: https://brain.labsolver.org
- File-format documentation: https://dsi-studio.labsolver.org/doc/cli_data.html
- Central QC release: https://github.com/frankyeh/FiberDataHub/releases/tag/qc-data

Public Fiber Data Hub data are distributed primarily as GitHub release assets in repositories under organizations including:

- `data-hcp`
- `data-nih`
- `data-openneuro`
- `data-indi`
- `data-dandi`
- `data-others`

The current repository list is maintained on https://brain.labsolver.org. Use the portal rather than assuming the list above is exhaustive.

### Discover repositories and datasets

A dataset is normally addressed as:

```text
owner/repository/tag
```

Examples:

```text
data-hcp/lifespan/hcp-ya
data-openneuro/brain/ds004299
```

GitHub API examples:

```text
https://api.github.com/users/{owner}/repos
https://api.github.com/repos/{owner}/{repository}/releases
https://api.github.com/repos/{owner}/{repository}/releases/tags/{tag}
```

The release-tag response contains an `assets` array. Use each asset's `name`, `size`, and `browser_download_url` to inspect or download files.

### Search QC data

Centralized QC tables are release assets at:

```text
https://api.github.com/repos/frankyeh/FiberDataHub/releases/tags/qc-data
```

Select TSV assets matching the requested owner/repository/dataset, download them using `browser_download_url`, and search the table contents. The Fiber Data Hub homepage contains a current Python example.

### File formats

Common Fiber Data Hub files include:

- `*.fz` — fiber orientation and diffusion-derived metrics
- `*.sz` — diffusion MRI volumes and b-table after preprocessing
- `*.dz` — group/connectometry database data
- `*.tsv` — metadata or QC tables

For direct programmatic reading or conversion of DSI Studio formats, follow:

https://dsi-studio.labsolver.org/doc/cli_data.html

Use the documented format rather than guessing the binary layout.

## Route 2: DSI Studio Fiber Data Hub commands

Use this route when DSI Studio is available and the task benefits from its built-in Hub integration, local GUI/session context, opening downloaded data, visualization, tractography, or subsequent DSI Studio analysis. It may also be useful when direct public access is insufficient for the requested dataset.

Current Fiber Data Hub commands are:

```text
hub_repo
hub_tags <repo>
hub_files <repo> [tag] [text] [offset] [limit]
hub_open <repo> <tag> <file>
hub_show <repo> <tag> [file]
hub_download <repo> [tag] <file> <dir>
```

Here `<repo>` is normally `owner/repository`.

For `hub_files`, empty tag/text values mean match all; tag and text may be regular expressions. For `hub_download`, `<file>` is a wildcard pattern such as `*.qsdr.fz` and may match multiple files.

When using DSI Studio through an AI-agent connection, invoke these commands through the DSI Studio command interface provided by that session. Do not substitute web scraping if the requested operation specifically requires opening or analyzing the data inside DSI Studio.

## Choosing a route

Choose based on the requested result rather than a fixed preference:

- **Dataset/repository discovery**: either route
- **List tags or files**: either route
- **Inspect GitHub release metadata**: direct web/GitHub is natural
- **Search QC TSV data**: direct web/GitHub is natural; DSI Studio is also valid when useful
- **Download public assets**: either route
- **Read/convert documented file contents in Python**: direct route is valid
- **Open a dataset in DSI Studio**: DSI Studio route
- **Tractography, ROI operations, visualization, tract statistics, connectometry, or other DSI Studio analysis**: DSI Studio route

If one route fails or is unavailable, try the other when it can satisfy the same request.

## Data-use rules

Fiber Data Hub derivatives originate from multiple source datasets with different licenses and data-use requirements.

- Follow the dataset-specific documentation and license.
- Do not infer that public availability of a derivative grants access to restricted original data or phenotypes.
- Do not bypass authentication or access controls.
- Cite the original dataset and required source publications/portals.
- When applicable, cite the Fiber Data Hub / DSI Studio resource described on the dataset page.

## Ground truth

For current dataset availability, metadata, download links, licensing notes, and citations, use the live Fiber Data Hub pages and corresponding GitHub releases. Do not rely on a hard-coded dataset count or an old cached repository list when live information is available.
