# U.S. Natural Gas & LNG Market Analysis

## Project Overview

This project analyzes the major fundamental factors affecting U.S. natural gas prices, with a focus on Henry Hub.

Using historical data from the U.S. Energy Information Administration (EIA), the analysis examines the relationships between:

- Henry Hub natural gas prices
- U.S. dry natural gas production
- U.S. natural gas storage
- U.S. LNG exports

The goal is to determine what supply/demand variables are strong indicators natural gas price movements.

## Tools Used

- Python
- pandas
- NumPy
- Matplotlib
- SQL
- DuckDB
- JupyterLab

## Key Finding

Henry Hub prices were strongly correlated with storage levels, and weakly correlated with production or LNG exports individually.

During 2020–2024, storage levels relative to normal storage levels had an approximately **-0.88 correlation** with Henry Hub prices. Monthly changes in the storage balance also had an approximately **-0.67 correlation** with monthly changes in Henry Hub prices.

These results suggest that storage can serve as a useful indicator of the balance between U.S. natural gas supply and demand.

## Key Visualization

![Henry Hub Price vs. U.S. Storage Balance](charts/henry_hub_price_vs_storage.png)

## Data Sources

All datasets were obtained from the U.S. Energy Information Administration (EIA).

- Henry Hub Natural Gas Spot Prices ($/MMBtu)
- U.S. Natural Gas Production (Bcf/d)
- U.S. Natural Gas Storage (Bcf)
- U.S. LNG Exports (Bcf/d)

Data was cleaned and standardized to support monthly comparisons.

## Methodology

### 1. Data Preparation

Python and pandas were used to import, clean, and standardize EIA datasets.

This included:

- Converting dates into consistent formats
- Converting production and LNG export volumes to Bcf/d
- Manipulating observations to monthly frequency
- Calculating natural gas storage relative to a historical seasonal benchmark

### 2. SQL Analysis

DuckDB was used to query and combine the datasets into a monthly natural gas market dataset.

SQL queries were used to:

- Join datasets by month and year
- Calculate LNG exports as a percentage of U.S. production
- Analyze relationships between production, LNG exports, storage, and prices
- Compare relationships across different LNG export growth periods

### 3. Statistical Analysis and Visualization

Python, pandas, NumPy, and Matplotlib were used to calculate correlations, examine monthly changes, and visualize relationships.

Particular attention was given to the 2020–2024 period to examine natural gas market behavior in the modern U.S. LNG export era.

## Detailed Findings

### Storage and Henry Hub Prices

From 2020–2024, Henry Hub prices exhibited a strong negative correlation (**-0.88**) with storage levels relative to normal storage levels.

The correlation between monthly changes in storage levels relative to normal storage levels and monthly changes in prices was also strongly negative (**-0.67**).

These findings suggest that storage conditions provide a useful indicator of how undersupplied or oversupplied the market is.

### Production and LNG Exports

During 2020–2024, production and LNG exports individually exhibited weak correlations with Henry Hub prices:

- Production vs. price: **0.02**
- LNG exports vs. price: **0.09**

However, production and LNG exports were strongly positively correlated (**0.80**), reflecting the growth of both during this period.

### Limitations

This analysis is based on historical correlations and does not establish causal relationships.

Several important natural gas market drivers were not directly modeled, including:

- Weather-driven events
- Heating and cooling demand
- Power generation demand
- Pipeline exports and imports
- International natural gas prices
- Infrastructure constraints and supply disruptions

Monthly data may also obscure short-term price volatility.

Storage levels relative to normal storage levels should be interpreted as an accumulation of many supply/demand variables rather than an independent driver of prices.

## Conclusion

The results suggest that Henry Hub prices appear to be driven less by any single supply or demand variable and more by the balance between supply and demand (i.e. storage levels relative to normal storage levels).

Among the variables analyzed, natural gas storage levels relative to normal storage levels exhibited the strongest relationship with Henry Hub prices during 2020–2024.

This project demonstrates the application of Python, SQL, statistical analysis, and data visualization to understanding fundamental energy market relationships.