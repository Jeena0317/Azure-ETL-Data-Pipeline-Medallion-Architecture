# Superstore Data Pipeline – Medallion Architecture

## Overview

This project demonstrates an **end-to-end data pipeline** using **Azure Data Factory (ADF)** and **Azure Data Lake Storage Gen2 (ADLS Gen2)**.  
It follows **Medallion Architecture** (Bronze → Silver → Gold) to ingest, clean, and aggregate data for analytics.

**Dataset:** Superstore Sales Dataset (CSV)

---

## Technologies Used

- Azure Data Factory (ADF)  
- Azure Data Lake Storage Gen2 (ADLS Gen2)  
- Parquet File Format  
- Mapping Data Flows (for transformations)  

---

## Architecture & Folder Structure
superstore-data/
├── bronze/raw/ # Raw CSV data
├── silver/cleaned/ # Cleaned & transformed data
└── gold/aggregated/ # Aggregated datasets


---

## Pipeline Workflow

1. **Bronze Layer** – Ingest raw CSV into ADLS using ADF.  
2. **Silver Layer** – Clean and transform data:
   - Correct data types (Sales → Decimal, Quantity → Integer)  
   - Filter invalid rows  
   - Add derived columns (YearMonth, ProfitMargin)  
3. **Gold Layer** – Aggregate data:
   - Total Sales by Month  
   - Profit by Category  
   - Revenue by Region  

---

## Key Features

- Clear **Bronze/Silver/Gold layers** for structured data  
- Scalable and reusable **ADF pipelines**  
- **Data validation** between layers  
- Optimized storage using **Parquet and partitioning**  

---

## Outcome

- Structured, analytics-ready datasets in ADLS  
- Ready for reporting or further analysis  
- Demonstrates real-world **Data Engineering best practices**  

---



## Author

**Jeena Paul** – Aspiring Data Engineer  
