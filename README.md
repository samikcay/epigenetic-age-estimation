# Human Age Estimation from DNA Methylation Profiles

Bioinformatics term project proposal: **Human Age Estimation from DNA Methylation Profiles Using Feature Selection and Regression Models**.

## Current status

Proposal and repository setup. Data acquisition, implementation, model training, and evaluation are planned work; no experimental results are claimed.

The four submission fields, work allocation, and references are available in [the project proposal](docs/project-proposal.md).

## Research objective

Estimate chronological age from blood DNA methylation profiles and measure the trade-off between prediction error and the number of CpG sites used. Compare Elastic Net and Random Forest regression against a mean-age baseline.

## Planned analysis

1. Obtain the processed methylation measurements and sample age metadata for GEO GSE40279.
2. Match sample identifiers, check data quality, and create a reproducible 80/20 training/test split.
3. Evaluate feature subsets of 10, 25, 50, 100, and 500 CpG sites using five-fold cross-validation within the training set. Feature counts are planned experimental settings, not reported findings.
4. Fit missing-value handling, feature selection, and any scaling inside each training fold. Use the same validation splits for all model comparisons. Keep the test set outside feature-count and hyperparameter selection.
5. Report held-out mean absolute error (MAE, years), root mean squared error (RMSE, years), and R-squared. Compare these results with the mean-age baseline and inspect errors across age ranges.
6. Summarize prediction error versus feature count, selected-feature stability across folds, and study limitations.

The training/validation distinction is important because the number of methylation features is much larger than the number of participants. The project evaluates chronological-age prediction within a blood dataset; its planned analysis does not establish clinical utility or performance in other tissues or populations.

## Repository layout

```text
.
|-- .gitattributes
|-- .gitignore
|-- README.md
|-- data/
|   `-- README.md
`-- docs/
    `-- project-proposal.md
```

## Data and generated files

See [the data notes](data/README.md) for the verified dataset source and intended local storage. Dataset downloads, participant-level metadata, processed data, trained models, environments, caches, and generated experiment outputs are excluded by `.gitignore`. Small, deliberately prepared summary figures and tables may later be committed under `docs/`.

## Planned tools

Python, pandas, NumPy, scikit-learn, and Matplotlib. Dependencies will be pinned when the executable analysis is implemented and validated.

## References

- Hannum et al. (2013), [Genome-wide methylation profiles reveal quantitative views of human aging rates](https://doi.org/10.1016/j.molcel.2012.10.016).
- NCBI GEO, [GSE40279](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE40279).
- scikit-learn, [Feature selection](https://scikit-learn.org/stable/modules/feature_selection.html) and [preventing data leakage](https://scikit-learn.org/stable/common_pitfalls.html#data-leakage).
