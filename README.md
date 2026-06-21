# Healthcare Data Engineering Pipeline using Azure Databricks

This project demonstrates an end-to-end Healthcare Data Engineering Pipeline using Azure Data Factory, Azure Data Lake Storage Gen2, Azure Databricks, PySpark, Delta Lake, Azure SQL Database, and Power BI.

## Architecture

Healthcare CSV Source Files → Azure Data Factory → ADLS Bronze → Azure Databricks/PySpark → Silver Delta Tables → Gold Delta Tables → Azure SQL Database → Power BI

## Tools Used

- Azure Data Factory
- Azure Data Lake Storage Gen2
- Azure Databricks
- PySpark
- Delta Lake
- Azure SQL Database
- Power BI

## Key Features

- Azure Data Factory orchestration
- Azure Data Lake Storage Gen2 (Bronze, Silver, Gold)
- Azure Databricks notebooks
- PySpark transformations
- Delta Lake implementation
- Data quality validation
- Azure SQL Database integration
- Power BI reporting
- Medallion Architecture

## Dataset

This project uses a publicly available synthetic healthcare dataset obtained from Kaggle for educational and portfolio purposes.

The dataset is ingested using Azure Data Factory into Azure Data Lake Storage Gen2 and processed in Azure Databricks using PySpark and Delta Lake before being loaded into Azure SQL Database for reporting and analytics.

## Project Workflow

1. Download healthcare dataset from Kaggle.
2. Ingest raw CSV into Azure Data Lake Storage Gen2 using Azure Data Factory.
3. Store raw data in the Bronze layer.
4. Clean and transform the data using Azure Databricks and PySpark.
5. Store validated data in Silver Delta tables.
6. Create Gold business-ready datasets.
7. Load curated data into Azure SQL Database.
8. Build reporting dashboards in Power BI.

