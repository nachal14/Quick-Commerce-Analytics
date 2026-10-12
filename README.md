# 🛵 Quick Commerce Analytics & Automated Data Pipeline

An end-to-end data analytics and engineering project investigating unit economics, delivery performance, dark-store inventory bottlenecks, and customer churn in a 10-minute quick commerce model.

---

## 🎯 Business Context & Stakeholder Problem

Quick commerce operates on razor-thin margins and aggressive service-level agreements (SLAs). In a 10-minute delivery environment, a single delayed order can drive customer churn, while dark-store stockouts lead directly to lost revenue.

**Core Business Questions Addressed:**
* **Delivery Performance:** Where and when do fulfillment delays happen, and do they directly impact ratings and customer retention?
* **Dark Store Inventory:** Where do stockouts and overstocking cause the most financial friction?
* **Customer Behavior:** Who are the high-value repeat customers, and which segments are at immediate risk of churn (RFM Modeling)?
* **Pricing & Promotions:** Which campaigns drive net-incremental volume versus those that erode product margins?

---

## 🏗️ Architecture & Technical Stack

Raw CSV Files
│
▼
Python ETL Pipeline (Pandas, SQLAlchemy, PyODBC, Pathlib, Argparse)
│  ├── Chunked Batch Ingestion (chunksize=1000)
│  ├── Connection Pooling & Dynamic Schema Building
│  └── Idempotent Lifecycle Management (if_exists='replace')
▼
Microsoft SQL Server Database (Relational Schema)
│
▼
SQL Analytical Views, Window Functions & CTEs
│
▼
Python Predictive Modeling & Power BI Dashboards

* **Data Pipeline / ETL:** Python (`pandas`, `sqlalchemy`, `pyodbc`, `pathlib`, `argparse`)
* **Database & Data Modeling:** Microsoft SQL Server (SSMS)
* **Analytics & Business Intelligence:** SQL (CTEs, Window Functions), Python (`scikit-learn`, `statsmodels`), Power BI

---

## 📁 Repository Structure

```text
├── data/                       # Local raw datasets (CSVs)
├── scripts/
│   └── data_loading.py         # Automated Python ETL pipeline script
├── sql/
│   ├── schema/                 # Staging tables and database creation DDL
│   └── analytics/              # Analytical SQL queries, CTEs, and RFM views
├── dashboards/                 # Power BI (.pbix) reports and visuals
├── requirements.txt            # Python dependencies
└── README.md                   # Project documentation



