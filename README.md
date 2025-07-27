# 🏗️ SQL Server Data Warehouse (Bronze → Silver → Gold)  

## 📌 Overview  
This project implements a **modern data warehouse architecture** on **SQL Server**, following the **Bronze → Silver → Gold** layered approach.  
The solution is designed for **scalable, reliable, and maintainable data pipelines** that transform raw data into high-quality analytics-ready datasets.  

---

## 🔥 Architecture  
The data warehouse follows a **three-layered architecture**:  

1. **Bronze Layer (Raw Ingestion)**  
   - Stores raw, unprocessed data from various sources (CSV, APIs, transactional DBs, etc.).  
   - Data is loaded as-is for traceability and auditing.  
   - Typically stored in staging tables.  

2. **Silver Layer (Cleansed & Conformed)**  
   - Cleanses, deduplicates, and standardizes data.  
   - Implements business rules and joins multiple raw datasets into a **conformed model**.  
   - Serves as a reliable source for downstream analytics.  

3. **Gold Layer (Curated & Aggregated)**  
   - Contains **business-ready, analytics-friendly datasets**.  
   - Data is aggregated, enriched, and optimized for reporting tools (Power BI, Tableau, etc.).  
   - Supports KPI dashboards and advanced analytics.  

---

## 🔄 Data Flow  
```mermaid
flowchart LR
    Source[Data Sources] --> Bronze[Bronze Layer<br>(Raw Tables)]
    Bronze --> Silver[Silver Layer<br>(Cleansed & Modeled Tables)]
    Silver --> Gold[Gold Layer<br>(Curated Data Marts)]
    Gold --> BI[Reporting & Analytics]
