# Data Engineering End to End - Azure Data Factory

<B>Paris Olympics 2024 event</B>

<B>DESCRIPTION</B><BR>
This project provides a data engineering and anlytical journey on the Tokyo Olympic dataset. Starting with a CSV on GitHub, the data is ingested into the Azure ecosystem via Azure Data Factory. It's initially stored in Azure Data Lake Storage Gen2, then transformed in Azure Databricks. The enriched data, once again housed in ADLS Gen2, undergoes advanced analytics in Azure Synapse. The insights are finally visualized in Azure Synapse or Power BI, offering a comprehensive view of the dataset.

 <B>ARCHITECTURE</B><BR>

<b>Goal:</b> The goal of this project is to identify the trends in the previously organised olympic games, specifically to see the analysis and data visualisation for the athletes, medals, events etc.  By performing a data analysis using Data Flow in Azure Data Factory, this project aims to provide valuable insights that can help tell a story and assist in making informed decisions about the olympic games, which country won highest the number of medals, countries with the highest medals.

<b>Description:</b> This project analyzes 2.8 million rows of data using SQL and Excel to help an agency in Chicago improve service ticket resolution time by understanding where to focus their resources on first. After exploring the data, I create a priority quadrant based on two selected metrics, plot the data against the quadrant, cross-validate the findings with data from New York City, and deep-dive to find more patterns at district level.

Tools: PostgreSQL, Excel, and PowerPoint.

Skills: Data querying, data validation, JOINs & UNION clauses, aggregation, datetime convertion, filtering, subqueries, CTEs, conditions, PivotTables, Pivot Charts, and presentation.

Outputs:

Detailed SQL scripts with in-line comments in .sql format.
Excel workbook in .xlsx with multiple tabs covering data dictionary, data handling documentation, queried tables, pivot tables, and charts.
Presentation slides in .pdf format containing problem statement, data details, findings, summary, and additional remarks.
Tables

chicago_311_2020 - Chicago 311 service ticket data in 2020
Fields: 15
Records: 572,514
chicago_311_2019 - Chicago 311 service ticket data in 2019
Fields: 15
Records: 1,826,465
chicago_311_2018 - Chicago 311 service ticket data in 2018
Fields: 15
Records: 461,170
chicago_311_community_areas - Chicago community areas data (incompleted)
Fields: 2
Records: 7
nyc_311_2019 - New York City 311 service ticket data in 2019
Fields: 20
Records: 2,456,955
Acknowledgements

The data is stored in General Assembly's internal database but is also available on City of Chicago official data portal.
