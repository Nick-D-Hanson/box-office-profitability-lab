# Box Office Profitability Lab

Exploring the factors associated with film profitability through large-scale data preparation, exploratory analysis, and comparative machine learning.

**Research question:** How well can historical movie metadata distinguish films whose reported box-office revenue exceeds their stated production budget?

> **Scope:** This is a retrospective classification study, not a validated pre-release box-office forecasting tool. Some features, including audience ratings and popularity, can reflect information only available after a movie's release.

## Data and methods

- **Sources:** [TMDb Movies Dataset on Kaggle](https://www.kaggle.com/datasets/asaniczka/tmdb-movies-dataset-2023-930k-movies), plus IMDb's [non-commercial datasets](https://developer.imdb.com/non-commercial-datasets/) for crew and name metadata.
- **Processing:** Python, Pandas, and PySpark for data cleaning, exploratory analysis, feature engineering, and joins.
- **Models explored:** random forest, logistic regression, and multilayer perceptron classification, alongside tuning and K-fold cross-validation experiments.
- **Segments:** comparisons between pre-2020 and 2020-onward movie releases.
- **Outcome:** a binary indicator based on whether reported revenue minus production budget is positive. This proxy does **not** account for marketing, distribution, or other financial costs.

## Research notebooks

| Notebook | Purpose |
|---|---|
| [Exploratory data analysis](Box_Office_Quants_EDA_7_17_24.ipynb) | Source ingestion, joins, cleaning, and preliminary profiling |
| [Initial models](Box_Office_Quants_FirstModel_7_24_24.ipynb) | First profitability classifiers and split-period comparisons |
| [Model tuning](Box_Office_Quants_InitialModelTuning_8_7_24.ipynb) | Extended experiments and alternative model configurations |
| [Final experimental analysis](Box_Office_Quants_FinalPresentationModels_8_21_24.ipynb) | Feature importance, cross-validation, and comparative results |

These notebooks preserve the original exploration and its intermediate outputs. They were prepared for a Colab/Spark environment and are **not yet a one-command reproducible pipeline**. Download the source datasets under their applicable terms and use your own local Kaggle configuration; never commit credentials.

## Interpretation and known limitations

1. The label represents **revenue greater than production budget**, not true accounting profitability.
2. Audience ratings, vote counts, and popularity can introduce hindsight if a model is described as predicting profitability *before release*. No such prospective claim is made here.
3. Random train/test splits and shared preprocessing from the original notebooks require stricter validation before reporting generalized performance.
4. Comparisons across COVID-era periods are exploratory associations, not causal estimates.

## Next engineering milestone

Rebuild the research into a tested pipeline with explicit **as-of-release feature availability**, chronological holdouts, leakage-safe transformations, a simple financial baseline, and calibrated evaluation. Publish a model card with verified performance and failure cases before offering predictions.

## Project origin

This work began as a collaborative graduate data-science capstone by the **Box Office Quants** team. The notebooks remain as historical research artifacts; this repository's presentation and future independent engineering iterations are being developed as an ongoing portfolio project. Individual contributions should be specified rather than attributed to one person by default.
