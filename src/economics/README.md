# src / economics

Builds the **Economic** sub-index from GDP per capita, GDP growth, inflation,
unemployment and the cost-of-living block. Reads the economic panels from
`Data/interim/economic pre impute/` and `Data/raw/`, and writes the finished
score to `Data/processed/Economic_data.csv`.

Two imputation strategies are implemented in parallel so they can be compared:
**MICE** (chained equations) and **RFR** (random forest).

## Notebooks

| Notebook | Role |
|---|---|
| `Econ_MICE_data_imputation.ipynb` | Fill missing economic values with MICE |
| `Econ_RFR_imputation.ipynb` | Fill missing economic values with random-forest regression |
| `FA_Econ_MICE.ipynb` | Factor analysis / PCA on the MICE-imputed data |
| `FA_Econ_RFR.ipynb` | Factor analysis / PCA on the RFR-imputed data |
| `Econ_MICE_Index_creation.ipynb` | Build the economic index from the MICE branch |
| `RFR_Index_creation.ipynb` | Build the economic index from the RFR branch |

## Flow
`raw / interim economic data` → impute (MICE or RFR) → factor analysis → index
creation → `Data/processed/Economic_data.csv`.

The MICE-vs-RFR accuracy comparison for this pillar lives in `experiments/Econ/`.
