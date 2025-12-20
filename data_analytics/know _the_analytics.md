# 📊 Data Analytics Project

This project contains a structured collection of **SQL analytics scripts** designed to explore, analyze, and derive insights from a relational data warehouse.  
The analytics are primarily performed on **business-ready (Gold layer) views** and focus on common analytical patterns used by data analysts and BI professionals.

---

## 📁 scripts/
The `scripts` folder contains SQL files organized in a **logical execution and learning order**, starting from basic data exploration to advanced analytical reporting.

---

## 📄 Analytics Scripts Description

- **01_database_exploration.sql**  
  Performs initial exploration of the database, including table inspection, row counts, and overall data understanding.

- **02_dimensions_exploration.sql**  
  Explores dimension data such as customers and products to understand attributes and distributions.

- **03_date_range_exploration.sql**  
  Analyzes date ranges available in the data to identify time coverage and data completeness.

- **04_measures_exploration.sql**  
  Examines key measures such as sales, quantity, and pricing metrics.

- **05_magnitude_analysis.sql**  
  Analyzes the magnitude of metrics to understand scale, volume, and contribution.

- **06_ranking_analysis.sql**  
  Uses ranking logic to identify top and bottom entities (e.g., top customers, top products).

- **07_change_over_time_analysis.sql**  
  Analyzes how metrics change over time to identify trends and patterns.

- **08_cumulative_analysis.sql**  
  Performs cumulative and running total analysis using SQL window functions.

- **09_performance_analysis.sql**  
  Evaluates performance across different dimensions such as customers, products, or time periods.

- **10_data_segmentation.sql**  
  Segments data into meaningful groups to support targeted analysis and insights.

- **11_part_to_whole_analysis.sql**  
  Analyzes contribution of individual segments to overall totals (part-to-whole relationships).

---

## 📑 Customer Analytics Report (`12_report_customers.sql`)

This script generates a **customer-focused analytical report** by aggregating and analyzing customer-level data.  
It provides insights such as:
- Customer contribution to overall sales
- Customer performance metrics
- Identification of high-value and low-value customers
- Customer segmentation for analytical insights

This report is designed to support **customer behavior analysis and business decision-making**.

---

## 📦 Product Analytics Report (`13_report_products.sql`)

This script generates a **product-focused analytical report** by aggregating and analyzing product-level data.  
It provides insights such as:
- Product sales and revenue performance
- Top- and bottom-performing products
- Category and subcategory analysis
- Product contribution to overall business metrics

This report supports **product performance evaluation and portfolio analysis**.

---

## 🎯 Purpose of This Project

- Demonstrate practical **SQL-based data analytics skills**
- Apply common **analytical patterns** used in real-world projects
- Enable structured exploration and reporting on business-ready data
- Serve as a reference for **data analysis, BI, and interview preparation**

---

This project showcases a **systematic approach to data analytics using SQL**, progressing from exploration to insight-driven reporting.

