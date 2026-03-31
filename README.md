#  Retail Analytics Data Pipeline

## Overview
This project demonstrates a complete **end-to-end Data Engineering pipeline** built on Microsoft Azure to solve the problem of fragmented retail data.

The solution integrates **multi-source data** (SQL databases + REST APIs) into a centralized **Delta Lakehouse architecture**, enabling scalable processing and real-time analytics.

---

##  Key Features
- End-to-End ETL/ELT pipeline using Azure services
- Medallion Architecture (Bronze → Silver → Gold)
- Scalable data processing with PySpark (Databricks)
- ACID-compliant storage using Delta Lake
- Interactive dashboard for insights (Power BI)

---

##  Architecture
> Data flows through a modern architecture:

- **Ingestion Layer (ADF)**
- **Storage Layer (ADLS Gen2 / Delta Lake)**
- **Processing Layer (Azure Databricks - PySpark)**
- **Serving Layer (Power BI Dashboard)**

##  Tech Stack
- **Cloud:** Microsoft Azure  
- **Data Pipeline:** Azure Data Factory  
- **Processing:** Azure Databricks (PySpark)  
- **Storage:** Azure Data Lake Gen2 + Delta Lake  
- **Visualization:** Power BI  
- **Languages:** Python, SQL  


## 🔄 Data Pipeline Flow

### Data Ingestion (Bronze Layer)
- Connected to multiple data sources:
  - SQL Databases (Transactions, Products, Stores)
  - REST APIs (Customer data)
- Used Azure Data Factory pipelines for orchestration
- Stored raw data in **Parquet format** in ADLS Gen2
  

###  Data Transformation (Silver Layer)
- Cleaned and transformed data using **PySpark**
- Handled:
  - Missing values
  - Duplicate records (`dropDuplicates()`)
  - Data type consistency (`cast()`)
- Performed joins across multiple datasets:
  - Transactions
  - Customers
  - Products
  - Stores

- Created **Unified Sales Dataset**


###  Gold Layer
- Generated business metrics:
  - Total Revenue
  - Average Transaction Value (ATV)
  - Product Category Performance

- Stored final data as **Delta Tables**
- Enabled:
  - Incremental loads
  - Time travel
  - High-performance querying


##  Dashboard & Insights

Power BI dashboard provides key business insights:

-  **Revenue Analysis:** Total revenue reached $134.57K  
-  **Store Performance:** Identified top-performing outlets  
-  **Customer Behavior:** Category-wise purchase trends  
-  **KPI Tracking:** Sales, transactions, and growth metrics
  

##  Key Learnings
- Building scalable pipelines using Azure ecosystem  
- Implementing Medallion Architecture in real-world scenarios  
- Optimizing data storage using Delta Lake  
- Designing analytics-ready data models  
- End-to-end integration from ingestion to visualization


##  Conclusion
This project showcases a **production-style Data Engineering workflow**, transforming raw multi-source data into **actionable business insights** using modern cloud technologies.


##  Author
**Soban Munir**  
Aspiring Data Engineer  

- GitHub: https://github.com/soban-munir  
- LinkedIn: www.linkedin.com/in/soban-munir-89b64b333
