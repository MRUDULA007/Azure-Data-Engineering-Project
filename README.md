# ✨🚀 End-to-End Data Engineering Pipeline on Azure
This repository showcases a complete end-to-end data engineering solution built using Azure's modern data tools. The project demonstrates how to ingest, process, transform, and visualize data for Business Intelligence (BI) needs. It utilizes the AdventureWorks dataset (sourced from GitHub) and leverages key Azure services including:

- Azure Data Factory – for data ingestion
- Azure Databricks – for data transformation
- Azure Synapse Analytics – for data warehousing
- Power BI – for reporting and visualization


Explore this project to understand how various Azure services can be integrated to build a scalable and efficient data pipeline.

![image alt](https://github.com/MRUDULA007/Azure-Data-Engineering-Project/blob/660619a80438917e39271ce5e36016e880c9f58c/adw1.png)

## 🧠 Architecture Overview

### ⚙️ Step 1: Azure Environment Setup

The following Azure services were provisioned for building the pipeline:

- **Azure Data Factory (ADF):** Orchestrates and automates data workflows  
- **Azure Storage Account:** Serves as a data lake with Bronze (raw), Silver (processed), and Gold (curated) layers  
- **Azure Databricks:** Executes data processing and transformations  
- **Azure Synapse Analytics:** Manages warehousing for BI consumption  

All resources were secured and integrated using appropriate **IAM roles** for seamless access and security.

---

### 🚀 Step 2: Data Ingestion with Azure Data Factory

ADF functions as the pipeline's orchestrator, managing the flow of data from source to storage.

- **Dynamic Copy Activity:**  
  - Data was pulled directly from GitHub using the HTTP connector  
  - Stored in the **bronze** layer of Azure Storage  
  - Pipeline parameters allow flexibility for future data source changes  

➡️ At this stage, the raw data is securely ingested and ready for transformation.

---

### 🔄 Step 3: Data Transformation with Azure Databricks

Azure Databricks was used to clean, normalize, and process the raw data from the bronze layer.

#### Key Highlights:
- **Cluster Setup:** Created a Databricks cluster for efficient processing  
- **Azure Storage Integration:** Connected to data lake for accessing raw files  

#### Data Processing Steps:
- Standardized date formats  
- Filtered out incomplete or incorrect records  
- Grouped and aggregated data for analysis  
- Saved results as **Parquet files** in the **silver** container for optimal performance

---

### 📊 Step 4: Data Warehousing with Azure Synapse Analytics

Processed data from the silver layer was structured for analysis using Synapse.

#### Implementation Steps:
- Connected Synapse to Azure Storage  
- Used **serverless SQL pools** to query data efficiently  
- Created **external tables** and **views** for BI access  
- Organized data into structured **databases and schemas**  

Final curated data was stored in the **gold** layer, ready for reporting.

---

### 🕵️‍♂️ Step 5: Visualization with Power BI

To deliver business value, the data was visualized using **Power BI**:

- Connected Power BI to **Azure Synapse Analytics**  
- Designed interactive **dashboards and reports**  
- Shared actionable insights with business stakeholders  

---

## 🌟 Key Highlights

This project demonstrates how to build a scalable and efficient Azure-based data engineering pipeline, featuring:

- **Automation:** Smooth data orchestration across all stages  
- **Scalability:** Handles large datasets with minimal overhead  
- **Optimization:** Uses Parquet format and serverless queries for performance  
- **Insights:** Delivers meaningful reports using Power BI  

This architecture exemplifies how cloud-native tools can turn raw data into strategic business insights.

---

## 🎉 Acknowledgment

This project is inspired by an excellent GitHub repository by **Ansh Lamba**.  
For a full walkthrough, check out his [YouTube channel](https://www.youtube.com/).  
Special thanks to Ansh for sharing such valuable knowledge and guidance for the data engineering community!
