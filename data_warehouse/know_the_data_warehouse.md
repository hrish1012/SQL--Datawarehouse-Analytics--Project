# 📁 Data Warehouse Project Structure

This document explains the folder and file structure of the **data_warehouse** project and the purpose of each component.

---

## 📘 doc/
This folder contains all **visual and design documentation** related to the project.  
It includes diagrams and representations used to explain:
- Data integration from CRM and ERP sources
- End-to-end data flow
- Overall data warehouse architecture (Bronze–Silver–Gold)

These visuals help in understanding the system design and data movement across layers.

---

## 🧩 scripts/
This folder contains all SQL scripts used to implement the **Medallion Architecture**.  
Each subfolder represents one layer of the data warehouse.
scripts/
├── bronze/
├── silver/
└── gold/

### 🥉 bronze/
Contains SQL scripts related to the Bronze (raw data) layer.

- `ddl_bronze.sql`  
  Defines the DDL for creating all Bronze schema tables.

- `proc_load_bronze.sql`  
  Contains a stored procedure responsible for loading raw data from both CRM and ERP source systems into the Bronze tables.

---

### 🥈 silver/
Contains SQL scripts related to the Silver (cleaned and standardized) layer.

- `ddl_silver.sql`  
  Defines the DDL for creating all Silver schema tables.

- `proc_load_silver.sql`  
  Contains a stored procedure that transforms data from the Bronze layer and loads it into the Silver schema tables.

---

### 🥇 gold/
Contains SQL scripts related to the Gold (business-ready) layer.

- `ddl_gold.sql`  
  Contains the DDL for creating Gold layer views that represent business-ready dimensions and fact views for analytics.

---

## 🧪 test/
This folder contains SQL scripts used for **data quality validation**.

- `quality_checks_silver.sql`  
  Includes SQL queries executed to validate data quality, consistency, and correctness in the Silver layer.

- `quality_checks_gold.sql`  
  Includes SQL queries used to verify data accuracy and integrity in the Gold layer views.

---

