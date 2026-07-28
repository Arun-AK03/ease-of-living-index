# experiments / Econ

Exploratory work for the **Economic** sub-index: assembling the raw economic
indicators and benchmarking imputation methods before the clean versions were
moved to `src/economics/`.

## Notebooks
- `Missing tables.ipynb` — maps the missing values in the economic panel.
- `Data_Imputation.ipynb` — early economic imputation experiments.
- `Econ_Mice_model_testing.ipynb` — benchmarks MICE imputation accuracy on
  synthetic missingness.
- `Combining.ipynb` / `Formating_and_Combining.ipynb` — merge and reshape the raw
  economic sources (GDP, inflation, unemployment, cost of living) into one panel.

Research-quality notebooks; the production pipeline is in `src/economics/`.
