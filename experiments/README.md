# experiments

Exploratory and benchmarking work that supports the pipeline but isn't part of
the production path. The main purpose here is the **MICE vs Random Forest
imputation comparison**: each sub-index gets a "Missing tables" analysis and a
model-testing notebook that injects synthetic missingness and measures how
accurately each method recovers the true values (RMSE / MAE). The winner informs
the choice made in `src/<pillar>/`.

You'll also find early data-cleaning, merging and formatting notebooks that were
used while assembling the raw indicators — kept for provenance.

## Folders (one per sub-index)

| Folder | Contents |
|---|---|
| `Econ/` | Economic imputation testing plus combining/formatting notebooks |
| `Institutional/` | Institutional imputation testing and index prototype |
| `Quality of life/` | QoL imputation testing plus data combining, formatting, HDI extraction |
| `Sustainability/` | Sustainability missing-data analysis and model testing |

## Typical notebooks
- `Missing tables.ipynb` — quantifies where and how much data is missing.
- `*model_testing*.ipynb` / `MICE_model_testing.ipynb` — benchmark MICE vs RFR
  on synthetic missingness.
- `Combining` / `Formating` / `Data_combining` / `HDI_extraction` — one-off data
  preparation steps.

These are research notebooks: expect rough edges and paths that may need
adjusting. The clean, reproducible versions live under `src/`.
