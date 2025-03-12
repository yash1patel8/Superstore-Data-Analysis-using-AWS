# Superstore Data Analysis using AWS

This project builds a pipeline to analyze Superstore sales data using AWS services. The pipeline transforms raw data into a format suitable for exploration, queries the data using SQL, and creates visualizations to uncover trends and patterns. The goal is to provide actionable insights into Superstore's sales performance.

## AWS Services Used

- **IAM (Identity and Access Management)**: Created an IAM user with specific permissions to access and manage data across AWS services like S3, Glue, Athena, and QuickSight.
- **S3 (Simple Storage Service)**: Used as the primary data storage repository. Raw data was uploaded to S3, and folders were organized to facilitate partitioning for the Glue Crawler.
- **AWS Glue**: Performed ETL (Extract, Transform, Load) operations. A Glue Crawler was used to create a Data Catalog, which automatically inferred the schema and partitioned the data.
- **AWS Athena**: Enabled querying of the transformed data stored in S3 using SQL. Athena was used to run analytical queries and generate insights.
- **Amazon QuickSight**: Used to create interactive visualizations and dashboards based on the analyzed data from Athena.

## Pipeline Overview

1. **Data Ingestion**: Raw Superstore data was uploaded to an S3 bucket.
2. **Data Transformation**: AWS Glue was used to clean, transform, and partition the data.
3. **Data Cataloging**: A Glue Crawler was run to create a Data Catalog, which allowed Athena to query the data.
4. **Data Analysis**: SQL queries were executed in Athena to uncover trends and patterns.
5. **Data Visualization**: QuickSight was used to create dashboards and visualizations for easy interpretation of the results.

## Results and Insights

### 1. Sum of Sales and Profit by Sub-Category
- **High-Sales Sub-Categories**: Phones, Chairs, and Storage are the top-performing sub-categories in terms of sales.
- **High-Profit Sub-Categories**: Copiers and Phones generate the highest profits, despite having lower sales volumes compared to other sub-categories.
- **Low-Profit Sub-Categories**: Supplies and Fasteners have the lowest profit margins, indicating potential inefficiencies or pricing issues.

**Visualization**:
- A bar chart showing the sum of sales and profit for each product sub-category.

### 2. Sum of Sales by Category
- **Office Supplies**: This category generates the highest sales, followed by Technology and Furniture.
- **Technology**: While Technology has lower sales compared to Office Supplies, it has higher profit margins.
- **Furniture**: Furniture has moderate sales but lower profit margins compared to the other categories.

**Visualization**:
- A bar chart illustrating the total sales for each product category (Office Supplies, Technology, Furniture).

### 3. Sum of Profit and Quantity by Product Name
- **High-Profit Products**: Products like #10 White Business Envelopes and 1.7 Cubic Feet Compact Office Refrigerator generate high profits.
- **High-Quantity Products**: Products like #10– 4 1/4 x 9 1/2 Recycled Envelopes and #10– 4 1/4 x 9 1/2 Security-Tint Envelopes are sold in large quantities but have lower profit margins.

**Visualization**:
- A table listing the profit and quantity sold for each product.

### 4. Count of Ship Date by Category
- **Office Supplies**: This category has the highest shipping volume, indicating high demand.
- **Technology**: Technology products have moderate shipping volumes.
- **Furniture**: Furniture has the lowest shipping volume, suggesting lower demand or longer lead times.

**Visualization**:
- A bar chart showing the count of ship dates for each product category.

### 5. Sum of Sales by City (Top 5 Cities)
- **Top-Performing Cities**: Cities like New York, Los Angeles, and Chicago contribute the most to overall sales.
- **Underperforming Cities**: Cities like Albuquerque and Nashville have lower sales volumes, indicating potential opportunities for growth.

**Visualization**:
- A bar chart highlighting the top 5 cities with the highest sales.

## Improvements

- **Data Quality Checks**: Implement data validation steps during the ETL process to ensure data accuracy and consistency.
- **Automation**: Use AWS Step Functions or Lambda to automate the entire pipeline, from data ingestion to visualization.
- **Advanced Analytics**: Incorporate machine learning models (using AWS SageMaker) to predict future sales trends or customer behavior.
- **Cost Optimization**: Monitor and optimize the cost of AWS services, especially for large datasets, by using S3 lifecycle policies and Athena query optimizations.
- **Enhanced Visualizations**: Use more advanced QuickSight features like forecasting, anomaly detection, and custom calculations to provide deeper insights.
- **Documentation**: Add detailed documentation for each step of the pipeline, including code snippets, query examples, and troubleshooting tips.

## Kaggle Dataset

The dataset used for this analysis is available on Kaggle:  
[Superstore Dataset](https://www.kaggle.com/datasets)

## Conclusion

This project demonstrates the power of AWS in building a scalable and efficient data analysis pipeline. By leveraging services like S3, Glue, Athena, and QuickSight, we were able to transform raw data into actionable insights. The insights gained can help Superstore optimize its sales strategy, improve customer segmentation, and enhance overall business performance.

