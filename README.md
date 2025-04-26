# Data Engineering Project with Azure DevOps, Unity Catalog, Delta Live Table

## Overview

This project demonstrates the creation of an **end-to-end Azure Data Engineering solution** leveraging **Azure Data Factory (ADF)**, **Azure Databricks**, **Azure DevOps**, and **Unity Catalog** for data orchestration, processing, and management. The goal was to build a scalable and automated pipeline that ingests, transforms, and stores data in Azure Data Lake and Delta Lake, applying best practices such as **CI/CD** for seamless deployment and integration.

## Project Details

### Key Components:
- **Azure Data Factory (ADF)**: Used for orchestrating the data pipeline and ingesting data from external sources (GitHub API) into **Azure Data Lake (Bronze layer)**.
- **Azure Databricks**: Used to perform data transformations such as **null handling**, **type conversions**, **deduplication**, and **window functions** in **PySpark**.
- **Delta Lake**: Data is stored in **Delta format** for optimized querying and performance.
- **Delta Live Table (DLT)**: Used for building reliable streaming pipelines in the Gold layer, enabling real-time data processing.
- **CI/CD via Azure DevOps**: Automated the entire workflow for seamless data pipeline deployment, version control, and continuous integration.

### Tech Stack:
- **Azure Data Factory (ADF)**
- **Azure Databricks**
- **Unity Catalog**
- **Delta Lake**
- **Delta Live Table (DLT)**
- **Azure DevOps (CI/CD)**

## Project Setup

### Prerequisites

1. **Azure Account**: Make sure you have an active Azure subscription.
2. **Azure Databricks Workspace**: Set up a Databricks workspace within your Azure subscription.
3. **Azure Data Factory (ADF)**: Set up an ADF instance for orchestration and pipeline management.
4. **GitHub**: A GitHub repository from which the data (CSV files) will be ingested.

### Steps to Set Up the Project:

1. **Azure Data Factory Setup**:
   - Create an **Azure Data Factory** instance.
   - Set up a **GitHub-linked dataset** to pull CSV files from a GitHub repository into Azure Data Lake (Bronze layer).
   - Create pipelines in ADF that extract the data from the GitHub API and store it in **Azure Data Lake (Bronze layer)**.

2. **Azure Databricks Setup**:
   - Set up an **Azure Databricks workspace** and create a new cluster.
   - Create **notebooks** in Databricks to perform transformations on the ingested data:
     - Handle null values.
     - Perform type conversion.
     - Apply deduplication.
     - Execute window functions.
   - Store the transformed data in **Delta Lake** (Silver layer).

3. **Delta Live Table (DLT)**:
   - Set up **Delta Live Table (DLT)** pipelines to continuously stream and process data.
   - Store processed data in the **Gold layer** (curated tables) for reporting and further analysis.

4. **Azure DevOps**:
   - Set up **Azure DevOps** for continuous integration and deployment (CI/CD).
   - Automate the deployment of **Azure Data Factory** pipelines and **Databricks** notebooks.
   - Use **Azure DevOps pipelines** to ensure that the data engineering workflow is automated, version-controlled, and scalable.

### Running the Project:

1. **Data Ingestion**:
   - The pipeline is triggered in **Azure Data Factory** to ingest CSV files from the **GitHub API** into **Azure Data Lake**.
   
2. **Data Transformation**:
   - The data in the **Bronze layer** is cleaned and transformed in **Azure Databricks** using **PySpark**.
   
3. **Data Storage**:
   - The transformed data is stored in **Delta format** in the **Silver layer** for further analysis.
   
4. **Streaming**:
   - The **Delta Live Table** pipelines process and stream data into the **Gold layer**, creating curated tables.

5. **CI/CD**:
   - The entire process is automated via **Azure DevOps** for continuous deployment and integration.



