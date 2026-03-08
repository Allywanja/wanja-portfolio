# wanja-portfolio

## Project Overview

This project analyzes global retail sales data to uncover insights into revenue, profitability, customer behavior, and regional performance.

The analysis was conducted using **SQL for data cleaning and analysis** and **Excel for visualization and dashboard creation**.

---

## Business Problem

Retail companies must understand:

- Which markets generate the most revenue
- Which regions are most profitable
- How sales change over time
- Which customers contribute most to revenue

This project answers these questions using transactional sales data.

---

## Dataset

Dataset: Global Superstore Orders

Key columns include:

- order_id
- order_date
- customer_name
- market
- region
- category
- product_name
- sales
- profit
- discount
- shipping_cost

Dataset contains multiple global markets including:

- APAC
- EU
- US
- LATAM
- Africa
- EMEA
- Canada

---

## Data Cleaning (SQL)

The dataset required several cleaning steps:

- Fixing encoding issues
- Converting text dates to SQL date format
- Correcting column data types
- Handling import errors
- Checking for duplicate records

Example SQL query:

```sql
SELECT COUNT(*) FROM orders;

##Exploratory Data Analysis

#Key analyses performed:

Revenue by Market

```sql
SELECT market,
SUM(sales) AS total_sales,
SUM(profit) AS total_profit
FROM orders
GROUP BY market;

Sales Trend Analysis

```sql
SELECT
YEAR(order_date),
MONTH(order_date),
SUM(sales)
FROM orders
GROUP BY YEAR(order_date), MONTH(order_date);

##Excel Dashboard

An interactive Excel dashboard was created to visualize key metrics.

Dashboard features:

Revenue by Market
Sales Trend (2011–2014)
Category Performance
Top 10 Customers
KPI Cards

##Key Insights

APAC generates the highest revenue.

EU shows strong profitability.

EMEA has the lowest margins due to high discount rates.

Sales peak during Q4 each year.

A small group of customers contributes significant revenue.

##Business Recommendations

Reduce excessive discounting in EMEA.

Increase investment in APAC and EU markets.

Develop loyalty programs for top customers.

Prepare inventory for Q4 seasonal sales spikes.

##Tools Used

MySQL

SQL

Excel (Pivot Tables, Charts, Dashboard)

Author

ALICE WANJA

Aspiring Data Analyst
