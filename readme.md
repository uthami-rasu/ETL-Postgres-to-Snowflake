

# ETL Pipeline Documentation

## Overview

The primary objective of this project is to facilitate efficient data transformation from **PostgreSQL** (hosted on **AWS RDS**) to **Snowflake**. By leveraging **Databricks**, we ensure effective data processing and handling, with transformed data being thoroughly cleaned and validated. **Amazon S3** serves as the data lake, providing scalable storage solutions for our raw data. Additionally, **Amazon CloudWatch** is employed for comprehensive logging and monitoring of data flows. The architecture utilizes a **star schema** in Snowflake, enhancing data accessibility and supporting informed decision-making through streamlined analytics.

## Pipeline Steps

1. **Extract from S3**: 
   - Retrieve raw data from AWS S3.

2. **Load to RDS**: 
   - Store the extracted data in Amazon RDS for structured management.

3. **Read from RDS**: 
   - Retrieve relevant tables for transformation from Amazon RDS.

4. **Write to Delta Tables**: 
   - Save the retrieved data into Delta tables for reliable storage.

5. **Transform Data**: 
   - Enhance the data by adding and removing columns, and performing cleaning and aggregation to meet business requirements.

6. **Load to Snowflake**: 
   - Transfer the transformed data to Snowflake for analytics.

## Conclusion

This pipeline effectively transitions data from S3 to Snowflake, optimizing it for analysis and reporting. The structured approach ensures data integrity and accessibility, enabling data-driven decision-making.

## ETL Workflow Diagram 

![Workflow](https://raw.githubusercontent.com/Razzkutty/S3-to-Snowflake-ETL-Pipeline/refs/heads/main/Diagrams/ETL%20Workflow.png)

## ER Diagram 
![ER Diagram](https://github.com/Razzkutty/S3-to-Snowflake-ETL-Pipeline/blob/main/Diagrams/ER%20Diagram.png)
