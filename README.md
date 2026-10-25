# Box Office Profitability Lab

**What makes a film commercially successful—and which signals are genuinely useful?**

A collaborative applied data-science study of historical film performance using large-scale data preparation, exploratory analysis, and machine learning. The work examines whether publicly reported movie attributes distinguish releases whose box-office revenue exceeds their production budgets.

**Project type:** Historical research | **Stack:** Python, Pandas, PySpark, scikit-learn | **Origin:** Box Office Quants graduate capstone

## The business question

Film decisions combine uncertainty about audience demand, production investment, and market conditions. This project explores associations between available movie attributes and a simple financial outcome: **reported revenue greater than production budget**.

That is **not** net profit: marketing, distribution, and other costs are outside the label. This is also **not yet a pre-release forecasting product**—some analyzed signals are observed after release.

## What the team built

- Joined and cleaned movie metadata and IMDb credits using Python, Pandas, and PySpark.
- Profiled distributions, missingness, and patterns across historical releases.
- Explored random forests, logistic regression, and multilayer perceptron classifiers.
- Compared model behavior across releases before 2020 and from 2020 onward.
- Documented where retrospective classification differs from a useful prospective prediction.

## Explore the analysis

| Notebook | What you will find |
|---|---|
| [Explore the dataset](Box_Office_Quants_EDA_7_17_24.ipynb) | Ingestion, joining, cleaning, and profiling |
| [Establish initial models](Box_Office_Quants_FirstModel_7_24_24.ipynb) | Initial classifiers and period comparisons |
| [Tune and compare](Box_Office_Quants_InitialModelTuning_8_7_24.ipynb) | Model experiments and parameter exploration |
| [Review findings](Box_Office_Quants_FinalPresentationModels_8_21_24.ipynb) | Comparative analyses and feature importance |

**Data:** [TMDb Movies Dataset](https://www.kaggle.com/datasets/asaniczka/tmdb-movies-dataset-2023-930k-movies) and [IMDb non-commercial data](https://developer.imdb.com/non-commercial-datasets/). The original notebooks were developed using Colab/Spark and are preserved as research artifacts, not presented as a one-command reproducible application. No private credentials are required in the repository.

## What this demonstrates

**Engineering:** integrating heterogeneous sources, analytical data preparation, PySpark workflows, and experiment organization.

**Analytical judgment:** defining measurable outcomes, comparing models, questioning feature availability, and explaining where apparently strong retrospective results might be misleading.

## Limitations and next iteration

Audience ratings and popularity can reflect post-release information. The historical notebooks also need stricter chronological holdouts and train-only preprocessing to support forward-looking performance claims. COVID-era comparisons describe associations rather than causal effects.

The next engineering milestone is a leakage-aware pipeline using pre-release features, chronological validation, simple financial baselines, calibrated metrics, and a tested model card. No unverified predictive performance is claimed.

## Attribution

This project began as the **Box Office Quants** collaborative graduate data-science capstone. The original research notebooks reflect team work; I am preserving that attribution while evolving the repository into a clearer engineering case study.
