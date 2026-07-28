# Data / raw

Canonical, unmodified source indicators. These are the starting point of the
pipeline — downloaded from public datasets and kept as-is so every downstream
result is traceable back to an original file. **Do not edit files here**; all
cleaning happens downstream in `interim/` and `processed/`.

Each file is a single indicator (or a small related bundle) keyed by country and
year. Coverage varies by indicator, roughly 1970–2023.

## Files by sub-index

### Economic
- `Economic_data.csv` — merged economic indicators bundle
- `GDP_Per_Capita 1970-2023.csv` — GDP per capita
- `GDP_Growth_Rate(1970-2023).csv` — GDP growth rate
- `Inflation Rate_1970-2023.csv` — inflation rate
- `Unemployment_Rate(1991-2023).csv` — unemployment rate (starts 1991)
- `Cost of Living.csv` — cost-of-living, rent, groceries, restaurant, purchasing-power indices

### Institutional
- `Institutional_data_full.csv` — governance indicators (corruption, effectiveness, stability, regulatory quality, etc.)
- `Rule of Law 1996-2022.csv` — rule-of-law estimate
- `Freedom of Speech overall.xlsx` — freedom-of-speech index (Excel source)

### Quality of Life
- `Human Development Index - Full.csv` — HDI and related development indices
- `LE_at_B.csv` — life expectancy at birth
- `No_of_Doctors_per_10,000.csv` — doctors per 10,000 people
- `All_countries_healthcare_data.csv` — healthcare access / index data
- `AVG_Healthcare_Expenditure.csv` — average healthcare expenditure
- `crimerate_data_all_countries.csv` — crime / safety index
- `Poverty Data (People earning less than $2.5).csv` — poverty headcount
- `Population_in_Slums.csv` — share of population in slums

### Sustainability
- `Access to Electricity 1990-2022.csv` — access to electricity (starts 1990)
- `Sustainability_1990.csv` — emissions, renewable/non-renewable electricity, air pollution

## Notes
- Filenames contain spaces and special characters; quote paths when loading.
- Country names and year ranges are not yet harmonised here — that alignment
  happens in `interim/`.
