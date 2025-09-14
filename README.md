# methylkit-workflow

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.17117988.svg)](https://doi.org/10.5281/zenodo.17117988)

A reproducible workflow for methylKit-based DNA methylation analysis. Loads sample metadata from an annotation master file, performs DMR/DMG computations, and generates publication-ready visualizations with ggplot2.

## Features

- Loads sample metadata from annotation files (Excel, CSV, TXT)
- Performs DMR (Differentially Methylated Regions) and DMG (Differentially Methylated Genes) analysis using methylKit
- Generates summary statistics and quality control reports (MultiQC)
- Exports results and generates publication-ready plots (ggplot2)
- Includes scripts for annotation, visualization, and downstream analysis
- Example annotation and result files included

## Getting Started

1. Clone the repository:
   ```
   git clone https://github.com/pgasperowicz/methylkit-workflow.git
   ```
2. Install required R packages using `install_project_libraries.R`.
3. Edit `config.yaml` to match your data and analysis settings.
4. Run the main workflow script: `methylkit_main.R`.

## Folder Structure

- `annotations/` – Sample metadata and annotation files
- `bismark_align/` – Bismark alignment and coverage files
- `methylkit_results/` – Output from methylKit analyses
- `multiqc_data/` – MultiQC reports and data
- `markdown/` – Documentation and markdown reports
- `*.R` – R scripts for each step of the workflow
- `config.yaml` – Main configuration file
- `CITATION.cff` and `zenodo.json` – Citation and metadata files

## Citing

If you use this workflow, please cite as described in `CITATION.cff` or the Zenodo record.

## Versioning

This project uses semantic versioning. To bump the version automatically across all files:

1. Install bump2version: `pip install bump2version`
2. Run one of the following commands:
   - `bump2version patch` (for bug fixes, e.g., 0.0.1-alpha → 0.0.2-alpha)
   - `bump2version minor` (for new features, e.g., 0.0.1-alpha → 0.1.0-alpha)
   - `bump2version major` (for breaking changes, e.g., 0.0.1-alpha → 1.0.0)
   - For custom versions: `bump2version --new-version 1.0.0 release`

This will update `CITATION.cff` and `zenodo.json`, commit the changes, and create a Git tag.

## License

MIT License
