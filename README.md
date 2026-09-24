# SA Development Analysis

Statistical analysis of South African unemployment and poverty using World Bank data, comparing the 2008 financial crisis and the COVID-19 pandemic.

## Project Status

Core analysis complete.

## Objective

How did poverty and unemployment in South Africa shift around two major economic shocks, the 2008 global financial crisis and the COVID-19 pandemic, and how do the two shocks compare in severity and recovery?

## Data Sources

- World Bank Open Data: Poverty headcount ratio at national poverty lines (% of population)
- World Bank Open Data: Unemployment, total (% of total labor force), modeled ILO estimate

## Project Structure

- data/raw/: raw datasets downloaded from World Bank
- notebooks/: exploratory analysis and visualizations
- outputs/: charts and results

## Methodology

- Filtered both datasets to South Africa only
- Reshaped data from wide format (one column per year) to long format (one row per year) using pandas
- Poverty data has only 5 data points (2005, 2008, 2010, 2014, 2022) due to survey-based collection, so it is plotted as discrete points rather than a continuous line
- Unemployment data has full annual coverage (1991 to 2025), used as the primary time series to track shock timing
- Visualized both variables on a dual-axis line/scatter chart with 2008 and 2020 marked

## Key Findings

- Unemployment rose by about 2.4 percentage points from 2007 to 2010 (22.3% to 24.7%) following the 2008 financial crisis
- Unemployment rose by about 5.5 percentage points from 2019 to 2021 (28.5% to 34.0%) following COVID-19, more than double the rate of increase seen after 2008
- Unemployment has not returned to pre-shock levels after either event, suggesting a ratchet effect where each shock permanently raises the baseline
- Poverty data is too sparse to isolate a COVID-era spike directly (no data points between 2014 and 2022), a limitation of the dataset rather than the analysis



![Unemployment vs Poverty chart](https://github.com/tomzavi56/SA-Development-Analysis/raw/main/outputs/unemployment_vs_poverty.png)



## Limitations

- Poverty data's low frequency (survey based, only 5 points across 20 years) means it cannot precisely track the timing of either shock. Unemployment data carries most of the analytical weight here
- Analysis is descriptive (percentage point comparisons), not a formal statistical test of significance

## Tools

Python, pandas, matplotlib, Google Colab

## Author

Tom Ntaba
