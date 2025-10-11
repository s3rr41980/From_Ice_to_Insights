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
Ingest CSV files from Azure Blob into Bronze Lakehouse (Landing Zone)
Transform data in Silver Lakehouse (Processed Zone) with cleansing, schema evolution, and deduplication
Load enriched and modelled tables into Gold Lakehouse (Analytics Zone) for consumption
Model fact and dimension tables following a Fact Constellation Schema
Implement SCD Type 2 tracking and Delta Time Travel for historical accuracy
Visualise insights in Power BI for player performance and game analytics

---

## 🧩 Architecture
Medallion Layers:
Bronze Lakehouse (Landing Zone): Ingest raw CSV data from Azure Blob Storage
Silver Lakehouse (Processed Zone): Cleanse, transform, and standardise data into relational schema
Gold Lakehouse (Analytics Zone): Model facts and dimensions for Power BI visualisation
Environment: Dev → Test → Prod

---

## 🌟 Key Features
Automated Orchestration: Parameterised ingestion and dynamic partitioning
Data Quality: Fault-tolerant, idempotent, and deduplication-enabled workflows
Scalability: Supports incremental and upsert-based loading
Data Lineage: Partitioned landing zone for CDC and SCD Type 2 tracking
Observability: Error alerts, logging, and pipeline recovery
Security: RLS/CLS, masking, and role-based access

---

## 🎓 Skills Demonstrated
Microsoft Fabric · Databricks · PySpark · Azure Blob · Delta Lake · Power BI · SQL Analytics · OneLake · Great Expectations · Data Modelling · SCD Type 2 · Data Quality Automation
