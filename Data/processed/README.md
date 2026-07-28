# Data / processed

Final, index-ready outputs. Everything here is clean, fully imputed (no missing
values), and standardised — the endpoint of the pipeline and the files you cite
or plot from. One file per sub-index, plus the composite Ease of Living Index.

## Files

- `Ease_Of_Living_Index_Final.csv` — the composite index. One row per country per
  year with each sub-index score (`Econ_Index`, `Institutional_Index`,
  `Quality_Of_Life_Index_FA`, `Sustainability_Index_FA`) and the combined
  `Ease_of_Living_Index`.
- `Ease_Of_Living_Index_Final_With_Ranks.csv` — the same, plus a rank column for
  each sub-index and the `Global_EoLI_Rank`. **This is the headline output** of
  the whole project.
- `Economic_data.csv` — processed economic sub-index inputs (GDP, inflation,
  unemployment, and the cost-of-living block).
- `Institutional_Index.csv` — governance indicators plus the institutional index
  computed by factor analysis (`_FA`) and PCA (`_PCA`).
- `QOLI_Index.csv` — quality-of-life indicators (life expectancy, doctors,
  electricity, HDI/GDI/GII, healthcare, crime) plus `QOLI_Index_FA` / `_PCA`.
- `Sustainability_index.csv` — emissions, renewable/non-renewable electricity and
  air pollution, plus `Sustainability_index_FA` / `_PCA`.

## Conventions
- `_FA` = score from factor analysis; `_PCA` = score from principal component
  analysis. The composite index uses the factor-analysis scores.
- Keyed by `Country` and `Year` throughout.

## Regenerating
These files are written by the notebooks in `src/<pillar>/` (per sub-index) and
`src/ranking/` (composite + ranks).
