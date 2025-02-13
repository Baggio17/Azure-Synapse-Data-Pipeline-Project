# **Azure Synapse Data Pipeline Project**

## **Project Overview**

This project demonstrates my expertise in Azure Synapse Analytics, showcasing my ability to design, build, and optimize data pipelines for real-world applications. Using the 2021 Tokyo Olympics dataset, I implemented a scalable data pipeline that integrates Azure Data Lake Gen2, Synapse Dedicated SQL Pool, and Power BI for seamless data ingestion, transformation, and visualization.

This project is part of my professional portfolio, aimed at highlighting my proficiency in cloud-based data engineering and analytics. It underscores my ability to handle large-scale data solutions, unify big data and data warehousing, and derive actionable insights—all essential skills for modern data engineering roles.

## **Why This Project is Important**

Azure Synapse Analytics is a leading solution for unified analytics. This project showcases my ability to:

**Design Scalable Pipelines:** Ingest, transform, and store data efficiently in a cloud-based environment.

**Integrate Big Data and Warehousing:** Seamlessly connect Azure Data Lake Gen2 with Synapse SQL Pools for high-performance analytics.

**Enable Business Insights:** Leverage Power BI to transform raw data into meaningful visualizations.

**Handle Real-World Data:** Work with multi-faceted datasets to solve business problems and showcase actionable outcomes.

## **Project Workflow**

**1. Dataset and Tools Used**

**Dataset:** Tokyo 2021 Olympics (Athletes, Coaches, Gender Entries, Medals, Teams)

**Tools:**

Azure Synapse Analytics (SQL Pools, Pipelines, Integration with Power BI)

Azure Data Lake Storage Gen2

Power BI Desktop
![resources](https://github.com/user-attachments/assets/abfb2ba8-81e6-4018-b366-a84836dff027)


**2. Project Architecture**

Step 1: Store raw data files in Azure Data Lake Gen2.

Step 2: Build an Azure Synapse pipeline to load data into Synapse Dedicated SQL Pools.

Step 3: Create SQL tables for the dataset and transform data for reporting.

Step 4: Use Power BI to visualize insights from the loaded data.
![Screenshot (98)](https://github.com/user-attachments/assets/1cfa9ed7-7331-4ca5-908c-f08bcaf14162)


## **Step-by-Step Implementation**

**Step 1: Azure Data Lake Gen2 Setup**

Set up: Azure Data Lake Gen2 for scalable and secure storage.

Configured: a container named "source".

Uploaded: the 5 dataset files (Athletes.csv, Coaches.csv, EntriesGender.csv, Medals.csv, Teams.csv) to the container.

**Step 2: Azure Synapse Workspace and SQL Pool**

Created Synapse Workspace:

Set up the workspace and linked it to the storage account.

Created a dedicated SQL Pool for high-performance querying and storage.

**Step 3: Table Creation in SQL Pool**

Defined and executed: SQL scripts to create tables for each dataset:

sql
CREATE TABLE [dbo].[AthletesOlympics] (
  [PersonName] NVARCHAR(100),
  [Country] NVARCHAR(100),
  [Discipline] NVARCHAR(100)
);
(Repeated for all datasets: Coaches, EntriesGender, Medals, Teams)

**Step 4: Data Pipeline in Synapse**

In Synapse Studio, created a new pipeline named "Ingesting Athlete Data".

Used Copy Data activity to connect to Azure Data Lake Gen2 and select files.

Connected to the Synapse SQL Pool and mapped each file to its respective table.

Tested the pipeline: using the Debug option to ensure data is ingested into the SQL tables.

Cloned the pipeline to replicate the process for the remaining files but I could have used the "Get Metadata" Activity + "ForEach Activity" + "Copy Data" Activity to dynamically copy the remaining files.
![pipelines](https://github.com/user-attachments/assets/9d83efaf-5918-4f08-b3a9-6f65139b87f6)


**Step 5: Power BI Visualization**

Used Power BI Desktop to connect to Synapse SQL Pool and access the tables.

Built interactive dashboards to analyze.

Published the dashboard for easy sharing and access via Azure Synapse Studio.
![powerbi 2](https://github.com/user-attachments/assets/7b55de83-3b9e-4e3d-bc22-c314a42b2218)
![powerbi 1](https://github.com/user-attachments/assets/e279bb8b-ceb5-4115-9252-3a5f3864cba0)
![power bi 3](https://github.com/user-attachments/assets/829a409e-cf07-41ac-9782-18133cf3613f)

**Results and Outputs**

SQL Tables: Data from all five datasets ingested into Synapse SQL Pool.

Power BI Dashboard:

Medal distribution by country and event.

Gender representation in the Olympics.


**Conclusion**

This project exemplifies my ability to use Azure Synapse Analytics for end-to-end data engineering, from storage and processing to visualization. By showcasing this project, I aim to demonstrate my readiness to design and implement scalable, cloud-based data solutions—an essential skill for any data engineering role.

