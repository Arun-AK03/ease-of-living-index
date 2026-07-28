# src / sustainability

Builds the **Sustainability** sub-index from environmental indicators: carbon
dioxide emissions, greenhouse-gas emissions, renewable and non-renewable
electricity production, and micro air pollution. Reads from
`Data/interim/sustainability merged data/` and `Data/raw/`, and writes
`Data/processed/Sustainability_index.csv`.

Both **MICE** and **RFR** imputation branches are provided for comparison.

## Notebooks

| Notebook | Role |
|---|---|
| `MICE_Data_Imputation.ipynb` | Fill missing environmental values with MICE |
| `RFR_data_imputation.ipynb` | Fill missing values with random-forest regression |
| `FA_Sus_MICE.ipynb` | Factor analysis / PCA on the MICE-imputed data |
| `FA_Sus_RFR.ipynb` | Factor analysis / PCA on the RFR-imputed data |
| `MICE_Index_creation.ipynb` | Build the sustainability index from the MICE branch |
| `RFR_Index_creation.ipynb` | Build the sustainability index from the RFR branch |

## Flow
`merged sustainability data` → impute (MICE or RFR) → factor analysis → index
creation → `Data/processed/Sustainability_index.csv` (`Sustainability_index_FA`
and `_PCA`).

The MICE-vs-RFR accuracy comparison for this pillar lives in
`experiments/Sustainability/`.
