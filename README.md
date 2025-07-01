# 📊 Sales Trend Analysis Using SQL

## 🎯 Objective
Analyze monthly revenue and order volume using SQL queries on the `online_sales` dataset.

## 🧰 Tools Used
- PostgreSQL / MySQL / SQLite (any one)
- SQL for querying and time-based aggregation

## 📂 Project Structure
```
Sales_Trend_Analysis/
├── scripts/
│   ├── sales_trend_analysis_postgres.sql   # Query for PostgreSQL/MySQL
│   └── sales_trend_analysis_sqlite.sql     # Query for SQLite
├── results/
│   └── sales_trend_results.csv             # Sample output table
├── README.md                               # Project guide and instructions
```

## 🧪 Dataset Info
Table name: `online_sales`

Columns required:
- `order_id` (unique order identifier)
- `order_date` (timestamp/date)
- `amount` (numeric, order revenue)
- `product_id` (optional for future filtering)

## 🔍 What This Query Does
- Extracts **year and month** from `order_date`
- Calculates:
  - `SUM(amount)` → Total revenue
  - `COUNT(DISTINCT order_id)` → Number of orders
- Sorts results by year and month

## 💡 SQL Notes
### PostgreSQL / MySQL
- Use `EXTRACT(YEAR FROM order_date)`
- Use `EXTRACT(MONTH FROM order_date)`

### SQLite
- Use `strftime('%Y', order_date)` and `strftime('%m', order_date)`

## ✅ Output
Check `results/sales_trend_results.csv` for a sample output. Replace it with your real query results after execution.

## ▶️ How to Use
1. Choose your SQL script depending on your database.
2. Run it against the `online_sales` table.
3. Export the result as CSV and save to the `results/` folder.
