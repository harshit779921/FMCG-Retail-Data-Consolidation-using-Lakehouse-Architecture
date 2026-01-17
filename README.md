# FMCG Retail Data Consolidation using Lakehouse Architecture (Databricks, Spark, AWS)                                                                               

## Project Overview
This project demonstrates an end-to-end data engineering pipeline built using **Databricks** and **AWS** for an FMCG business use case. The project handles data ingestion from multiple source systems, supports full and incremental loads, performs transformations, and prepares analytics-ready datasets following data engineering best practices.

## Tech Stack
- Databricks (Apache Spark)
- PySpark
- SQL
- AWS (data storage and integration)
- CSV Files

## Key Features
- Full and incremental data load implementation
- Multi-source data ingestion (Parent & Child companies)
- Data cleansing and transformations using PySpark
- Analytics-ready datasets for reporting
- Cloud-based processing using Databricks and AWS

## Project Structure
```
FMCG Retail Data Consolidation using Lakehouse Architecture/
│
├── 0_data/
│   ├── 1_parent_company/
│   │   ├── full_load/
│   │   │   ├── dim_customers.csv
│   │   │   ├── dim_products.csv
│   │   │   ├── dim_gross_price.csv
│   │   │   └── fact_orders.csv
│   │   └── incremental_load/
│   │       ├── fact_orders.csv
│   │       └── incremental_data_parent_company_query.txt
│   │
│   ├── 2_child_company/
│   │   └── full_load/
│   │       ├── customers/
│   │       ├── gross_price/
│   │       └── orders/
│
└── notebooks/
    ├── data_ingestion
    ├── transformations
    └── analytics
```

## Data Pipeline Flow
1. Ingest raw CSV data from AWS storage into Databricks
2. Perform full load for initial data setup
3. Process incremental data for new or updated records
4. Apply transformations using PySpark and SQL
5. Generate final datasets for analytics and reporting

## Use Case
Designed for FMCG analytics such as sales performance tracking, customer insights, and pricing analysis.

## How to Run
1. Upload project files to Databricks Workspace
2. Configure access to AWS storage
3. Create a cluster using Databricks Free Edition
4. Execute notebooks in the following order:
   - Data Ingestion
   - Transformations
   - Analytics
