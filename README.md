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

The complete workflow is broken down into several tasks, that are listed below:

1. Creation of Azure Subscription and Resource Group

2. Creation of a storage container. <br>
   An azure storage account (olympic-data) was setup and three folders were created, <b>input-data</b>, <b>raw-data</b>, and <b>transformed-data</b> were created within the storage account. The data analysis data used were ingested from this github account which can be found in the "Olympics_Data" folder.     

   ![iScreen Shoter - Google Chrome - 241021045746](https://github.com/user-attachments/assets/db649ba4-ced4-40e6-9e11-d46c9588d554)

3. Creation of Azure Data Factory Studio, launch the studio and carry out data ingestion. <br>
   
![iScreen Shoter - Google Chrome - 241021045316](https://github.com/user-attachments/assets/a18e4df4-225b-4b9f-887f-622f35a1da79)

Select pipeline and create a pipeline to ingest data, by creating a new dataset selecting HTTP as the data store with a corresponding linked service and use the github link to select the raw file for the olympic csv files. 

![iScreen Shoter - Google Chrome - 241021045922](https://github.com/user-attachments/assets/a3438d7b-5375-4be1-a65d-1b1f4414b10b)


After the raw files in csv format were linked as datasets, validatition should be carried out and then click on debug the pipeline should be triggered to ingest data for all data sets by successfully fetching the raw data and store it, as shown in the screenshots for 9 csv files. 

![iScreen Shoter - Google Chrome - 241021045434](https://github.com/user-attachments/assets/c52916d8-b636-4b34-8d39-7fdb0c715515)

The data is copied from the individual csv files to the datasets created as shown in the activity names, the status of the copy can be monitored to know when it is in progress, and if it succeeded or failed as seen in the screenshot above.

A successfully fetched data should look like the screen below, the files are listed in the storage bucket folder "raw-data" 

![iScreen Shoter - Google Chrome - 241021045702](https://github.com/user-attachments/assets/b9a79069-7074-4ded-8a13-97f245d1b70c)

4. The data ingestion is complete, and the next workflow task is data transformation. Data transformation will be carried out using Azure Databricks.
   
5. Azure Databricks is selected from the Azure portal and an Azure Databricks Workspace is created entering the subscription name, resource group, workspace name and managed resource name. The created account is connected to Azure storage Gen 2.

After the creation of databricks workspace, a notebook is created and codes were written to connect to the connect to the storage and mount the storage location, 

![iScreen Shoter - Google Chrome - 241021050327](https://github.com/user-attachments/assets/fa3e86dd-3b84-4865-a5e3-e77b85de5e1f)


6. The configuration settings are generated and included in the config code as seen below. necessary functions and types from pyspark are imported, then the azure storage configurations are defined, followed by the mounting of Azure data lake storage Gen2 to the databricks filesystem.
   
![Vector](https://github.com/user-attachments/assets/4f438790-ead8-4da4-8ac8-9869744d062c)

7. The csv files that were ingested into the storage container file directory "raw-data" is read into spark dataframes as seen in the screenshot below.

![iScreen Shoter - Google Chrome - 241023051559](https://github.com/user-attachments/assets/732e9573-04b4-40d9-a97c-e71d2537276d)

The content of a dataframe is shown to see the data as seen in the next screenshot.

![iScreen Shoter - Google Chrome - 241023051616](https://github.com/user-attachments/assets/09f3a573-c650-4237-9c9b-7bbf03d6d631)

After seeing the data, the schema is printed to review the schema if it requires modification. See the schema below for the dataframe shown above.

![iScreen Shoter - Google Chrome - 241023051630](https://github.com/user-attachments/assets/d3b3e534-e762-41cd-bef2-5f0a73036143)

Subsequently, all other dataframes are reviewed showing the contents and printing the schema as seen below for two dataframes.

![iScreen Shoter - Google Chrome - 241023051646](https://github.com/user-attachments/assets/e20b33da-0703-4eb0-8507-5de75276e7e3)


![iScreen Shoter - Google Chrome - 241023051915](https://github.com/user-attachments/assets/4c94ec4d-d804-4dde-9a96-0bcb20c037ef)

Looking at the medals dataframe above the code column has a string datatype, this column should be an integer, the column is then converted to the appropriate data type of integer as seen below.

![iScreen Shoter - Google Chrome - 241023051941](https://github.com/user-attachments/assets/230f1788-802d-424b-9ba7-63f753430af7)





Outputs:
The output was presented in Power BI as seen below: 

Data analysis using Power BI involves several steps to transform, visualize, and gain insights from the data. However, the transformation had already been carried out in Azure Databricks.

The following was performed in Power BI

Data Collection and Import: The data was imported from the processed data from Azure (ADF) as CSV.

Data Transformation and Cleaning: Date of birth column was used to generate the age column, conditional columns were created to analyse the medallists table.

Data Modeling: Relationships were created between tables (Athletes, Medallists, Medals Table). Primary and foreign keys were used to enable data modeling.

Data Visualization: Visualizations were built to help you understand the data. 

Data Analysis and Calculation: DAX (Data Analysis Expressions) was used to create calculated columns and measures that provide deeper insights into the data. DAX is a formula language specific to Power BI.

Dashboard Creation: Visualizations were assembled into a cohesive dashboard consisting of the following visuals, slicers, with a user-friendly layout for easy consumption.

Interactivity: Filters, slicers, and drill-through actions were put in place. 

![Dashboard](https://github.com/user-attachments/assets/3fe43757-1860-4cb3-8715-9cfccd0a2dcf)

[Olympics Dashboard 2024.pdf](https://github.com/user-attachments/files/17793985/Olympics.Dashboard.2024.pdf)



