# Data Analysis

This folder contains Jupyter notebooks for data exploration and cleaning. Each notebook covers one data source and works through loading, inspecting, cleaning, and saving a processed subset to `data/clean/`.

## Notebooks

| Notebook | Dataset | Description |
|----------|---------|-------------|
| `01_worldbank_exploration.ipynb` | World Bank WDI | Explores GDP per capita PPP, Gini index, life expectancy, and health expenditure. Reshapes from wide to long format and saves a clean country-level subset. |
| `02_who_exploration.ipynb` | WHO Global Health Observatory | Explores life expectancy and HALE at birth by country. Filters to relevant years and saves a clean subset for both sexes combined. |
| `03_numbeo_cost_of_living_exploration.ipynb` | Numbeo Cost of Living | Explores Cost of Living Index, Rent Index, and Local Purchasing Power Index across 15 project years (2019-2025). |
| `04_numbeo_crime_exploration.ipynb` | Numbeo Crime | Explores Crime Index and Safety Index by city across 15 project years. |
| `05_numbeo_healthcare_exploration.ipynb` | Numbeo Healthcare | Explores Health Care Index by city across 15 project years. |
| `06_numbeo_pollution_exploration.ipynb` | Numbeo Pollution | Explores Pollution Index by city across 15 project years. |
| `07_numbeo_property_prices_exploration.ipynb` | Numbeo Property Prices | Explores Price to Income Ratio, Mortgage as % of Income, and Affordability Index by city across 15 project years. |
| `08_numbeo_traffic_exploration.ipynb` | Numbeo Traffic | Explores Traffic Index and Time Index by city across 15 project years. |
