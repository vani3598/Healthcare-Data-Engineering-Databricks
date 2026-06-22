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

## Dataset Profile

- Records: 55,500
- Columns: 15
- Format: CSV
- Domain: Healthcare
- Source: Public synthetic healthcare dataset

The dataset contains patient demographics, hospital admissions, medical conditions, insurance information, medications, billing amounts, and laboratory outcomes. It is processed using Azure Databricks and PySpark following a Medallion Architecture.

## Storage Architecture

The project follows the Medallion Architecture pattern:

- **Bronze Layer** – Stores raw healthcare data exactly as received.
- **Silver Layer** – Stores cleaned and validated Delta tables after PySpark transformations.
- **Gold Layer** – Stores business-ready datasets used for reporting and analytics.

Azure Data Lake Storage Gen2 is used as the central storage platform for all three layers.

## Azure Data Factory

Azure Data Factory is used to orchestrate data ingestion into the Bronze layer of Azure Data Lake Storage Gen2.

### Pipeline Components

- Linked Service: `ls_adls_healthcare`
- Source Dataset: `ds_healthcare_csv`
- Sink Dataset: `ds_bronze_output`
- Pipeline: `pl_ingest_healthcare_csv`
- Activity: `copy_healthcare_to_bronze`

The pipeline can be extended with triggers, parameterization, and metadata-driven orchestration for enterprise-scale implementations.
