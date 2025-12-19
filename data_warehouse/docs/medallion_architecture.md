# 🏗️ Medallion Architecture – Project Implementation

## What is Medallion Architecture?
Medallion Architecture is a layered data design pattern commonly used in modern data warehousing.  
It organizes data into **Bronze, Silver, and Gold layers**, where each layer represents a different level of data refinement.  
This approach helps in maintaining data quality, scalability, and a clear separation between raw data, processed data, and business-ready data.

---

## 🥉 Bronze Layer (Raw Data)
The Bronze layer contains **6 raw tables** that store data ingested directly from the CRM and ERP source systems.  
Data in this layer is stored **as received**, without any transformation or validation, ensuring full traceability to the source.

**Bronze Tables:**
- bronze.crm_cust_info  
- bronze.crm_prd_info  
- bronze.crm_sales_details  
- bronze.erp_cust_az12  
- bronze.erp_loc_a101  
- bronze.erp_px_cat_g1v2  

---

## 🥈 Silver Layer (Cleaned & Standardized Data)
The Silver layer consists of cleaned and standardized tables created from the Bronze data and stored under the Silver schema.  
This layer applies data quality rules, standardization, and deduplication to prepare reliable datasets for analytics.

**Silver Tables:**
- silver.crm_cust_info  
- silver.crm_prd_info  
- silver.crm_sales_details  
- silver.erp_cust_az12  
- silver.erp_loc_a101  
- silver.erp_px_cat_g1v2  

---

## 🥇 Gold Layer (Business-Ready Data)
The Gold layer is implemented using **three SQL views** designed in a **Star Schema** format.  
These views apply business logic and aggregations to deliver analytics-ready data.

**Gold Views:**
- `gold.dim_customers` – Customer dimension integrating CRM and ERP data  
- `gold.dim_products` – Product dimension enriched with category details  
- `gold.fact_sales` – Sales fact view linked to customer and product dimensions  

---

This layered approach ensures **data quality, scalability, and a clear separation of responsibilities** across the data pipeline.

