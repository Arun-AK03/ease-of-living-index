# src / quality_of_life

Builds the **Quality of Life** sub-index from health, safety and material
wellbeing indicators: life expectancy at birth, doctors per 10,000, access to
electricity, HDI / Gender Development / Gender Inequality indices, a healthcare
index and a crime index. Reads from `Data/interim/merged_csv.csv` and
`Data/raw/`, and writes `Data/processed/QOLI_Index.csv`.

Both **MICE** and **RFR** imputation branches are provided for comparison.

## Notebooks

| Notebook | Role |
|---|---|
| `MICE_data_imputation.ipynb` | Fill missing quality-of-life values with MICE |
| `RFR_data_imputation.ipynb` | Fill missing values with random-forest regression |
| `FA_Qal_MICE.ipynb` | Factor analysis / PCA on the MICE-imputed data |
| `FA_Qal_RFR.ipynb` | Factor analysis / PCA on the RFR-imputed data |
| `MICE_Index_creation.ipynb` | Build the QoL index from the MICE branch |
| `RFR_Index_creation.ipynb` | Build the QoL index from the RFR branch |

## Flow
`merged health / crime / development data` → impute (MICE or RFR) → factor
analysis → index creation → `Data/processed/QOLI_Index.csv` (`QOLI_Index_FA` and
`QOLI_Index_PCA`).

The MICE-vs-RFR accuracy comparison for this pillar lives in
`experiments/Quality of life/`.
