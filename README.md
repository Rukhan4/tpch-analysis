# TPC-H SQL + Python Analytics

This project analyzes the [TPC-H](https://www.tpc.org/tpch/) benchmark dataset using SQLite, SQL, and Python (pandas + seaborn). It demonstrates real-world data analytics workflows combining relational queries with Python visualizations.

## Project Structure


## Tech Stack

- Database: SQLite
- Language: SQL + Python
- Libraries: pandas, seaborn, matplotlib, sqlite3
- IDE: Visual Studio Code with Jupyter extension

## Analyses

### 1. Annual Revenue Trend

Shows yearly revenue across all orders.

- SQL: JOIN `orders` + `lineitem`
- Visualization: Bar chart of revenue by year

```sql
SELECT substr(o_orderdate, 1, 4) AS year, 
       SUM(l_extendedprice * (1 - l_discount)) AS total_revenue
FROM orders
JOIN lineitem ON o_orderkey = l_orderkey
GROUP BY year;
```

### 2. Top 10 Customers by Total Spend

Identifies the top 10 customers by total revenue generated.

- SQL: JOIN `customer`, `orders`, `lineitem`
- Visualization: Horizontal bar chart of customer spend

### 3. Most Popular Ship Modes

Shows shipment volume and revenue by shipping method.

- SQL: GROUP BY `l_shipmode`
- Visualizations:
  - Shipment count by mode
  - Revenue by mode

### 4. Delivery Delays by Ship Mode

Calculates average delivery delays and their financial impact.

- SQL: Uses `julianday()` and CASE filtering
- Visualizations:
  - Average delay by ship mode
  - Count of delayed shipments
  - Revenue from delayed orders

### 5. Top Supplier per Region by Revenue (Advanced SQL)

Ranks suppliers in each region by revenue using CTEs and window functions.

- SQL: RANK() OVER (PARTITION BY ...), WITH clause (CTE)
- Visualization: Bar chart of top supplier revenue per region

## Getting Started

1. Clone the repository:

```bash
git clone https://github.com/your_username/tpch-analysis.git
cd tpch-analysis
```

2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Run the notebook:

Open `tpch_analysis.ipynb` in VS Code with the Jupyter extension and execute all cells.

## Learning Outcomes

- Write efficient SQL queries across normalized schemas
- Use Python and pandas to process and visualize SQL results
- Analyze benchmark datasets in a structured project
- Apply window functions and multi-join logic in SQL

