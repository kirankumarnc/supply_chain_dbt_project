# Supply Chain Data Pipeline (Snowflake + dbt)

## Project Overview

A batch data pipeline that ingests, transforms, and serves supply chain datasets
for reporting and analytics. Raw CSV files are loaded from AWS S3 into Snowflake
and transformed through a medallion architecture using dbt (Data Build Tool).

The pipeline covers three core datasets:
- **Item Inventory** — Product details, category, variant, and fuel type
- **Customer Orders** — Order details, customer info, product, and warehouse mapping
- **Warehouse Locations** — Static master data managed via dbt seed

---

## Business Objectives

- Automate ingestion of raw CSV files from S3 into Snowflake.
- Standardize and clean data for downstream consumption.
- Maintain historical data through incremental processing and snapshots.
- Enable self-service analytics using curated Gold-layer datasets.
- Support production deployment and scheduled execution through dbt Cloud.

---
## Tech Stack

| Tool | Purpose |
|---|---|
| **Snowflake** | Cloud data warehouse |
| **dbt Cloud** | Data transformation and documentation |
| **AWS S3** | Source file storage |
| **GitHub** | Version control and collaboration |

---

## Architecture

Data flows through five layers:

