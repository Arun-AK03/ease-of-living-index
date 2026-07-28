# src / ranking / index dataset

Exported ranking tables produced by `../Ranking.ipynb`. The same underlying
ranks (Economic, Institutional, Quality of Life, Sustainability, and overall
Ease of Living) are sliced three different ways for convenience.

## Contents

- `All_Years_All_Index_Rankings.csv` — everything in one table: one row per
  country per year with all five rank columns.
- `Index_Wise/` — one file per index, spanning all years. Use these to track a
  single dimension (e.g. how economic rank changes over time).
- `Year_Wise/` — one file per year, containing all five index ranks. Use these
  to see the full picture for a single year.
- `Year_and_Index_Wise/` — the finest slice: one subfolder per year, and inside
  it one file per index for that year.

All three are views of the same data — pick whichever slice matches your query.

## Note on year coverage
Years are not perfectly contiguous (e.g. 1997, 1999, 2001 are absent) because a
year only appears where enough indicators are available to rank countries.
