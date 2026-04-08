# Data

This folder contains all raw and cleaned data files for the "Quality of Life Per Dollar" project.

## Folder Structure

- `raw/`: original downloaded files, unmodified
- `clean/`: processed subsets created and saved by the analysis notebooks in `data_analysis/`

## Raw Data Files

### World Bank World Development Indicators

| File | Description |
|------|-------------|
| `worldbank_wdi_raw.csv` | Main data file. 4 series for 217 countries, 2011–2024. Load with `na_values=['..']`. |
| `worldbank_wdi_series_metadata.csv` | Metadata describing each series. |

**Variables:** GDP per capita PPP (current international $), Gini index, Life expectancy at birth (years), Current health expenditure per capita PPP.

**Source:** [World Bank Open Data](https://data.worldbank.org): downloaded as CSV.

---

### WHO Global Health Observatory

| File | Description |
|------|-------------|
| `who_le_at_birth.csv` | Life expectancy at birth (years) by country and sex, 2000–2021. |
| `who_hale_at_birth.csv` | Healthy life expectancy (HALE) at birth (years) by country and sex, 2000–2021. |

**Key columns:** `Location`, `Period`, `Dim1` (sex: Both sexes / Male / Female), `FactValueNumeric` (the estimate), `FactValueNumericLow`, `FactValueNumericHigh` (confidence interval).

**Note:** Data only extends to 2021. Country-level only, not city-level.

**Source:** [WHO Global Health Observatory](https://www.who.int/data/gho): downloaded as CSV.

---

### Numbeo City Indices

All Numbeo files are Excel workbooks with one sheet per year (2016–2025 or 2026). Years used in this project: **2019, 2020, 2021, 2022, 2024**.

| File | Key Variables |
|------|--------------|
| `numbeo_cost_of_living.xlsx` | Cost of Living Index, Rent Index, Local Purchasing Power Index, Groceries Index, Restaurant Price Index |
| `numbeo_crime.xlsx` | Crime Index, Safety Index |
| `numbeo_health_care.xlsx` | Health Care Index |
| `numbeo_pollution.xlsx` | Pollution Index |
| `numbeo_property_prices.xlsx` | Price to Income Ratio, Mortgage as % of Income, Affordability Index |
| `numbeo_traffic.xlsx` | Traffic Index, Time Index (minutes) |

**Source:** [Numbeo](https://www.numbeo.com): data was manually collected from the Numbeo website. Data is crowd-sourced.
