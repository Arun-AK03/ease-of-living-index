# Data / interim / sustainability merged data

Merged sustainability panels created while combining the raw environmental
indicators into one country/year table, before imputation and index
construction in `src/sustainability/`.

## Files

- `merged_grouped_data.csv` — the full merge: renewables share of energy,
  greenhouse-gas and total emissions, trade and industry per GDP, labour force,
  CO₂ per capita, renewable electricity production, renewable energy
  consumption, and related fields.
- `filtered_merged_grouped_data.csv` — a trimmed version keeping only the
  columns carried forward into the sustainability index (emissions, renewables
  share, industry per GDP, CO₂ per capita, renewable electricity production and
  consumption).

Keyed by `country` and `year`. Still contains missing values — imputation
happens downstream.
