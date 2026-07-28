# Data / interim / economic pre impute

Economic sub-index panels captured **just before missing-data imputation**.
These are staging tables that show the economic data being assembled step by
step, keyed by `Year` and `Country`. They feed the imputation notebooks under
`src/economics/`.

## Files

- `Econ_Testing.csv` — core macro series only: inflation, GDP per capita, GDP
  growth rate, unemployment.
- `Econ_Testing_2.csv` — the above plus the cost-of-living block (cost of living,
  rent, groceries, restaurant price, local purchasing power indices).
- `Econ_testing_3.csv` — a further iteration of the merged economic panel.

The numbered progression reflects columns being added and joins being refined
before the data is handed to MICE / Random Forest imputation. Still contains
missing values by design.
