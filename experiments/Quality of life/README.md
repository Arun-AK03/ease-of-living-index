# experiments / Quality of life

Exploratory work for the **Quality of Life** sub-index: pulling together the
health, crime and development indicators and testing imputation before the clean
versions moved to `src/quality_of_life/`.

## Notebooks
- `Missing tables.ipynb` — maps missing values across the QoL indicators.
- `Data_Imputation_Q.ipynb` — early QoL imputation experiments.
- `model_testing.ipynb` — benchmarks imputation-method accuracy (MICE vs RFR).
- `Data_combining.ipynb` / `Formating.ipynb` — merge and reshape the raw sources
  (life expectancy, doctors, healthcare, crime, development indices).
- `HDI_exteaction.ipynb` — extracts the Human Development Index (and related
  gender indices) from the raw HDI source. *(filename is misspelled "exteaction")*

Research-quality notebooks; the production pipeline is in `src/quality_of_life/`.
