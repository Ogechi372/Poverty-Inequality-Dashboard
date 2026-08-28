# Poverty & Inequality Dashboard — Data Analytics Capstone Project

**AnalystLab Africa Internship — Week 8 Final Capstone Project**

## Objective

This project applies a complete data analytics workflow: extraction, cleaning, analysis, and visualization to World Bank development data, exploring global poverty and income inequality trends across regions and countries.

## Dataset

**Source:** [World Bank — World Development Indicators (WDI)](https://datatopics.worldbank.org/world-development-indicators/)

Six indicators were selected for this analysis:
- Gini index
- Income share held by lowest 20%
- Income share held by highest 20%
- Poverty headcount ratio at $3.00 a day (2021 PPP), % of population
- Unemployment, total (% of total labor force), modeled ILO estimate
- GDP per capita (current US$)

The raw file contains 396,970 rows across all WDI indicators, countries, and years. After filtering, reshaping, and cleaning, the analysis dataset contains 33,191 rows.

## Tools Used

- **Python (pandas)** — data extraction, filtering, reshaping (wide → long), and cleaning
- **Power BI Desktop** — interactive dashboard and visualization
- **Jupyter Notebook** — data cleaning workflow

## Repository Contents

| File | Description |
|---|---|
| `capstone_poverty_inequality.ipynb` | Full data cleaning notebook (Python/pandas) |
| `poverty_inequality_cleaned.csv` | Final cleaned dataset used in Power BI |
| `poverty_inequality_dashboard.pbix` | Power BI dashboard file |
| `dashboard_screenshot.png` | Screenshot of the finished dashboard |
| `Poverty_Inequality_Final_Report.pdf` | Full written report |

## Data Cleaning Process

1. Filtered the raw WDI file down to the 6 target indicators, resolving naming inconsistencies (e.g. the poverty line threshold changed from $2.15/day to $3.00/day between WDI releases)
2. Reshaped data from wide format (one column per year) to long format (one row per country–indicator–year)
3. Removed rows with no reported value
4. Removed exact duplicate rows
5. Merged in official WDI country metadata to tag rows as **Country** vs **Aggregate**, and to attach Region/Income Group

## Dashboard Features

- 4 interactive slicers: Indicator Name, Region, Year, Type
- 6 KPI cards showing global averages for each indicator
- Line chart: poverty rate trend over time
- Bar chart: average Gini index by region
- Bar chart: income share gap (lowest vs. highest 20%) by region
- Matrix table: GDP per capita vs. poverty rate by country

## Key Findings

- Global average Gini index: **37.33**
- Global average poverty rate ($3.00/day, 2021 PPP): **14.48%**
- Top 20% of earners hold **44.48%** of income on average, vs. **6.71%** for the bottom 20%
- **Latin America & Caribbean** and **Sub-Saharan Africa** show the highest regional inequality (Gini ≈ 48 and 44)
- **Europe & Central Asia** shows the lowest regional inequality (Gini ≈ 33)

Full findings, insights, and recommendations are available in the [Final Report](./Poverty_Inequality_Final_Report.pdf).

## Author

Benjamin Umanta Esther 
Data Analytics Intern, AnalystLab Africa
