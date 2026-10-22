# Data notes

## Source

- Accession: [NCBI GEO GSE40279](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE40279).
- Study: Hannum et al. (2013), *Genome-wide methylation profiles reveal quantitative views of human aging rates*.
- Publication: https://doi.org/10.1016/j.molcel.2012.10.016
- Data type: processed whole-blood DNA methylation beta values and corresponding sample metadata, including chronological age.
- Study size: 656 samples measured on the Illumina HumanMethylation450 platform. The analysis sample count will be documented after matching and quality checks.

## Planned local storage

Create these directories when data acquisition begins:

```text
data/raw/         Original downloaded data and sample metadata
data/interim/     Temporary transformations
data/processed/   Matched and processed analysis matrices
```

All content under `data/` except this README is ignored by Git. Keep participant-level data and metadata local. Record download URLs, retrieval dates, checksums, preprocessing choices, exclusions, and final sample counts when implementing the analysis.

Use the processed beta-value matrix rather than raw intensity files for the initial project scope. Match samples by accession identifiers, not column order. Keep the held-out test set separate before fitting any learned preprocessing or age-based feature selection.

No dataset has been downloaded or analyzed in this repository yet.
