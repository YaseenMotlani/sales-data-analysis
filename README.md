# Smart Stock Intelligence & Expiry Risk Analyzer

An ongoing, hands-on data analytics project focused on analyzing retail sales and inventory data to identify business trends, data quality issues, and inventory-related risks using Python and Pandas.

The project aims to transform raw retail data into meaningful business insights that can support sales performance analysis, inventory monitoring, and data-driven decision-making.

## Current Progress

**Phase 1: Data Loading & Audit — Completed**

- Loaded and inspected retail sales and inventory datasets using Pandas.
- Analyzed dataset structure, column data types, missing values, and duplicate records.
- Investigated return transactions, negative sales quantities, and financial values.
- Identified negative inventory quantities and examined affected products, stores, and stock statuses.
- Validated date columns and documented initial data quality findings.
- Exported audit-stage datasets to Parquet for reuse across separate Jupyter notebooks.

### Initial Audit Findings

| Finding                               | Result | 
|---|---:|
| Sales dataset                         | 125,751 rows × 17 columns |
| Inventory dataset                     | 284,755 rows × 18 columns |
| Return-marked sales records           | 7,491 (5.96%) |
| Missing values in `Reason of Return`  | 125,751 (100%) |
| Negative inventory records            | 1,380 |
| Total negative inventory quantity     | -1,767 units |
| Negative `Cost of Stocks` records     | 8,022 |
| Negative stock selling amount records | 1,380 |
| Exact duplicate rows in sales         | 0 |
| Exact duplicate rows in inventory     | 0 |
| Invalid sales dates                   | 0 |
| Invalid inventory start dates         | 0 |
| Invalid inventory end dates           | 0 |

**Key observations:**

- All 7,491 return-marked records contain negative quantities, sales amounts, and COGS.
- `Full Price` has the highest number of negative-stock records (1,078).
- Product `PROD-161865` has 58 negative-stock records.
- Store `STR-1198` has 96 negative-stock records.
- The inventory dataset contains the end date `9999-12-31`, which requires further investigation.

*Note: These are initial audit findings. Negative values have not been automatically removed or modified.*

## Project Roadmap

- **Data Cleaning:** Investigate missing values, validate data types, and handle data quality issues using appropriate business rules.
- **Exploratory Data Analysis (EDA):** Analyze sales performance, product trends, returns, and inventory patterns.
- **Data Visualization:** Create meaningful charts and comparisons using Python.
- **Business Insights:** Identify important trends, risks, and opportunities for improvement.
- **Future Expansion:** Extend the analysis using Excel, SQL, and Power BI to develop interactive dashboards and performance metrics.
- **Expiry Risk Analysis:** Explore expiry-related analysis if reliable product expiry or batch-level data becomes available.

## Project Goal

Gradually develop this mini-project into a comprehensive, end-to-end data analytics portfolio project covering data loading, cleaning, exploratory analysis, visualization, and actionable business insights.

## Tech Stack

Python · Pandas · NumPy · Matplotlib · Jupyter Notebook · Parquet

**Planned:** Excel · SQL · Power BI

**Status:** In Progress — Data Loading & Audit completed; Data Cleaning is the next phase.