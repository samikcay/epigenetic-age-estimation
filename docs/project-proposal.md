# PROJECT TOPIC (TITLE)

Human Age Estimation from DNA Methylation Profiles Using Feature Selection and Regression Models

# PROJECT CONTENT - SUMMARY

This project will investigate how accurately human chronological age can be estimated from DNA methylation profiles and how prediction performance changes when fewer CpG sites are used. Processed whole-blood methylation data and age metadata from the public GEO dataset GSE40279 will be analyzed. The study will compare Elastic Net and Random Forest regression against a mean-age baseline using several feature subset sizes. Missing-value handling, scaling where appropriate, and feature selection will be fitted within the training folds to prevent data leakage. Model and feature-count selection will use cross-validation on the training set, followed by a final evaluation on an untouched test set. Performance will be reported using mean absolute error in years, root mean squared error, and R-squared. Expected outputs include a reproducible Python analysis, a comparison of prediction error versus feature count, and an assessment of the stability of selected CpG sites across validation folds.

# PROJECT TASK DISTRIBUTION/ALLOCATION

Responsibilities are organized by work package, with the following planned workload allocation:

| Work package | Allocation | Main responsibilities and deliverables |
| --- | --- | --- |
| Literature review and data acquisition | 15% | Review methylation-based age estimation; retrieve GSE40279 processed data and sample age metadata; document provenance and sample matching. |
| Data preparation and exploratory analysis | 20% | Check missing values, duplicated samples, and age distributions; define a reproducible training/test split and preprocessing pipeline. |
| Feature selection and model development | 30% | Implement feature selection, Elastic Net regression, Random Forest regression, and a mean-age baseline; compare feature subset sizes within training cross-validation. |
| Evaluation and interpretation | 20% | Evaluate final models on the held-out test set; report MAE, RMSE, and R-squared; analyze residuals by age range and CpG selection stability. |
| Documentation and presentation | 15% | Maintain the repository and analysis instructions; prepare figures, the final report, and the project presentation. |

# SOURCES/REFERENCES

1. Hannum, G., et al. (2013). Genome-wide methylation profiles reveal quantitative views of human aging rates. *Molecular Cell, 49*(2), 359-367. https://doi.org/10.1016/j.molcel.2012.10.016
2. NCBI Gene Expression Omnibus. *GSE40279: Genome-wide Methylation Profiles Reveal Quantitative Views of Human Aging Rates.* https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE40279
3. scikit-learn developers. *Feature selection.* https://scikit-learn.org/stable/modules/feature_selection.html
4. scikit-learn developers. *Common pitfalls and recommended practices: Data leakage.* https://scikit-learn.org/stable/common_pitfalls.html#data-leakage
