🛒 Walmart Sales Data Engineering Pipeline (End-to-End ETL)
🔍 Overview

This project implements a production-style batch ETL pipeline for Walmart sales data using PySpark and Databricks, following the Medallion (Bronze–Silver–Gold) architecture.
The pipeline ingests raw sales data, applies data quality checks and transformations, and produces analytics-ready datasets for business reporting.

🎯 Business Problem

Retail organizations need reliable, scalable, and cost-efficient pipelines to analyze sales performance across stores, products, and time periods.

Challenges addressed:

Large-volume data processing

Data quality and consistency

Incremental processing

Analytics-ready outputs for BI teams

🧠 Solution Approach

Designed a layered ETL architecture (Bronze → Silver → Gold)

Implemented incremental processing using Spark optimizations

Applied data validation rules to ensure correctness

Optimized Spark jobs for performance and cost

🏗 Architecture
Source Data
   │
   ▼
Bronze Layer (Raw Ingestion)
   │  - Schema enforcement
   │  - Raw data storage
   ▼
Silver Layer (Cleaned & Enriched)
   │  - Null handling
   │  - Type casting
   │  - Business rules
   ▼
Gold Layer (Analytics Ready)
   - Aggregated sales metrics
   - KPIs for reporting

🛠 Tech Stack

Language: Python

Processing: PySpark

Platform: Databricks

Storage: Delta Lake

Architecture: Medallion (Bronze–Silver–Gold)

🚀 Pipeline Features

Batch ETL with scalable Spark jobs

Schema validation & null checks

Repartitioning and caching for performance

Idempotent transformations

Analytics-ready fact tables

📊 Example KPIs Produced

Total sales per store

Weekly & monthly revenue trends

Product-level performance

Store-wise contribution to revenue

⚡ Performance Optimization

Optimized joins using broadcast hints

Reduced shuffles via proper partitioning

Cached intermediate datasets

Used column pruning & predicate pushdown

🧪 Data Quality Checks

Schema validation

Null & duplicate detection

Row count reconciliation between layers

📈 Results

Processed large-scale sales data efficiently

Reduced transformation runtime through Spark tuning

Delivered clean, analytics-ready datasets for BI consumption

🔮 Future Improvements

Airflow orchestration

Incremental loads using Delta Lake MERGE

Automated data quality alerts

BI dashboard integration

👤 Author

Tushar Patgar
Data Engineer | PySpark | Databricks | AWS
