# src

The core pipeline. One folder per sub-index plus a `ranking/` folder that
combines them. Each pillar folder is self-contained and follows the same recipe:

1. **Impute** missing values — two competing methods, kept side by side:
   - `*MICE*data_imputation` — Multiple Imputation by Chained Equations
   - `*RFR*data_imputation` — Random Forest Regression imputation
2. **Factor-analyse** the imputed indicators — `FA_*` notebooks run factor
   analysis / PCA to reduce many indicators to one score.
3. **Build the index** — `*Index_creation` notebooks produce the sub-index score
   written to `Data/processed/`.

Both MICE and RFR variants are retained so the two imputation strategies can be
compared (the head-to-head accuracy benchmark lives in `experiments/`).

## Folders

| Folder | Sub-index |
|---|---|
| `economics/` | Economic (GDP, inflation, unemployment, cost of living) |
| `institutional/` | Institutional (governance, rule of law, freedoms) |
| `quality_of_life/` | Quality of Life (health, crime, HDI) |
| `sustainability/` | Sustainability (emissions, energy, air quality) |
| `ranking/` | Combines the four sub-indices into the final EoLI and ranks countries |

## Naming key
`MICE` = chained-equations imputation · `RFR` = random-forest imputation ·
`FA` = factor analysis · index files ending `_FA` / `_PCA` denote which
dimensionality-reduction method produced the score.
