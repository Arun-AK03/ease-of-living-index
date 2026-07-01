# Global Ease of Living Index (EoLI)

A transparent, reproducible framework for measuring quality of life and cost of
living across countries over time.

The Ease of Living Index combines four sub-indices — **Economic**,
**Institutional**, **Quality of Life**, and **Sustainability** — into a single
composite score per country per year, using missing-data imputation (MICE and
Random Forest) and Principal Component Analysis (PCA) to weight and combine
indicators measured on different scales and units.

This repository contains the data pipeline, imputation models, and ranking
methodology behind the paper:

> *Global Ease of Living Index: a machine learning framework for longitudinal
> analysis of quality of life and cost of living*
> Transitional Artificial Intelligence Research Group, School of Mathematics and
> Statistics, UNSW Sydney, and the Centre for Artificial Intelligence and
> Innovation, Pingla Institute.
> [arXiv:2502.06866]([https://arxiv.org/abs/2502.06866])

## Why this exists

Existing cost-of-living and quality-of-life indices are often opaque about
their data sources, how missing values are handled, and how sub-indicators are
weighted into a final score. This project aims to be fully transparent and
reproducible: every raw data source, every imputation choice, and every
weighting step is open and re-runnable from raw data to final country
rankings.

## The four sub-indices

| Sub-index | What it measures | Example indicators |
|---|---|---|
| **Economic** | Cost and stability of economic life | GDP per capita, GDP growth rate, inflation, unemployment, cost of living |
| **Institutional** | Governance and civic freedoms | Rule of law, freedom of speech |
| **Quality of Life** | Health, safety, and material wellbeing | Healthcare access/expenditure, life expectancy, crime rate, poverty, HDI |
| **Sustainability** | Environmental conditions | Greenhouse gas emissions, access to electricity |

Each sub-index is built independently (clean → impute missing values → factor
analysis / PCA → index score), then all four are combined into the final EoLI
score and country ranking.

## Methodology, in brief

1. **Data collection** — indicators sourced from public datasets (World Bank,
   UN, etc.) and merged by country and year.
2. **Missing-data imputation** — two approaches are implemented and compared:
   Multiple Imputation by Chained Equations (MICE) and Random Forest
   Regression (RFR). Accuracy is evaluated on synthetic missingness (RMSE,
   MAE) before choosing an approach per sub-index.
3. **Standardisation** — indicators are converted to common units/scales
   (e.g. GDP to a common currency) so they can be combined.
4. **Index construction** — PCA reduces each group of standardised indicators
   to a single sub-index score.
5. **Composite index** — the four sub-indices are combined into the final
   Ease of Living Index as a weighted sum, and countries are ranked, including
   a sensitivity analysis of the ranking to weighting choices.

For the full methodology and evaluation results, see the paper.

## Data coverage

Major economies, roughly 1970–2023 depending on indicator availability
(some indicators, e.g. unemployment, only go back to 1991).

## Getting started

```bash
pip install -r requirements.txt
```

Output: `data/processed/eoli_final_with_ranks.csv` — final index score and
rank per country per year, plus each sub-index score individually.

## Repository layout

- `data/raw/` — canonical copies of source indicators
- `src/<pillar>/` — build, impute, and index-construction code per sub-index
- `src/ranking/` — combines the four sub-indices, PCA weighting, sensitivity analysis
- `experiments/` — MICE vs Random Forest benchmark per sub-index
- `notebooks/` — exploratory plots and figures, built on top of `src/eoli`
- `reports/` — generated charts (as shown in the paper)

## Citing this work

If you use this index or code, please cite the paper (see `CITATION.cff`).

## Contributing

Issues and pull requests are welcome — especially additional country coverage,
more recent years, or alternative imputation methods.

## License

See `LICENSE`.
