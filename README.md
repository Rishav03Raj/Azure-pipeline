# Azure Data Engineering Project – Healthcare Revenue Cycle Management

## 📌 Project Overview
This project demonstrates an **end-to-end Data Engineering pipeline** built on **Azure Cloud** for **Healthcare Revenue Cycle Management (RCM)**. It simulates how raw healthcare datasets (Electronic Medical Records, Claims, ICD Codes) are ingested, transformed, and stored in a scalable platform for **analytics and reporting**.

The pipeline follows the **Medallion Architecture** (Bronze → Silver → Gold) with **Delta Lake**, ensuring **automation, scalability, and governance**.

---

## 🏗️ Architecture

**1. Data Ingestion (Bronze Layer)**
- Raw data files ingested from on-prem into **Azure Data Lake Storage Gen2 (ADLS)**.
- **Azure Data Factory (ADF)** pipelines handle extraction and loading.

**2. Data Transformation (Silver Layer)**
- **Azure Databricks (PySpark notebooks)** cleans, integrates, and standardizes data.
- **Slowly Changing Dimension (SCD) Type-II** applied to preserve history of claims & patients.

**3. Data Modeling & Aggregation (Gold Layer)**
- Built a **Star Schema** in **Azure SQL Database**.
- **Fact tables**: Claims, Transactions
- **Dimension tables**: Patients, Providers, ICD Codes

**4. Orchestration & Security**
- Automated using **ADF Triggers**.
- **Azure Key Vault** secures all credentials & connections.

---

## ⚙️ Tools & Technologies
- **Cloud**: Azure Data Factory, Azure Data Lake Gen2, Azure Databricks, Azure SQL Database, Azure Key Vault  
- **Programming**: Python, PySpark, SQL  
- **Data Modeling**: Star Schema, SCD Type-II  
- **Architecture**: Medallion (Bronze → Silver → Gold)

---

## 🔄 Workflow
1. **Extract & Load** → ADF pulls raw healthcare data → Bronze (Raw Layer).  
2. **Clean & Transform** → Databricks processes & enriches → Silver (Cleaned Layer).  
3. **Aggregate & Model** → Curated data stored in SQL DB → Gold (Analytics Layer).  
4. **Orchestrate** → ADF Triggers for automation & monitoring.  
5. **Secure** → Secrets managed by Azure Key Vault.  

---

## 📊 Outcomes
- Built a **scalable & automated ETL pipeline** for healthcare RCM datasets.  
- Enabled **historical tracking** of patients & claims using SCD-II.  
- Established a **robust foundation** for BI, Reporting & ML analytics.  

---

## 📂 Repository Structure
```bash
azure-data-engineering-project
 ┣ 📂 notebooks/       # Databricks notebooks for transformation
 ┣ 📂 pipelines/       # ADF pipeline JSON definitions
 ┣ 📂 sql/             # SQL queries & DDL scripts
 ┣ 📂 reports/         # Power BI dashboards (pbix files)
 ┣ 📄 architecture.png # Project architecture diagram
 ┣ 📄 README.md        # Documentation
```

---

## 🚀 Future Enhancements
- Integration with **Power BI / Tableau** for interactive dashboards.  
- Add **real-time streaming ingestion** with Kafka + Azure Event Hubs.  
- Expand into **predictive analytics** using ML on curated Gold layer.  

---

## 👨‍💻 Author
**Rishav Raj**  
B.Tech CSE | Data Engineering & AI Enthusiast  
🔗 [LinkedIn](#) | [GitHub](#)
