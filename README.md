# From_Ice_to_Insights

**Overview**
This project simulates a production-level data pipeline using Microsoft Fabric to process, transform, and analyse NHL game data. It implements a Medallion Architecture (Bronze → Silver → Gold) for ingestion, transformation, and visualisation, enabling faster, data-driven insights into player and team performance.

**Architecture**
Medallion Layers:
- Bronze Lakehouse (Landing Zone): Ingest raw CSV data from Azure Blob Storage.
- Silver Lakehouse (Processed Zone): Clean, transform, and standardise data into a relational schema for machine learning or downstream analytics.
- Gold Lakehouse (Analytics Zone): Model facts and dimensions for Power BI visualisation and advanced reporting.
Environment: Dev → Test → Prod Lakehouses

**Key Features**
**Source**: CSV data in Azure Blob Storage simulating production ingestion
**Architecture**: Medallion Architecture on Lakehouses with Dev-Test-Prod environments
**Optimization**: Parallel execution and strategic load patterns (overwrite, incremental, upsert)
**Scalable**: Parameterized ingestion with dynamic adaptation
**Quality**: Automated data-quality check, fault tolerant, idempotent and deduplication
**Monitoring**: Automated failure handling, error alerts, and logging
**Data Modellin**g: Fact constellation schema
**Data Lineage**: Partitioned landing zone for CDC, SCD Type 2, Delta time travel
**Compliance & Reliability**: RBAC, RLS/CLS, data masking, OneLake ZRS (12 9s durability)
