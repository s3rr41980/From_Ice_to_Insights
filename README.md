## 🧊 From Ice to Insights – NHL Analytics Pipeline

****This project simulates a production-level data pipeline using Microsoft Fabric to process, transform, and analyse NHL game data. Designed and implemented an end-to-end metadata-driven ingestion data pipeline in Microsoft Fabric using a medallion (Bronze–Silver–Gold) architecture. The solution automates dynamic landing zone creation, performs incremental ingestion, enforces data quality using Great Expectations, handles SCD Type 2 for historical tracking, refreshes a Power BI semantic model, and provides Teams-based alerting and observability.****
---

## 📊 Data Sources
- **CSV Data (Azure Blob Storage):** Simulated raw game and player datasets from Kaggle representing production ingestion

---

## 🛠 Tech Stack
- **Platform:** Microsoft Fabric, Azure
- **Storage:** Delta Lakehouse, Azure Blob Storage
- **Processing Enging:** Notebooks (Spark Runtime), Data Pipelines, SQL Analytics Endpoint
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

## 🧩 Data Modelling (Constellion Schema)
- **Initial Challenge:** Discovered that dimensional modelling was more complex than anticipated, requiring a deeper understanding of relationships, keys, and granularity
- **Leveraging Kimball Principle:** → Applied Kimball’s methodology to map initial facts and dimensions in Excel, iterating through multiple schema proposals
- **Ambiguous Columns:** → Addressed ambiguity where attributes could belong to either fact or dimension tables, refining definitions for consistency
- **Understanding Granularity:** → Ensured each fact table maintained a consistent level of detail, supporting accurate joins and aggregations
- **Near Misses:** → Faced several divergent schema designs before achieving alignment between fact tables and conformed dimensions
- **Success through Refinement:** → Through iterative comparison and validation, finalised a robust Galaxy Schema that supports analytical flexibility and scalability

---

## 🌟 Key Features
- **Optimization:** Parallel execution and strategic load patterns (overwrite, incremental, upsert)
- **Scalable:** Parameterized ingestion with dynamic adaptation
- **Quality:** Automated data-quality check, fault tolerant, idempotent and deduplication
- **Monitoring:** Automated failure handling, error alerts, and logging
- **Data Modelling:** Fact constellation schema
- **Data Lineage:** Partitioned landing zone for CDC, SCD Type 2, Delta time travel
- **Compliance & Reliability:** RBAC, RLS/CLS, data masking, OneLake Security, OneLake ZRS (12 9s durability)

---

## 🎓 Skills Demonstrated
Microsoft Fabric · Databricks · PySpark · Azure Blob · Delta Lake · Power BI · SQL Analytics · OneLake · Great Expectations · Data Modelling · SCD Type 2 · Data Quality Automation
