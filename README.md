# 🚗 Vehicle Insurance Claims Analytics Platform

## 📌 Overview
This project is an end-to-end **Data Engineering pipeline** built using **Databricks, PySpark, and Delta Lake** following the **Medallion Architecture (Bronze, Silver, Gold)**.

The platform processes raw vehicle insurance data and transforms it into **business-ready insights** for:
- Claims analysis  
- Risk assessment  
- Fraud detection  
- Operational reporting  

---

## 🎯 Problem Statement
Insurance data is often:
- Distributed across multiple systems  
- Inconsistent and unclean (nulls, duplicates)  
- Difficult to analyze for fraud and risk  

This leads to:
- Delayed decision-making  
- Poor visibility into claims performance  
- Challenges in identifying high-risk customers  

---

## 🎯 Objective
- Build a scalable data pipeline  
- Clean and standardize raw data  
- Generate analytics-ready datasets  
- Provide KPIs for business decision-making  

---

## 📂 Datasets Used
The project uses 6 core datasets:

- **Claims** → claim details (amount, status, date)  
- **Customers** → customer information and risk category  
- **Policies** → policy and premium details  
- **Payments** → claim payment transactions  
- **Vehicles** → vehicle details  
- **FNOL (First Notice of Loss)** → incident reporting data  

These datasets together represent the **complete insurance claim lifecycle**.

---

## 🏗️ Architecture
The project follows **Medallion Architecture**:

### 🥉 Bronze Layer (Raw Data)
- Data ingested from S3 (CSV format)  
- Stored in Delta tables  
- No transformations applied  
- Acts as the **source of truth**  

---

### 🥈 Silver Layer (Cleaned Data)
- Removed duplicates using business keys  
- Handled null and missing values  
- Standardized formats (text, dates)  
- Filtered invalid records (negative values, future dates)  

Ensures **high-quality, reliable data**.

---

### 🥇 Gold Layer (Business Layer)
- Joined all datasets into a unified view  
- Created analytics-ready datasets  
- Generated business KPIs  

This layer is used for **dashboards and reporting**.

---

## 📊 Key KPIs
The platform generates the following insights:

- **Total & Average Claim Amount** → financial overview  
- **Settlement Rate** → operational efficiency  
- **Average Payment per Claim** → cost tracking  
- **Policy Claim Ratio** → profitability analysis  
- **Vehicle-wise Claims** → risk segmentation  
- **FNOL Conversion Rate** → process efficiency  
- **Repeat Claims** → suspicious activity detection  
- **High Claim Outliers** → anomaly detection  

---

## 📈 Dashboard
A dashboard is built on top of Gold layer data to:
- Visualize KPIs  
- Monitor claims performance  
- Identify risk patterns  
- Enable quick decision-making  

---

## ⚙️ Technologies Used
- **Databricks**  
- **PySpark**  
- **Delta Lake**   
- **Unity Catalog**  
- **S3 (Data Source)**  

---

## 🚀 Advanced Concepts Implemented
- **Delta Lake ACID Transactions**  
- **Time Travel** for historical data access  
- **Schema Evolution**  
- **SCD Type 2** for tracking changes  
- **Idempotent Processing**  
- **Exactly-Once Data Handling**  
- **Medallion Architecture Design Pattern**  

---

## ⚠️ Challenges Faced
- Handling missing and inconsistent data  
- Removing duplicates across datasets  
- Standardizing formats  
- Managing schema inconsistencies  

---

## 💼 Business Impact
- Improved fraud detection  
- Better risk analysis  
- Faster and data-driven decisions  
- Optimized claim processing costs  

---

## ✅ Conclusion
This project demonstrates how raw insurance data can be transformed into **meaningful business insights** using a scalable and robust data engineering pipeline.

It highlights the importance of:
- Data quality  
- Structured architecture  
- Business-focused analytics
## 👨‍💻 Author
**Your Name**  
Data Engineering Enthusiast
