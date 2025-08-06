# ☁️🔄 Azure End-to-End Data Engineering Pipeline with ADF, Databricks, Synapse & Power BI 📊🚀

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
- **Azure Storage Account:** Serves as a data lake with Bronze 🥉 (raw), Silver 🥈 (processed), and Gold 🥇 (curated) layers  
- **Azure Databricks:** Executes data processing and transformations  
- **Azure Synapse Analytics:** Manages warehousing for BI consumption  

All resources were secured and integrated using appropriate **IAM roles** for seamless access and security.
![image alt](https://github.com/MRUDULA007/Azure-Data-Engineering-Project/blob/3b945fbf6d496b009ad2a7412ddd8f199f1f4501/azure%20environment%20.png)
---

### 🔄 Step 2: Data Ingestion with Azure Data Factory

ADF functions as the pipeline's orchestrator, managing the flow of data from source to storage.

- **Dynamic Copy Activity:**  
  - Data was pulled directly from GitHub using the HTTP connector  
  - Stored in the **bronze** layer🥉 of Azure Storage  
  - Pipeline parameters allow flexibility for future data source changes  
![image alt](https://github.com/MRUDULA007/Azure-Data-Engineering-Project/blob/3b945fbf6d496b009ad2a7412ddd8f199f1f4501/dynamic%20copy.png)
➡️ At this stage, the raw data is securely ingested and ready for transformation.
![image alt](https://github.com/MRUDULA007/Azure-Data-Engineering-Project/blob/3b945fbf6d496b009ad2a7412ddd8f199f1f4501/bronze%20containers%20data%20lake.png)
---

### 🛠️ Step 3: Data Transformation with Azure Databricks

Azure Databricks was used to clean, normalize, and process the raw data from the bronze layer.

#### Key Highlights:
- **Cluster Setup:** Created a Databricks cluster for efficient processing  
- **Azure Storage Integration:** Connected to data lake for accessing raw files  
![image alt](https://github.com/MRUDULA007/Azure-Data-Engineering-Project/blob/3b945fbf6d496b009ad2a7412ddd8f199f1f4501/adw%20databricks.png)

#### Data Processing Steps:
- Standardized date formats  
- Filtered out incomplete or incorrect records  
- Grouped and aggregated data for analysis  
- Saved results as **Parquet files** in the **silver** 🥈 container for optimal performance
![image alt](https://github.com/MRUDULA007/Azure-Data-Engineering-Project/blob/3b945fbf6d496b009ad2a7412ddd8f199f1f4501/db%20transformations.png)
![image alt](https://github.com/MRUDULA007/Azure-Data-Engineering-Project/blob/3b945fbf6d496b009ad2a7412ddd8f199f1f4501/silver%20containers%20datalake.png)
---

### 📊 Step 4: Data Warehousing with Azure Synapse Analytics

Processed data from the silver layer was structured for analysis using Synapse.

#### Implementation Steps:
- Connected Synapse to Azure Storage  
- Used **serverless SQL pools** to query data efficiently  
- Created **external tables** and **views** for BI access  
- Organized data into structured **databases and schemas**  
![image alt](https://github.com/MRUDULA007/Azure-Data-Engineering-Project/blob/3b945fbf6d496b009ad2a7412ddd8f199f1f4501/synapse1.png)
![image alt](https://github.com/MRUDULA007/Azure-Data-Engineering-Project/blob/3b945fbf6d496b009ad2a7412ddd8f199f1f4501/synapse2.png)
Final curated data was stored in the **gold** layer🥇, ready for reporting.
![image alt](https://github.com/MRUDULA007/Azure-Data-Engineering-Project/blob/3b945fbf6d496b009ad2a7412ddd8f199f1f4501/gold%20container%20datalake.png)
---

### 🕵️‍♂️ Step 5: Visualization with Power BI

To deliver business value, the data was visualized using **Power BI**:

- Connected Power BI to **Azure Synapse Analytics**  
- Designed interactive **dashboards and reports**  
- Shared actionable insights with business stakeholders  
![image alt](https://github.com/MRUDULA007/Azure-Data-Engineering-Project/blob/1a7bc6b1c8c38c50457844fee966477488fb3c22/pbi%201.png)
---

## 🌟 Key Highlights

This project demonstrates how to build a scalable and efficient Azure-based data engineering pipeline, featuring:

- **Automation:** Smooth data orchestration across all stages  
- **Scalability:** Handles large datasets with minimal overhead  
- **Optimization:** Uses Parquet format and serverless queries for performance  
- **Insights:** Delivers meaningful reports using Power BI  

This architecture exemplifies how cloud-native tools can turn raw data into strategic business insights.

---

##### 🎉 Acknowledgment
This project is inspired by an excellent GitHub repository by **Ansh Lamba**.  
