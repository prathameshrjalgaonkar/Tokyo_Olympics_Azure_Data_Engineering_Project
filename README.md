# Tokyo_Olympics_Azure_Data_Engineering_Project

## Overview
This project demonstrates an end-to-end data engineering pipeline built using various Azure services, including Azure Data Factory, Azure Databricks, and Azure Synapse Analytics. The goal is to extract, transform, and analyze data from the Tokyo Olympics 2021 to provide insights into the performance of athletes, countries, and events.

## Architecture
The architecture follows a typical ETL (Extract, Transform, Load) process:
1. Extract: Data is extracted from a public dataset using Azure Data Factory.
2. Transform: Data is transformed using Apache Spark within Azure Databricks, including cleaning, deduplication, and enrichment.
3. Load: Transformed data is stored in Azure Data Lake Storage for analysis.
4. Analyze: Azure Synapse Analytics is used for running SQL queries on the transformed data.
5. Visualize: The results are visualized using Power BI for dashboards and reports.

## Dataset
The dataset used in this project comes from the Tokyo 2021 Olympics, available on [Kaggle](https://www.kaggle.com). It includes data on:
- Athletes
- Coaches
- Events
- Medals
- Teams

### Data Files:
- `athletes.csv`: Details of athletes participating in the Tokyo Olympics.
- `coaches.csv`: Information about the coaches.
- `medals.csv`: Medal tally data for each country.
- `teams.csv`: Teams participating in different events.
- `entries_gender.csv`: Gender-wise participation in events.

## Azure Services Used
- Azure Data Factory: To build and orchestrate the data pipeline, extracting data from the source and loading it into Azure Data Lake Storage.
- Azure Databricks: For transforming the data using Apache Spark.
- Azure Data Lake Storage (Gen2): For storing both raw and transformed data.
- Azure Synapse Analytics: For querying and analyzing the transformed data using SQL.
- Power BI: For visualizing the insights and creating dashboards.

## Steps Involved
### 1. Data Ingestion
- Use Azure Data Factory to ingest raw data from a GitHub repository or Kaggle dataset into Azure Data Lake Storage.

### 2. Data Transformation
- Leverage Databricks and Apache Spark to clean and transform the raw data:
    - Remove duplicates
    - Normalize data formats
    - Aggregate data by country, event, and athlete

### 3. Data Analysis
- Use Azure Synapse Analytics to perform SQL-based analysis on the transformed data.
- Example queries include:
    - Counting the total number of athletes by country
    - Aggregating medal counts for each country

### 4. Data Visualization
- Connect Power BI to Azure Synapse Analytics to create visualizations, such as:
    - Medal tallies per country
    - Gender participation by sport

## How to Run the Project
### Prerequisites
- Azure account with access to Data Factory, Databricks, Synapse Analytics, and Data Lake Storage
- Basic knowledge of Python, SQL, and Apache Spark

### Setup
1. Clone this repository to your local machine.
2. Set up Azure services as described in the architecture:
    - Create a Data Lake Storage account.
    - Create a Data Factory pipeline.
    - Set up Databricks for data transformation.
    - Connect Synapse Analytics to query the transformed data.
3. Ingest the data into the raw storage and proceed with transformation and analysis.

### Running the Pipeline
1. Start by triggering the Data Factory pipeline to copy raw data to the storage.
2. Execute the transformation jobs in Databricks using Apache Spark.
3. Query the transformed data using Synapse Analytics and visualize results in Power BI.

## Conclusion
This project demonstrates the power of Azure cloud services for building a scalable and efficient data engineering pipeline. The Tokyo Olympics dataset serves as a case study for handling large-scale, real-world data in an end-to-end manner, from extraction to visualization.

