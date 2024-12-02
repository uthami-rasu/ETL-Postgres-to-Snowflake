
---
# ETL Pipeline: PostgreSQL to Snowflake

## Overview
This project demonstrates the creation of a scalable **ETL (Extract, Transform, Load)** pipeline to efficiently process and transform data from **PostgreSQL (AWS RDS)** into **Snowflake**. The pipeline leverages **Databricks**, **AWS S3**, **Amazon CloudWatch**, and **Snowflake**, employing a **star schema** for efficient analytics and reporting.

## Objectives
- **Efficient Data Transformation**: Clean, aggregate, and format data during the transformation process.
- **Data Integrity and Quality**: Ensure accurate and consistent data is ready for analysis.
- **Optimized Performance**: Handle large datasets with scalability.

---

## Tools and Technologies
- **PostgreSQL (AWS RDS)**: For structured data storage and management.
- **Databricks**: Distributed data processing and transformation.
- **AWS S3**: Data lake for raw data storage.
- **Amazon CloudWatch**: Monitoring and logging operations.
- **Snowflake**: Cloud-based analytics platform with a star schema architecture.
- **Delta Tables**: Reliable and incremental data processing.
- **Power BI**: Visualization and reporting of analytics data.

---
## ETL Workflow Diagram 

![Workflow](https://raw.githubusercontent.com/Razzkutty/S3-to-Snowflake-ETL-Pipeline/refs/heads/main/Diagrams/ETL%20Workflow.png)

## Pipeline Workflow

### 1. Extract Data from AWS S3
- **Tools**: Databricks, AWS S3, Python
- **Process**: Retrieve raw data (CSV) from AWS S3.

### 2. Load Data into PostgreSQL (RDS)
- **Tools**: Databricks, PostgreSQL  
- **Process**: Load raw data into PostgreSQL for structured storage.

### 3.  Read Data from PostgreSQL and Write to Delta Tables
- **Tools**: Databricks, PostgreSQL, Delta Lake  
- **Process**: Establish a JDBC connection to PostgreSQL from Databricks, query relevant data using  PySpark, and save the retrieved data into Delta Tables. This ensures reliable storage with ACID compliance, enabling incremental processing for further transformations.  

### 5. Transform Data
- **Tools**: Databricks, PySpark, Spark SQL  
- **Process**: Clean, deduplicate, and transform data based on business requirements.

### 6. Load Transformed Data into Snowflake
- **Tools**: Databricks, Snowflake  
- **Process**: Store transformed data in Snowflake using a star schema.

---

## Snowflake Architecture
- **Star Schema**: Optimized for analytics.  
  - **Fact Tables**: Aggregate numerical data.  
  - **Dimension Tables**: Descriptive attributes.
 
## ER Diagram 
![ER Diagram](https://github.com/Razzkutty/S3-to-Snowflake-ETL-Pipeline/blob/main/Diagrams/ER%20Diagram.png)

This architecture ensures fast query performance and simplifies data joins.

---

## Monitoring and Logging
- **Amazon CloudWatch**: Tracks pipeline stages for errors, anomalies, and performance metrics.  
- **Features**:
  - Logs for error resolution.
  - Monitoring alerts for proactive issue detection.

![Logging](https://raw.githubusercontent.com/uthami-rasu/ETL-Postgres-to-Snowflake/refs/heads/main/Diagrams/function%20logs.png)
![Logging](https://raw.githubusercontent.com/uthami-rasu/ETL-Postgres-to-Snowflake/refs/heads/main/Diagrams/logs.png)

---

## Outcome and Dashboard
- **Data Visualization**: A **Power BI dashboard** connects to Snowflake to display KPIs and actionable insights.  
- **Stakeholder Benefits**: Accurate, up-to-date data for informed decision-making.
  
![Dashboard](https://raw.githubusercontent.com/uthami-rasu/ETL-Postgres-to-Snowflake/refs/heads/main/Diagrams/Project-01%20DashBoard.png)

---

## Key Learnings
- Building scalable ETL pipelines.
- Integrating cloud platforms like AWS, Databricks, and Snowflake.
- Using Delta Tables for reliable incremental processing.
- Implementing star schemas for analytics.
- Automating workflows and monitoring with CloudWatch.

---

## Contact
For questions or collaboration, please reach out at uthamirasuv@gmail.com.



