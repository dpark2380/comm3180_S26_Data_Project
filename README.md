# Quality of Life Per Dollar: Finding the World's Most Underrated Cities

A data journalism project for COMM3180 Stories from Data (Spring 2026).

## Overview

Existing liveability indices like the EIU Global Liveability Ranking consistently place wealthy Western cities at the top. Vienna, Copenhagen, and Zurich appear year after year. But these rankings share a common blind spot: they completely ignore what things actually cost for the people who live there.

This project builds an original "value for living" index across 500+ global cities and 90+ countries, asking a different question: which cities offer the highest quality of urban life relative to their cost of living? The answer looks nothing like the standard rankings.

## Research Questions

| # | Question |
|---|----------|
| RQ1 | Which cities score highest on quality of life relative to cost of living? |
| RQ2 | Are good-value countries clustered in particular world regions, and what are the indicators of such countries? |
| RQ3 | What is the relationship between city-level traffic and pollution? |
| RQ4 | Does income inequality explain why some low-cost countries still score poorly on quality of life? |
| RQ5 | Has the cost of living risen faster than quality of life since COVID? |

## Key Findings

- Top-value cities concentrate in Eastern Europe and South Asia, with quality scores above average on safety combined with cost of living indices well below 25 on the NYC-anchored scale
- GDP per capita is strongly negatively correlated with the value index (r = -0.56), confirming that richer countries are systematically more expensive relative to their quality
- EIU top cities rank in the bottom 10% of our index: Vienna 106th, Zurich 217th of 222 cities
- Affordability fell 28% during the COVID shock and had not recovered for 101 of 125 cities by 2024

## Repository Structure

```
data/
  raw/          Numbeo sub-index files (cost of living, crime, healthcare, pollution, traffic)
  clean/        Processed datasets saved by exploration notebooks

data_analysis/
  01_worldbank_exploration.ipynb
  02_who_exploration.ipynb
  03_numbeo_cost_of_living_exploration_city.ipynb
  03_numbeo_cost_of_living_exploration_country.ipynb
  04_numbeo_crime_exploration.ipynb
  05_numbeo_healthcare_exploration.ipynb
  06_numbeo_pollution_exploration.ipynb
  07_numbeo_property_prices_exploration.ipynb
  08_numbeo_traffic_exploration.ipynb
  rq1_value_for_living_city.ipynb
  rq2_value_for_living_country.ipynb
  rq3_traffic_and_pollution.ipynb
  rq4_income_inequality.ipynb
  rq5_covid_value_trends.ipynb

presentations/  Slide decks from project presentations
```

## Data Sources

| Dataset | Source | Coverage |
|---------|--------|----------|
| Cost of Living, Safety, Healthcare, Pollution, Traffic sub-indices | Numbeo | 500+ cities, 90+ countries, 2016-2024 |
| GDP per capita PPP, Gini coefficient, life expectancy | World Bank WDI | 217 countries, 2011-2024 |
| Healthy life expectancy (HALE) | WHO Global Health Observatory | Country-level |

## Index Construction

The composite quality score averages four dimensions: Safety Index, Healthcare Index, Clean Air (100 minus Pollution Index), and Low Traffic (Traffic Index rescaled to 0-100). The value index divides this quality score by the Cost of Living Index. A quality floor at the 25th percentile is applied to rankings so that very cheap but low-quality cities do not dominate purely through low cost.

## Team

COMM3180 Stories from Data, University of Pennsylvania, Spring 2026.
