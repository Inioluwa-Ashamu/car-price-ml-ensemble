# Car Price Prediction with Ensemble Machine Learning

Portfolio project based on an MSc machine-learning assessment. The project builds an end-to-end tabular regression workflow for estimating used-car listing prices from AutoTrader-style advert data.

## Overview

The modelling task is to predict vehicle price from advert attributes such as mileage, registration year, make, model, fuel type, body type, colour, and condition. The project demonstrates practical data cleaning, feature engineering, model comparison, ensemble learning, dimensionality reduction, and explainable AI techniques.

## Methods

- Missing-value analysis and group-based imputation.
- Outlier treatment using domain-aware mileage and price handling.
- Categorical encoding and numerical scaling.
- Train, validation, and test splitting.
- Recursive Feature Elimination with a Random Forest estimator.
- Random Forest and Gradient Boosting regression.
- Averaging and stacking ensembles.
- PCA and Isomap dimensionality reduction.
- Polynomial Ridge regression benchmark.
- KMeans-derived feature engineering.
- Permutation importance, SHAP, and partial dependence plots.

## Results Snapshot

The advanced notebook reports validation performance around:

| Model | Validation R2 |
| --- | ---: |
| Random Forest | 0.7208 |
| Gradient Boosting | 0.7222 |
| Averaging Ensemble | 0.7273 |
| Stacking Ensemble | 0.7274 |
| PCA Gradient Boosting | 0.6884 |
| Polynomial Ridge | 0.6905 |
| Gradient Boosting with cluster feature | 0.7068 |

The strongest result came from a stacked ensemble, with tree-based models outperforming linear and compressed-feature baselines.

## Repository Structure

```text
.
├── notebooks/
│   ├── advanced_car_price_modeling.ipynb
│   └── baseline_car_price_modeling.ipynb
├── data/
│   └── README.md
├── docs/
│   └── portfolio_notes.md
├── requirements.txt
└── README.md
```

## Data

The original CSV is not included because redistribution rights need to be confirmed. To run the notebooks, place the dataset at:

```text
data/adverts.csv
```

The expected target column is `price`.

## How to Run

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
jupyter lab
```

Open `notebooks/advanced_car_price_modeling.ipynb`.

## Portfolio Value

This project is best presented as evidence of applied data science: cleaning a messy real-world tabular dataset, building interpretable features, comparing multiple modelling families, and explaining predictions with SHAP/PDP rather than reporting a single black-box score.

## Limitations

- The raw dataset is excluded from the public repo.
- The notebooks should be refactored into reusable Python modules before production use.
- Validation results should be rerun after any data or preprocessing changes.
