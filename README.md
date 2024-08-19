# YouTube Data Analysis | End-to-End Data Engineering Project

## Project Overview

This project demonstrates an end-to-end data engineering workflow for analyzing YouTube data using various AWS services. The goal is to build a comprehensive data pipeline that ingests, transforms, and analyzes YouTube data, providing actionable insights for improving video marketing strategies. The project covers data ingestion, ETL (Extract, Transform, Load), querying, and visualization using AWS tools like S3, Glue, Athena, Lambda, and QuickSight.

## Key Steps

### 1. Data Collection and Preparation

- **Data Ingestion**: Collected YouTube data in CSV format, including details such as video ID, upload date, view count, likes, comments, and other relevant metrics.
- **Data Upload**: Set up an AWS S3 bucket to store the raw data files. Utilized AWS CLI to upload data from local storage to the S3 bucket.

### 2. AWS Account Setup and Configuration

- **AWS Account**: Created an AWS account and configured it for the project, ensuring secure access with proper credentials and permissions.
- **S3 Bucket**: Uploaded the CSV files to an S3 bucket and configured necessary permissions for data access.

### 3. Data Cataloging and ETL

- **Glue Data Catalog**: Used AWS Glue to create a data catalog for the S3 bucket. Configured a Glue Crawler to scan the CSV files and build a data catalog.
- **Role and Permissions**: Created and assigned a Glue role with the required permissions to access S3 data and perform ETL operations.

### 4. Data Querying

- **AWS Athena**: Used Athena to query the data catalog. Demonstrated how to create tables and perform queries to analyze the YouTube data, including handling JSON serialization/deserialization issues and preprocessing data for efficient querying.

### 5. Lambda Functions

- **AWS Lambda**: Created a Lambda function using AWS Wrangler to process data. Configured the Lambda function to handle data in Parquet format and store the cleaned data back into S3.
- **Error Handling**: Addressed common errors related to package dependencies and function integration.

### 6. Data Transformation and Loading

- **ETL Pipeline**: Built an ETL pipeline using AWS Glue to move data from the raw S3 bucket to a clean S3 bucket. Applied transformations, created partitions, and filtered out unwanted data.
- **Glue ETL Jobs**: Configured Glue ETL jobs to handle data transformations and updates.

### 7. Data Visualization

- **AWS QuickSight**: Used AWS QuickSight to create visualizations and dashboards based on the processed data. Built graphs and charts to analyze metrics such as video performance, engagement trends, and audience insights.
- **Athena Integration**: Created a dashboard in Athena to visualize the results and share insights.

### 8. Automation and Deployment

- **Lambda Triggers**: Set up triggers for the Lambda function to automatically process new data uploaded to the S3 bucket.
- **Monitoring and Maintenance**: Monitored ETL jobs and data pipelines to ensure smooth operation and timely data processing.

## Tools Used

- **Amazon S3**: Data storage and retrieval
- **AWS Glue**: Data cataloging, ETL jobs
- **AWS Athena**: Data querying
- **AWS Lambda**: Serverless data processing
- **AWS QuickSight**: Data visualization and dashboard creation
- **AWS CLI**: Command-line interface for AWS services
- **AWS Wrangler**: Data transformation library

## Outcome

The project successfully demonstrated an end-to-end data engineering workflow for YouTube data analysis. The final setup provided a robust pipeline for ingesting, transforming, and analyzing data, resulting in a comprehensive dashboard that offers insights into video performance, trends, and audience behavior. The project showcased the effective use of AWS tools for managing big data and deriving actionable insights for video marketing strategies.

## Challenges and Solutions

- **Big Data Handling**: Addressed challenges related to data size and format issues. Recommended using pre-processing tools and optimizing data storage formats (e.g., Parquet) for better performance.
- **Error Resolution**: Solved issues related to Lambda functions and data compatibility through detailed troubleshooting and adjustments.

### Link to dashboard :
https://us-east-1.quicksight.aws.amazon.com/sn/dashboards/dc10c358-72b6-4b37-bbaa-ecaf3fb560b4?#

