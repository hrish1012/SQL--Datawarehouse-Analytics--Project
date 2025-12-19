## 📌 Overview

This folder contains **raw source data files** used to load the **Bronze layer** of the data warehouse.

The data originates from **two independent source systems**:

1. **CRM** (Customer Relationship Management)
2. **ERP** (Enterprise Resource Planning)

These datasets represent **unprocessed source data** and are ingested into corresponding **Bronze tables** before any cleansing or transformation.

---

## 🔹 CRM Source System Datasets

### 1️⃣ Customer Information  
**Target Table:** `bronze.crm_cust_info`

| Column             | Description                   |
| ------------------ | ----------------------------- |
| cst_id             | Unique customer identifier    |
| cst_key            | Business customer key         |
| cst_firstname      | Customer first name           |
| cst_lastname       | Customer last name            |
| cst_marital_status | Marital status                |
| cst_gndr           | Gender                        |
| cst_create_date    | Customer record creation date |

---

### 2️⃣ Product Information  
**Target Table:** `bronze.crm_prd_info`

| Column       | Description                  |
| ------------ | ---------------------------- |
| prd_id       | Unique product identifier    |
| prd_key      | Business product key         |
| prd_nm       | Product name                 |
| prd_cost     | Product cost                 |
| prd_line     | Product line / category      |
| prd_start_dt | Product effective start date |
| prd_end_dt   | Product effective end date   |

---

### 3️⃣ Sales Transactions  
**Target Table:** `bronze.crm_sales_details`

| Column       | Description                    |
| ------------ | ------------------------------ |
| sls_ord_num  | Sales order number             |
| sls_prd_key  | Product key                    |
| sls_cust_id  | Customer ID                    |
| sls_order_dt | Order date (integer format)    |
| sls_ship_dt  | Shipping date (integer format) |
| sls_due_dt   | Due date (integer format)      |
| sls_sales    | Total sales amount             |
| sls_quantity | Quantity sold                  |
| sls_price    | Unit price                     |

> ⚠ **Note:** Dates are stored as integers and are standardized in later layers.

---

## 🔹 ERP Source System Datasets

### 4️⃣ Customer Demographics  
**Target Table:** `bronze.erp_cust_az12`

| Column | Description         |
| ----- | ------------------- |
| cid   | Customer identifier |
| bdate | Birth date          |
| gen   | Gender              |

---

### 5️⃣ Customer Location  
**Target Table:** `bronze.erp_loc_a101`

| Column | Description         |
| ----- | ------------------- |
| cid   | Customer identifier |
| cntry | Country             |

---

### 6️⃣ Product Category Mapping  
**Target Table:** `bronze.erp_px_cat_g1v2`

| Column      | Description           |
| ----------- | --------------------- |
| id          | Product identifier    |
| cat         | Category              |
| subcat      | Sub-category          |
| maintenance | Maintenance indicator |
