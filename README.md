# End-to-End Azure Data Engineering Pipeline

This project demonstrates a scalable end-to-end data engineering pipeline built on Microsoft Azure.
The pipeline ingests data from multiple sources, processes it using Databricks, and serves analytics-ready datasets for BI tools.
The architecture follows a Medallion (Bronze-Silver-Gold) design pattern.


## Tech Stack

- Azure Data Factory (Data Ingestion)
- Azure Data Lake Storage Gen2 (Raw & Processed Storage)
- Azure Databricks (Transformation)
- Azure Synapse Analytics (Serving Layer)
- MongoDB (Enrichment Source)
- Power BI (Visualization)
- Python / PySpark


  ## Pipeline Flow

1. Data Ingestion  
   - Data is ingested from HTTP APIs (GitHub) and SQL tables using Azure Data Factory.

2. Raw Storage (Bronze Layer)  
   - Raw data is stored in ADLS Gen2 without modification.

3. Transformation (Silver Layer)  
   - Data cleaning, schema enforcement, and enrichment using Azure Databricks (PySpark).

4. Enrichment  
   - External reference data from MongoDB is joined for additional attributes.

5. Gold Layer  
   - Aggregated and analytics-ready datasets stored back in ADLS Gen2.

6. Serving  
   - Azure Synapse is used to expose transformed data for BI tools.(in progress right not completed)

7. Visualization  
   - Power BI dashboards built on top of curated datasets.(in progress right not completed )


## Key Features

- Scalable cloud-based architecture
- Medallion data design (Bronze/Silver/Gold)
- Data enrichment from NoSQL source
- Optimized storage using Parquet format
- Analytics-ready serving layer
