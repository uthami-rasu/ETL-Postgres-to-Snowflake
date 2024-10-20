### Data Pipeline Documentation

#### Overview

“A simplified ETL process for extracting, transforming, and loading data from AWS S3 to Snowflake, utilizing Amazon RDS, Apache Spark, Databricks, and Delta tables.”

#### Pipeline Steps

1. **Extract from S3**: 
   - Retrieve raw data from AWS S3.

2. **Load to RDS**: 
   - Store the extracted data in Amazon RDS for structured management.

3. **Read from RDS**: 
   - Retrieve relevant tables for transformation from Amazon RDS.

4. **Write to Delta Tables**: 
   - Save the retrieved data into Delta tables for reliable storage.

5. **Transform Data**: 
   - Add columns, remove unnecessary columns, and clean and aggregate data to meet business needs.

6. **Load to Snowflake**: 
   - Transfer the transformed data to Snowflake for analytics.

#### Conclusion
This pipeline effectively transitions data from S3 to Snowflake, optimizing it for analysis and reporting.


#### ETL Workflow Diagram 

![Workflow](Diagrams\ER Diagram.png)

#### ER Diagram 
