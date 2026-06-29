# Technical Brief

## What This Shows

This project is a complete tabular ML case study: messy structured data, domain-aware cleaning, model comparison, ensemble learning, and explainability.

## Technical Decisions

- Group-based imputations preserve relationships between make, model, condition, and registration year.
- RFE limits feature noise before fitting the highest-capacity models.
- Tree ensembles are the strongest fit because price is driven by non-linear interactions.
- Stacking edges out single models while keeping the base learners interpretable.
- SHAP and PDP analysis turn the model from a score generator into an explainable valuation workflow.

## Strongest Evidence

- Clear train/validation/test separation.
- Multiple model families compared on the same target.
- Ensemble lift measured against individual learners.
- Dimensionality-reduction experiments used as evidence, not decoration.
- Explainability techniques applied after model selection.

## Production Path

- Move preprocessing and model training into `src/car_price_modeling/`.
- Add a repeatable `train.py` entrypoint.
- Persist metrics, fitted encoders, selected features, and model artifacts.
- Add a compact synthetic fixture for CI tests.
