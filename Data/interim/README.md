# Data / interim

Intermediate working tables produced while turning `raw/` indicators into the
index-ready files in `processed/`. These are byproducts of the merge and
imputation steps — useful for debugging and reproducibility, but not final
outputs. Expect them to be regenerated when the pipeline is re-run.

## Files

- `Final_Merged_Series_Data.csv` — institutional indicators merged into one
  country/year panel (control of corruption, government effectiveness, political
  stability, regulatory quality, rule of law, etc.), the input to institutional
  imputation.
- `merged_csv.csv` — a wide cross-pillar merge (health, crime, emissions, and
  more) combined by country and year.

## Subfolders

- `economic pre impute/` — economic panels assembled just before imputation
  (`Econ_Testing*.csv`), progressively adding cost-of-living columns to the core
  GDP/inflation/unemployment series.
- `sustainability merged data/` — merged and filtered sustainability panels
  (emissions, renewables share, air pollution) before imputation and indexing.

## Notes
Headers and country/year keys are being harmonised at this stage, so column
names here are messier than in `processed/` (raw source labels, mixed casing).
