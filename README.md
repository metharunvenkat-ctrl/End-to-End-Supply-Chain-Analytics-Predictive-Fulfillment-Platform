# End-to-End Supply Chain Analytics & Predictive Fulfillment Platform

An enterprise-grade, end-to-end data engineering, machine learning, and business intelligence project built on Databricks Community Edition, MLflow, and Power BI. This solution processes over 180,000+ supply chain records to identify logistical bottlenecks, forecast delivery risks, and optimize regional profitability.

---

## 🚀 High-Level Tech Stack & Architecture

* **Data Engineering & Lakehouse:** Databricks (PySpark, Delta Lake, Medallion Architecture: Bronze $\rightarrow$ Silver $\rightarrow$ Gold layers)
* **Machine Learning & Experiment Tracking:** MLflow for model registry and tracking predictive fulfillment risks
* **Business Intelligence & Visualization:** Power BI (DAX measures, Matrix heatmaps, Donut charts, Custom KPI cards)
* **Version Control & CI/CD:** GitHub, Databricks Git Folders, Power BI Project (`.pbip`) format

---

## 🔄 End-to-End Process & Workflow

### 1. Ingestion & Storage (Bronze Layer)
* Ingested raw supply chain operational feeds (comprising 180K+ order transactions) directly into the Databricks environment.
* Maintained raw fidelity with schema enforcement and audit timestamps.

### 2. Transformation & Cleansing (Silver Layer)
* Performed data cleaning, handled missing values, and standardized date-time attributes, shipping modes, and regional hierarchies using PySpark.
* Formatted transactional data into structured Delta tables optimized for downstream analytics.

### 3. Aggregation & Feature Engineering (Gold Layer)
* Aggregated metrics by region, product categories, and shipping modes to calculate key performance indicators:
  * Total Orders: **181K**
  * Total Late Orders: **99K**
  * Overall Late Delivery Rate: **54.83%**
  * Total Profit: **$3.97M**
* Engineered high-level summaries and risk metrics ready for BI consumption.

### 4. Predictive Modeling & Tracking (MLflow)
* Developed predictive classification pipelines to forecast late delivery likelihood based on shipping tiers and product characteristics.
* Tracked parameters, metrics, and model artifacts using **MLflow**.

### 5. Business Intelligence & Executive Dashboard (Power BI)
* Connected Power BI directly to the Gold layer aggregations using modern `.pbip` project architecture.
* Designed an executive-level dashboard featuring:
  * **Top KPI Cards:** Instant visibility into order volume, delay counts, overall delay percentages, and total profit.
  * **Regional Fulfillment Matrix:** Granular breakdown of late delivery rates across geographic regions and shipping classes.
  * **Product Category Trends:** Dual-axis analysis tracking profit and average actual shipping duration across product lines.
  * **Shipping Mode Breakdown:** Donut and bar visualizations segmenting fulfillment channels.

---

## 📊 Power BI Executive Dashboard

![Power BI Executive Dashboard](Screenshot%202026-09-08%20234050.png)

---

## 📂 Repository Structure

* `retail_purchase_project.ipynb`: Core PySpark data processing and pipeline notebook.
* `Supplychain_Bi_pbip.pbip` & associated folders: Power BI project source definition.
* `README.md`: Comprehensive project documentation.
