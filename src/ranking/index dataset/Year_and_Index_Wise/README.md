# src / ranking / index dataset / Year_and_Index_Wise

The finest-grained slice of the rankings: broken down by **both year and
index**. There is one subfolder per year, and inside each year one file per
index.

## Structure
```
Year_and_Index_Wise/
  <YEAR>/
    <YEAR>_Economic_Rank.csv
    <YEAR>_Institutional_Rank.csv
    <YEAR>_Quality_of_Life_Rank.csv
    <YEAR>_Sustainability_Rank.csv
    <YEAR>_Ease_of_Living_Rank.csv
```
For example, `1971/1971_Economic_Rank.csv` is the economic ranking of countries
for 1971 only.

Each file holds `Year`, `Country`, and the single rank column for that index in
that year.

## When to use this
Reach for these when you want exactly one index in exactly one year without
filtering a larger table. For broader views use the coarser slices one level up:
`../Index_Wise/` (one index, all years) or `../Year_Wise/` (all indices, one
year).

## Note
Year subfolders exist only for years with sufficient data, so the set of years
is not perfectly contiguous. Every year folder shares the identical five-file
layout described above.
