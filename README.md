# Superstore Data Analysis using AWS
-------------------------------------------------------------

This project builds a pipeline to analyze Superstore sales data using the power of AWS. It transforms the data to make it ready for exploration. Querying the transformed data using SQL queries to uncover trends and patterns. Analyzing results and creates easy-to-understand visualizations, providing clear insights into Superstore sales performance.

#### AWS services used:

- IAM 
- S3
- AWS Glue
- AWS Athena
- AWS QuickSight

![Screenshot 2024-05-22 205016](https://github.com/bhavanachitragar/Superstore-Data-Analysis-using-AWS/assets/91766461/f654fcc3-24cb-40fc-beaf-f4535514ddd1)


### 1. IAM (Identity and Access Management): 
Creating an IAM user which defines permissions for users and applications to access and manage data in other services like S3, Glue, Athena, and QuickSight.

### 2. S3 (Simple Storage Service): 
S3 Bucket serves as the data storage repository where raw data is uploaded before processing. 
Created different folders which helps Crawler for Partition.

### 3. AWS Glue: 
Glue helps in extract, transform, and load (ETL) data. 
Running a Crawler to create a Data Catalog.

### 4. AWS Athena: 
Athena enables querying the transformed data stored in S3 by Glue.
It helped in running SQL queries.

![Screenshot 2024-05-22 181525](https://github.com/bhavanachitragar/Superstore-Data-Analysis-using-AWS/assets/91766461/d8809ed8-583f-4da0-b7aa-9ca56b9da2b9)

![Screenshot 2024-05-22 181538](https://github.com/bhavanachitragar/Superstore-Data-Analysis-using-AWS/assets/91766461/7b805de6-1d3b-4c28-ab2c-9c66fa8a01d4)

### 5. Amazon QuickSight:

QuickSight helps in creating visualizations and dashboards from data sources.
It used the results from Athena’s analysis of the data for  data visualization.

#### Sanpshots:

![Screenshot 2024-05-22 181446](https://github.com/bhavanachitragar/Superstore-Data-Analysis-using-AWS/assets/91766461/597ace09-6508-4705-b2a5-369c55130a2a)

![Screenshot 2024-05-22 203727](https://github.com/bhavanachitragar/Superstore-Data-Analysis-using-AWS/assets/91766461/413f8e08-8610-4055-b17c-358729215bf5)

 
----------------------------------------------------------------

Kaggle dataset: https://www.kaggle.com/datasets/vivek468/superstore-dataset-final
