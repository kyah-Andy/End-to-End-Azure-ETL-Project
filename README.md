# End-to-End Azure ETL Project

## 📌 Overview
This repository demonstrates an **end-to-end ETL pipeline on Microsoft Azure**, implementing the **Medallion Architecture (Bronze → Silver → Gold)**. It showcases how raw data is ingested, transformed, curated, and visualized using Azure services such as **ADF, Data Lake, Databricks, Synapse Analytics, and Power BI**.

The project is designed for **data engineering portfolio development**, highlighting secure connections via **Azure Key Vault** and best practices in building scalable ETL pipelines.

---

## 🏗️ Architecture
The pipeline follows a layered approach:

### **1. Data Extraction (Bronze Layer)**
- **Source:** SQL Server (SSMS)
- **Tool:** Azure Data Factory (ADF)
- Raw data stored in Azure Data Lake (**Bronze**)

### **2. Transformation (Silver Layer)**
- **Tool:** Databricks Notebooks  
- Cleans and standardizes raw data  
- Output stored in Azure Data Lake (**Silver**)

### **3. Curation (Gold Layer)**
- **Tool:** Databricks Notebooks  
- Business-ready transformations (e.g., header cleaning)  
- Output stored in Azure Data Lake (**Gold**)

### **4. Analytics & Reporting**
- **Azure Synapse Analytics:** Gold layer views created for reporting  
- **Power BI:** Dashboards built from Synapse views  

### **5. Security**
- All connections managed via **Azure Key Vault**

---

## 📂 Repository Structure

```text
End-to-End-Azure-ETL-Project/
│
├── ADF/                  # Data Factory pipelines
├── Architecture/         # Flowcharts & architecture diagrams
├── Data/                 # Sample datasets
├── Databricks/Notebooks/ # Transformation notebooks
├── PowerBi/              # Dashboard files
├── Synapse Analytics/    # SQL views and scripts
├── docs/                 # Documentation
└── README.md             # Project overview
```
---

## 🚀 Getting Started

### Prerequisites

#### Azure subscription with access to:
- Azure Data Factory  
- Azure Data Lake Storage  
- Azure Databricks  
- Azure Synapse Analytics  
- Power BI  

#### Other tools:
- SQL Server Management Studio (SSMS) for source extraction  
- Basic knowledge of Python, SQL, and Power BI  

---

### Setup Steps

1. Clone the repository:
   ```bash
   git clone https://github.com/kyah-Andy/End-to-End-Azure-ETL-Project.git
2. Backup AdventureWorksLT2022.bk file from `/data` into SSMS
3. Deploy ADF pipelines from `/ADF`.
4. Check Databricks notebooks from `/Databricks/Notebooks` to transform data (Automatic run by ADF pipeline).
5. Create Synapse views using scripts in `/Synapse Analytics`.
6. Connect Power BI to Synapse and build dashboards from `/PowerBi`.

---

## 📊 Dashboard Highlights
- Number of products   
- Number of Sales 
- costumer per title  
- Product Sales Performance  
- Inactive Customer Tracking
- Top Order sales

---

## 🔒 Security
All secrets (connection strings, credentials) are stored in **Azure Key Vault**.

Pipelines and notebooks reference secrets securely, ensuring compliance with best practices.

---

## 🎯 Use Cases
- Portfolio demonstration for data engineering roles  
- Learning resource for Azure ETL pipeline design  
- Template for enterprise-grade data workflows  

---

## 👨‍💻 Author
**Andy S. Razon**
