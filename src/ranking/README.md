# src / ranking

The final step of the pipeline. Takes the four completed sub-indices
(Economic, Institutional, Quality of Life, Sustainability) from
`Data/processed/`, combines them into the composite **Ease of Living Index**,
and ranks countries — overall and within each sub-index, per year.

## Contents

- `Ranking.ipynb` — combines the four sub-indices into the composite score,
  computes ranks, and writes `Data/processed/Ease_Of_Living_Index_Final.csv` and
  `..._With_Ranks.csv`. Also exports the rank tables into `index dataset/`.
- `index dataset/` — the exported rankings, sliced three ways (see its own
  README): all-in-one, by index, by year, and by year × index.

## Output columns
For each country and year: a rank for every sub-index (`Economic_Rank`,
`Institutional_Rank`, `Quality_of_Life_Rank`, `Sustainability_Rank`) plus the
overall `Global_EoLI_Rank` / `Ease_of_Living_Rank`.
