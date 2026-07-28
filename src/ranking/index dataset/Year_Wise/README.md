# src / ranking / index dataset / Year_Wise

Rankings sliced **by year**. One file per year, each containing all five rank
columns (Economic, Institutional, Quality of Life, Sustainability, and overall
Ease of Living) for every country — a full snapshot of a single year.

## Files
`Index_Rankings_<YEAR>.csv`, e.g. `Index_Rankings_1971.csv` … `Index_Rankings_2021.csv`.

Columns: `Year`, `Country`, `Economic_Rank`, `Institutional_Rank`,
`Quality_of_Life_Rank`, `Ease_of_Living_Rank`, `Sustainability_Rank`.

## Note
Years are not fully contiguous — a file exists only for years with enough data
to rank countries (so some years, e.g. 1997 and 1999, are missing). For the
complementary "one index, all years" view see `../Index_Wise/`.
