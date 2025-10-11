# From_Ice_to_Insights

🧊 From Ice to Insights – NHL Analytics Pipeline
This project simulates a production-level data pipeline using Microsoft Fabric to process, transform, and analyse NHL game data. It implements a Medallion Architecture (Bronze → Silver → Gold) for ingestion, transformation, and visualisation, enabling faster, data-driven insights into player and team performance.

---

## 📊 Data Sources
- **CSV Data (Azure Blob Storage):** Simulated raw game and player datasets from Kaggle representing production ingestion

---

## 🛠 Tech Stack
- **Platform:** Microsoft Fabric, Azure
- **Storage:** Delta Lakehouse, Azure Blob Storage
- **Processing Enging:** PySpark, SQL Analytics Endpoint
- **Data Quality & Validation:** Great Expectations  
- **Security & Compliance:** RBAC, OneLake Security, RLS/CLS, Data Masking
- **Visualisation**: Power BI

---

## 🔄 Pipeline Workflow
- **Dynamic Landing Zone Creation:** Automatically provisions a partitioned folder structure (by execution date) in Fabric Lakehouse for traceable raw ingestion whenever the pipeline runs
- **Metadata-Driven Ingestion:** Dynamically retrieves and processes file metadata, enabling fully parameterised and scalable ingestion across datasets
- **Bronze Load (Raw to Delta):** Performs full and incremental loads into the Bronze layer (Delta format) based on the latest partitioned folder in the landing zone
- **Data Quality Validation:** Integrates Great Expectations to enforce automated data-quality checks for validity, completeness, and conformity
- **Promotion to Silver Layer:** Cleanses, structures, and standardises datasets replicated from Bronze for downstream consumption
- **Gold Layer Load:** Applies SCD Type 2 logic for player and team dimension tables to track historical changes, and incremental updates for fact tables
- **Semantic Model Refresh:** Triggers Power BI dataset and semantic model refresh for up-to-date analytics and dashboards
- **Automated Monitoring & Alerts:** Sends success and failure notifications to Microsoft Teams, while logging failure metrics for observability and pipeline reliability

---

## 🧩 Architecture
Medallion Layers:
Bronze Lakehouse (Landing Zone): Ingest raw CSV data from Azure Blob Storage
Silver Lakehouse (Processed Zone): Cleanse, transform, and standardise data into relational schema
Gold Lakehouse (Analytics Zone): Model facts and dimensions for Power BI visualisation
Environment: Dev → Test → Prod

---

## 🌟 Key Features
- **Optimization:** Parallel execution and strategic load patterns (overwrite, incremental, upsert)
- **Scalable:** Parameterized ingestion with dynamic adaptation
- **Quality:** Automated data-quality check, fault tolerant, idempotent and deduplication
- **Monitoring:** Automated failure handling, error alerts, and logging
- **Data Modelling:** Fact constellation schema
- **Data Lineage:** Partitioned landing zone for CDC, SCD Type 2, Delta time travel
- **Compliance & Reliability:** RBAC, RLS/CLS, data masking, OneLake ZRS (12 9s durability)

---

## 🎓 Skills Demonstrated
Microsoft Fabric · Databricks · PySpark · Azure Blob · Delta Lake · Power BI · SQL Analytics · OneLake · Great Expectations · Data Modelling · SCD Type 2 · Data Quality Automation
