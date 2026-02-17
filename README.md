# TPC-H End-to-End Data Analytics Project

This project analyzes the [TPC-H](https://www.tpc.org/tpch/) benchmark dataset using SQL, Python, and Excel to simulate a real-world analytics workflow. It demonstrates the ability to extract relational data, model operational and financial risk, and translate technical outputs into an executive KPI dashboard.

---

## KPI Dashboard Preview

![KPI Dashboard](./kpi%20dashboard.jpg)

---

## Tech Stack

**Database:** SQLite  
**Languages:** SQL, Python  
**Python Libraries:** pandas, matplotlib, seaborn, sqlite3  
**Excel Tools:** Pivot Tables, XLOOKUP, calculated fields, ranking formulas, statistical functions  
**Visualization:** Excel, Power BI  
**IDE:** VS Code (Jupyter)

---

## Project Workflow

### 1. Data Extraction (SQL)

- Multi-table JOINs across normalized schema
- Aggregations with `GROUP BY`
- Revenue calculations with discount adjustments
- Delivery delay calculations using date functions
- Common Table Expressions (CTEs)
- Window functions (`RANK() OVER (PARTITION BY ...)`)
- Regional supplier ranking
- Shipping mode performance aggregation

---

### 2. Data Modeling & Analysis (Python)

- Query execution and result processing with `sqlite3`
- Data transformation and aggregation using `pandas`
- Revenue trend analysis
- Delay impact modeling
- Risk-adjusted revenue calculation
- Revenue-at-risk computation
- Operational efficiency ranking
- Statistical metrics:
  - Mean
  - Standard deviation
  - Coefficient of variability
- Data visualization using matplotlib and seaborn

---

### 3. Business Intelligence & KPI Dashboard (Excel)

Built an executive dashboard integrating SQL and Python outputs.

Key components:

#### Operational Risk Modeling
- Delay impact by shipping mode
- Risk-adjusted revenue
- Revenue at Risk
- Operational efficiency ranking
- Revenue recovery potential modeling

#### Concentration & Dependency Analysis
- Top 10 customer analysis
- Customer concentration ratio (CR10)
- Herfindahl-Hirschman Index (HHI)
- Supplier revenue distribution by region
- Supplier geographic concentration index

#### Excel Techniques Used
- Pivot Tables for aggregation and segmentation
- XLOOKUP for cross-table metric mapping
- Calculated KPI fields
- Ranking functions
- Statistical functions (AVERAGE, STDEV, etc.)
- Custom financial modeling formulas
- Dashboard layout and visualization design

---

## Key Analytical Insights

- Revenue per shipment is tightly clustered across shipping modes.
- Delay impact varies significantly, indicating mispriced operational risk.
- Certain logistics channels exhibit inefficient risk-return profiles.
- Customer and supplier concentration risk is structurally balanced.
- Operational optimization presents the strongest margin stabilization opportunity.

---

## Skills Demonstrated

- Relational data modeling and advanced SQL querying  
- Window functions and ranking logic  
- Financial and operational risk modeling  
- Statistical analysis and variability measurement  
- Concentration index modeling (HHI, CR10)  
- End-to-end data pipeline development  
- Executive dashboard design and KPI translation  

---

This project demonstrates the ability to move from normalized relational data to structured analysis, quantitative risk modeling, and executive-level business intelligence.
