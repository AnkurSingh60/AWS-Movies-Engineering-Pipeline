# AWS-Movies-Data-Engineering-Pipeline
End-to-end AWS Data Engineering Pipeline using S3, Glue, EventBridge, Athena,,PowerBI CloudWatch, and SNS for automated movie data processing and analytics.


 # AWS Movies Engineering Pipeline

## Project Overview

This project demonstrates an end-to-end AWS Data Engineering Pipeline built on AWS services. The pipeline automates movie data ingestion, cataloging, transformation, monitoring, and analytics using AWS Glue, EventBridge, Athena,PowerBI, CloudWatch, and SNS.

## Architecture

```text
Movies Dataset
      │
      ▼
Amazon S3 (Raw Zone)
      │
      ▼
Glue Crawler
      │
      ▼
Glue Data Catalog
      │
      ▼
EventBridge Scheduler
      │
      ▼
Glue Workflow
      │
      ▼
Glue ETL Job (PySpark)
      │
      ▼
Amazon S3 (Processed Zone)
      │
      ▼
Amazon Athena
      │
      ▼
Business Analytics

Monitoring:

Glue Job
   │
   ▼
CloudWatch Logs
   │
   ▼
CloudWatch Alarm
   │
   ▼
SNS Email Notification
```

## AWS Services Used

- Amazon S3
- AWS Glue Crawler
- AWS Glue Data Catalog
- AWS Glue ETL Job
- AWS Glue Workflow
- Amazon EventBridge
- Amazon Athena
- Amazon CloudWatch
- Amazon SNS
- PySpark

## Project Workflow

### 1. Data Ingestion
Movie dataset is stored in Amazon S3 Raw Zone.

### 2. Metadata Discovery
Glue Crawler scans the dataset and creates tables in the Glue Data Catalog.

### 3. Scheduling
Amazon EventBridge automatically triggers the Glue Workflow on a defined schedule.

### 4. Data Processing
Glue ETL Job written in PySpark cleans and transforms movie data.

### 5. Data Storage
Processed data is stored in Amazon S3 Processed Zone.

### 6. Analytics
Amazon Athena queries the processed dataset for business insights and reporting.

### 7. Monitoring & Alerting
- CloudWatch Logs capture ETL execution logs.
- CloudWatch Alarm monitors failures.
- SNS sends email notifications for alerts.

## Repository Structure

```text
AWS-Movies-Engineering-Pipeline/
│
├── architecture/
│   └── Architecture_Diagram.png
│
├── datasets/
│   └── movies_dataset.csv
│
├── scripts/
│   └── glue_spark_job.py
│
├── screenshots/
│   ├── s3_bucket.png
│   ├── glue_job.png
│   ├── crawler.png
│   ├── workflow.png
│   ├── eventbridge.png
│   ├── athena_query.png
│   └── cloudwatch_alarm.png
│
└── README.md
```

## Key Features

- Automated ETL Pipeline
- Metadata Management using Glue Catalog
- Scheduled Workflow Execution
- Serverless Analytics with Athena
- Monitoring and Alerting
- Scalable AWS Architecture

## Author

**Ankur Singh**
- Data Engineer Enthusiast
- AWS | PySpark | SQL | Data Engineering
