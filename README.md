# Data Engineering End to End - Azure Data Factory | Databricks | Azure Synapse Analytics | Power BI

<B>Paris Olympics 2024 event</B>

<B>DESCRIPTION</B><BR>
This project provides a data engineering and anlytical journey into the Olympic games dataset. Starting with CSVs on GitHub, the data is ingested into the Azure ecosystem via Azure Data Factory data pipelines. It's initially stored in Azure Blob Storage after which transformation is carried out in Databricks, and then moved to Azure Data Lake Storage Gen2. The enriched data, once again housed in ADLS Gen2, undergoes advanced analytics in Azure Synapse. The data is finally accessed for analysis in Azure Synapse after which visualization is carried out in Power BI, offering a comprehensive view of the dataset. 


 <B>ARCHITECTURE</B><BR>

<b>Goal:</b> The goal of this project is to identify the trends in the previously organised olympic games, specifically to see the analysis and data visualisation for the athletes, medals, events etc.  By performing a data analysis using Data Flow in Azure Data Factory, this project aims to provide valuable insights that can help tell a story and assist in making informed decisions about the olympic games, which country won highest the number of medals, countries with the highest medals.

A robust ETL pipeline is explored using a suite of azure services: Azure Data Factory, Azure Databricks, Azure synapse Analytics, and Azure Data Lake Storage Gen2. 

<B>Tools and Services : </B><BR>
Azure Data Factory  - Raw and transformed data storage, data integration service for data ingestion, transformatation. <BR>
Azure Databricks  - Data processing and transformation on an Apache Spark-based analytics platform. <BR>
Azure synapse Analytics  - Final data analysis carried out in the cloud-based analytics service using SQL queries. <BR>
Azure Data Lake Storage Gen2  - A scalable and secured could storage service built for data analytics <BR>
Power BI  - Data visualisation. <BR>

Skills: Azure(Data Ingestion, Transformation using Databricks, Azure Blob Storage for storage) Data querying, data validation, JOINs & UNION clauses, aggregation, datetime convertion, filtering, subqueries, CTEs, conditions, PivotTables, Pivot Charts, and presentation.

<B>Environment Set up: </B>

![setup-environment](https://github.com/user-attachments/assets/bfecc8b2-e2b3-4f66-a6e7-52f481dd5533)


<B>Workflow </B>




Outputs:
The output was presented in Power BI as seen below: 
