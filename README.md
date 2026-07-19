# Retail Superstore Sales Analytics — Power BI (CDAP Capstone)

**Author:** Diaa Aldein Alsayed Ibrahim Osman | [LinkedIn](http://www.linkedin.com/in/diaa-ibrahim-31381656)
**Program:** Certified Data Analyst Professional (CDAP) — Epsilon AI Institute — *Capstone project, highest score in cohort*

## Overview
A 14-page storytelling dashboard (~400 visuals) analyzing a retail superstore dataset end-to-end — covering **every required module and every bonus module** in the capstone brief:

| # | Page | Key techniques |
|---|------|----------------|
| 1 | Descriptive Statistics | Statistical KPI cards (mean, median, mode, STD) |
| 2 | Time-Series Analysis | SPLY comparisons, growth rates (DAX time intelligence) |
| 3 | Product Analysis | Top sellers, margins, discount exposure |
| 4 | Category / Sub-Category | Per-category sales & LY comparisons |
| 5 | Discount Analysis | Discount rate distribution, impact on sales & profit |
| 6 | Profitability Analysis | Profit margin by product / category |
| 7 | Quantity Analysis | Trends + correlation scatter (quantity vs. profit/discount) |
| 8 | Order Analysis | Average ticket size, order value distribution |
| 9 | Customer Analysis *(bonus)* | **CLV, churn rate, retention rate, customer lifespan** |
| 10 | Geographic Analysis | Map + decomposition tree (country → city root-cause) |
| 11 | Inventory Analysis *(bonus)* | **Inventory turnover rate**, slow-mover identification |
| 12 | Forecasting *(bonus)* | Time-series forecasts for sales & profit |
| 13 | Cost Analysis | COGS, cost-vs-profit scatter |
| 14 | Market Basket *(bonus)* | Product associations via disconnected table pattern |


## Dashboard Pages

| | |
|---|---|
| ![Descriptive](screenshots/01-descriptive-statistics.png) **1. Descriptive Statistics** | ![Time Series](screenshots/02-time-series-analysis.png) **2. Time-Series Analysis** |
| ![Product](screenshots/03-product-analysis.png) **3. Product Analysis** | ![Category](screenshots/04-category-subcategory-analysis.png) **4. Category / Sub-Category** |
| ![Discount](screenshots/05-discount-analysis.png) **5. Discount Analysis** | ![Profitability](screenshots/06-profitability-analysis.png) **6. Profitability Analysis** |
| ![Quantity](screenshots/07-quantity-analysis.png) **7. Quantity Analysis** | ![Order](screenshots/08-order-analysis.png) **8. Order Analysis** |
| ![Customer](screenshots/09-customer-analysis-bonus.png) **9. Customer Analysis (Bonus)** | ![Geographic](screenshots/10-geographic-analysis.png) **10. Geographic Analysis** |
| ![Inventory](screenshots/11-inventory-analysis-bonus.png) **11. Inventory Analysis (Bonus)** | ![Forecasting](screenshots/12-forecasting-bonus.png) **12. Forecasting (Bonus)** |
| ![Cost](screenshots/13-cost-analysis.png) **13. Cost Analysis** | ![Market Basket](screenshots/14-market-basket-analysis-bonus.png) **14. Market Basket (Bonus)** |

**Data cleaning documentation:**

![Cleaning Disclaimer](screenshots/00-data-cleaning-disclaimer.png)

## Data Model
Star schema: `Fact_Order Details` + 9 dimensions (Date, Product, Category, Sub-Category, Customer, Customer Profile, Orders, City, Country) + dedicated `_Key Measure` table with **35+ DAX measures**.

## Data Cleaning (documented in full disclaimer)
- Removed exact duplicates in `Dim_Orders` and `Fact_Order Details`
- Repaired corrupted keys (`"13*"→13`, `"546*"→546`, `"#14"→14`) and text-typed dates
- **Reconstructed missing Sales (194.25) and Profit (23.625) values** from the unit economics of a comparable order (same product, year, ship mode)
- Resolved duplicate primary keys and filtered unmatchable null ship dates

> See `Cleaning_Summary_Disclaimer.pdf` for the full decision log.

## Files
- `Diaa_Aldein_Alsayed_Ibrahim_Power_Bi_Project.pbix` — the report
- `Cleaning_Summary_Disclaimer.pdf` — cleaning decision log
- `/screenshots` — one image per page
