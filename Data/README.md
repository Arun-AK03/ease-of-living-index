# Data

The full data pipeline for the Ease of Living Index, organised into three stages
that mirror the flow from source files to final index scores. Data moves in one
direction: `raw/` → `interim/` → `processed/`.

## Stages

| Folder | Stage | What lives here |
|---|---|---|
| `raw/` | Source | Canonical, unmodified copies of every indicator downloaded from public datasets (World Bank, UN, cost-of-living sources, etc.). Nothing here is edited by the pipeline. |
| `interim/` | Intermediate | Merged and reshaped tables produced while combining raw indicators by country and year, and the "pre-impute" tables fed into the imputation models. |
| `processed/` | Final | Clean, fully imputed, index-ready outputs: one file per sub-index plus the final composite Ease of Living Index with ranks. |

## How it is produced

The notebooks under `src/<pillar>/` read from `raw/` and `interim/`, run
missing-data imputation (MICE / Random Forest) and factor analysis / PCA, and
write the per-pillar results into `processed/`. `src/ranking/` then combines
those into the final composite index.

## Naming note

Some code and the top-level README refer to this directory in lowercase
(`data/...`). On case-sensitive filesystems the actual folder name is `Data/`;
adjust paths accordingly when running notebooks.
