# Data Warehousing and Analytics
This repo showcases a complete data warehousing and analytics solution, starting from building the data warehouse to creating valuable insights from the data.

## Overview
This project includes the following components:
- **Data Architecture**: A well-defined Medallion architecture that outlines the flow of data from source systems to the data warehouse using Bronze, Silver, and Gold layers.
- **ETL Pipelines**: Scripts for Extract, Transform, Load (ETL) processes that ensure data is ingested, transformed, and stored efficiently.
- **Data Modeling**: A comprehensive data model that includes fact and dimension tables, ensuring a robust structure for analytics.


## Building the Data Warehouse (Data Engineering)
Develop a modern data warehouse using SQL Server to consolidate sales data, enabling analytical reporting and informed decision-making.

### Specifications
- **Data Sources**: Import data from two source systems (ERP and CRM) provided as CSV files.
- **Data Quality**: Ensure data quality by implementing validation checks during the ETL process.
- **Integration**: Integrate data from both source systems into a user-friendly and unified data model designed for analytical queries.
- **Scope**: The project focuses on latest sales data, including customer information, product details, and sales transactions.
- **Documentation**: Provide comprehensive documentation for the data model, ETL processes, and any transformations applied to the data.

## Medallion Architecture
The Medallion architecture is a layered approach to data management that organizes data into three distinct layers: Bronze, Silver, and Gold. Each layer serves a specific purpose in the data lifecycle, ensuring data quality and accessibility.

<img width="1674" height="758" alt="image" src="https://github.com/user-attachments/assets/32c9de0b-cbd7-4c9c-949a-20e02368b35a" />

### Bronze Layer
- **Data Ingestion**: Raw data is ingested from various sources, including databases.
- **Storage**: Data is stored in a raw format, preserving its original structure.
### Silver Layer
- **Data Cleaning**: Data is cleaned and transformed to ensure quality and consistency.
- **Storage**: Cleaned data is stored in a structured format, ready for analysis.
### Gold Layer
- **Data Aggregation**: Data is aggregated and summarized to create meaningful insights.
- **Storage**: Final datasets are stored in a format optimized for analytics and reporting.

## Project Structure
The project is organized into the following directories:
```
├── datasets
│   ├── source_crm
│   |    ├── cust_info.csv
│   |    ├── prd_info.csv
│   |    ├── sales_details.csv
│   ├── source_erp
│   |    ├── CUST_AZ12.csv
│   |    ├── LOC_A101.csv
│   |    ├── PX_CAT_GV1V2.csv
├── src
│   ├── bronze
│   |    ├── ddl_bronze.sql
│   |    ├── proc_load_bronze.sql
│   ├── silver
│   |    ├── ddl_silver.sql
│   |    ├── proc_load_silver.sql
│   ├── gold
│   |    ├── ddl_gold.sql
|   ├── init_database.sql
├── tests
│   ├── quality_checks_gold.sql
│   ├── quality_checks_silver.sql
├── README.md 
```
     

