# E-Commerce Revenue & Fulfillment Analytics (Power BI)

## 📌 Project Overview
An end-to-end Power BI solution analyzing e-commerce transactions. This project demonstrates **Star Schema modeling**, **Power Query ETL**, and **advanced DAX** for time intelligence and operational efficiency.

## 🛠 Tech Stack
- **Power BI Desktop** (Modeling, DAX, Visualization)
- **Power Query** (M Language) for data transformation.
- **Python** (Pandas) for synthetic data generation.

## 🗂 Data Model (Star Schema)
![Schema Diagram](docs/schema_diagram.png)
- **Fact Table:** `FactSales` (Grain: One row per order line).
- **Dimensions:** `DimDate`, `DimProduct`, `DimCustomer`.
- **Key Design Choice:** Implemented a dedicated Date table to enable accurate Time Intelligence (YTD, PY).

## 🧠 Key DAX Measures
| Measure | Logic | Purpose |
| :--- | :--- | :--- |
| `Revenue YTD` | `TOTALYTD` | Tracks cumulative performance. |
| `Revenue PY` | `CALCULATE` + `SAMEPERIODLASTYEAR` | Year-over-year comparison. |
| `% of Total` | `DIVIDE` + `ALL` | Contribution analysis. |

## 🚀 Power Query Transformations
- **Data Cleaning:** Fixed locale issues on imported dates.
- **Pivoting/Unpivoting:** Normalized quarterly columns into a flat structure.
- **Data Enrichment:** Merged product cost data to calculate profit margins.

## 📸 Dashboard Preview
