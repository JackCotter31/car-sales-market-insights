# Car Sales Market Insights

Exploratory and **business-focused** analysis of 50,000 used-car listings.
Originally produced as a mid-term assignment for *STAT40800 (UCD MSc)* and
extended with a market-analytics section aimed at a dealership / reseller
audience.

## What this project does

- Answers 8 structured data questions about the dataset (record count,
  year coverage, feature list, manufacturer frequencies, fuel-type mix,
  extremes, numeric summaries, correlations).
- Provides visual summaries for the three price drivers (mileage, engine
  size, fuel type) and the relationship between price and age.
- **Business analytics extension:**
  - Depreciation curve and implied annual depreciation rate.
  - **Value retention** by fuel type (young vs old stock).
  - **Brand positioning** table (median price, age, mileage, engine size).
  - **Price–mileage elasticity** via a log-linear regression with robust
    standard errors (`statsmodels`), isolating the price effect of mileage,
    age, engine size and fuel type.
  - **Segment analysis** (budget / mid / premium) with fuel-type mix.
  - **Value-for-money** ranking (price per 10k km) for 5–8-year-old cars.
- Closes with concrete recommendations for a dealership audience.

## Dataset

`car_sales_data.csv` — 50,000 rows, 7 columns:

| Column | Type | Description |
|---|---|---|
| Manufacturer | string | e.g. Ford, Toyota, VW, BMW |
| Model | string | e.g. Fiesta, RAV4 |
| Engine size | float | Litres |
| Fuel type | string | Petrol, Diesel, Hybrid |
| Year of manufacture | int | 1984 – 2022 |
| Mileage | int | km |
| Price | int | EUR |

## Getting started

```bash
git clone https://github.com/<you>/car-sales-market-insights
cd car-sales-market-insights
pip install -r requirements.txt
# put car_sales_data.csv in data/
jupyter notebook notebooks/car_sales_analysis.ipynb
