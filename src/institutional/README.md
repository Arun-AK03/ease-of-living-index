# src / institutional

Builds the **Institutional** sub-index from governance and civic-freedom
indicators: control of corruption, government effectiveness, political
stability, regulatory quality, rule of law, voice and accountability, and
freedom of speech. Reads from `Data/interim/Final_Merged_Series_Data.csv` and
`Data/raw/`, and writes `Data/processed/Institutional_Index.csv`.

Both **MICE** and **RFR** imputation branches are provided for comparison.

## Notebooks

| Notebook | Role |
|---|---|
| `MICE_Data_Imputation.ipynb` | Fill missing governance values with MICE |
| `RFR_data_imputation.ipynb` | Fill missing governance values with random-forest regression |
| `FA_Ins_MICE.ipynb` | Factor analysis / PCA on the MICE-imputed data |
| `FA_Ins_RFR.ipynb` | Factor analysis / PCA on the RFR-imputed data |
| `MICE_Index_creation.ipynb` | Build the institutional index from the MICE branch |
| `RFR_Index_creation.ipynb` | Build the institutional index from the RFR branch |

## Flow
`merged institutional data` → impute (MICE or RFR) → factor analysis → index
creation → `Data/processed/Institutional_Index.csv` (contains both `_FA` and
`_PCA` scores).

The MICE-vs-RFR accuracy comparison for this pillar lives in
`experiments/Institutional/`.
