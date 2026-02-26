# Azure-Data-Pipeline-for-Trip-Analytics-using-Delta-Lake

## 📌 Overview
This project implements an end-to-end Azure data engineering pipeline to process and analyze trip transaction and ride rating data. The solution follows the Medallion Architecture (Bronze → Silver → Gold) and leverages Azure cloud services to automate ingestion, transformation, validation, and reporting.

The objective is to build a scalable and resilient analytics pipeline that enables structured insights into customer behavior, driver performance, trip trends, and payment analytics.

---

## 🏗️ Architecture

The pipeline is designed using:

- **Bronze Layer** – Raw data ingestion from Azure SQL Database into ADLS Gen2 (Delta format)
- **Silver Layer** – Cleaned and transformed data using Azure Databricks (PySpark)
- **Gold Layer** – Aggregated and analytics-ready data stored as Delta tables

Data flows from Azure SQL → ADF → ADLS → Databricks → Delta Lake (Gold).

---

## ⚙️ Tech Stack

**Languages:** Python, SQL, Spark  
**Package:** PySpark  
**Services:**
- Azure Data Factory (ADF)
- Azure Databricks
- Azure Data Lake Storage Gen2 (ADLS)
- Azure SQL Database
- Azure Logic Apps
- Delta Lake

---

## 🔄 Pipeline Workflow

1. **Data Ingestion**
   - ADF pipelines replicate trip transactions and ride ratings data from Azure SQL Database to ADLS Gen2 (Bronze layer).
   - Supports scheduled execution and monitoring.

2. **Data Transformation**
   - Azure Databricks notebooks perform cleaning, validation, enrichment, and aggregations.
   - Data stored in Delta format for ACID compliance and schema enforcement.

3. **Data Aggregation (Gold Layer)**
   - Business metrics generated:
     - Customer trip patterns
     - Driver performance insights
     - Total trip distance analysis
     - Payment status tracking
     - Ratings trends

4. **Automation & Resiliency**
   - ADF triggers and scheduling for orchestration
   - Logic Apps for automated email notifications on pipeline success/failure
   - Monitoring through ADF pipeline runs

---

## 🔐 Delta Lake Features Used

- ACID Transactions
- Schema Enforcement
- Time Travel
- Data Versioning
- Optimized Query Performance

---

## 📊 Data Model

Fact & Dimension modeling implemented:

**Dimensions:**
- Customer Dimension
- Driver Dimension
- Date Dimension
- Payment Status Dimension

**Facts:**
- Trip Transaction Fact
- Ride Rating Fact

---

## 📈 Business Value

- Automated raw-to-analytics data movement
- Structured and reliable data processing using Delta Lake
- Improved visibility into trip behavior and driver performance
- Reduced manual intervention via scheduled orchestration
- Enabled analytics-ready reporting through Gold layer tables

---

## 🚀 Key Learnings

- Designing scalable Azure data pipelines
- Implementing Medallion Architecture
- Using Delta Lake for reliable data lakes
- Orchestrating workflows with Azure Data Factory
- Building resilient pipelines with Logic Apps alerts

---

## 📌 Future Improvements

- Implement incremental load optimizations
- Add data quality validation framework
- Integrate CI/CD for Databricks notebooks
- Build Power BI dashboard layer on Gold tables

---
