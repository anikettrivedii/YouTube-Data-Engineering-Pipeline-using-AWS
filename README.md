# 🎥 YouTube Trending Videos Data Pipeline and Analysis

This project demonstrates a complete **data engineering architecture** for processing and analyzing **YouTube trending video data** from multiple regions using **AWS cloud services**.  
The solution implements a scalable **data lake**, **data processing**, and **analytical access layers** to automate ingestion, transformation, and reporting.

---

## 📘 Dataset

The dataset used in this project is sourced from **Kaggle – Trending YouTube Video Statistics**.  
It contains daily statistics on the most popular YouTube videos from multiple regions and includes:

- Video title, channel title, and category  
- Publish and trending dates  
- Views, likes, dislikes, and comments  
- Tags, description, and region codes  

🔗 [Kaggle Dataset – Trending YouTube Video Statistics](https://www.kaggle.com/datasets/datasnaek/youtube-new)

---

## 🏗️ Architecture Overview

The project is built on a **modern AWS data lake architecture** with three primary layers:

### 🪣 Data Lake Layers
| Layer | Description |
|--------|--------------|
| **Landing Area** | Raw data from Kaggle is stored in S3 buckets for each region. |
| **Cleansed / Enriched** | Data is cleaned, normalized, and enriched using AWS Glue ETL jobs. |
| **Analytics / Reporting** | Transformed data is optimized and stored for analytical querying and visualization. |

---

## ⚙️ Data Processing Components

- **AWS S3** → Acts as the central data lake for storing raw and processed files.  
- **AWS Glue** → Performs ETL (Extract, Transform, Load) tasks, data cleaning, and cataloging.  
- **AWS Lambda** → Handles lightweight transformations and event-driven operations.  
- **AWS Athena** → Provides serverless SQL querying over processed S3 data.  
- **Amazon Redshift (Optional)** → Data warehouse for complex analytical workloads.  
- **AWS CloudWatch** → Monitors ETL jobs, logs, and triggers alerts on failures.  

---

## 🔄 Data Flow

1. **Source Ingestion:**  
   Raw YouTube CSV files are downloaded from Kaggle and uploaded to an AWS S3 bucket (Landing Zone).

2. **Bulk Data Upload:**  
   Data is loaded into dedicated S3 folders partitioned by region and date.

3. **Data Processing:**  
   AWS Glue jobs perform data transformation, cleaning, and enrichment.

4. **Event-Driven Processing:**  
   AWS Lambda functions handle incremental updates or trigger Glue workflows.

5. **Data Cataloging:**  
   AWS Glue Data Catalog classifies datasets and maintains metadata.

6. **Analytics Access:**  
   Data is queried directly from S3 using **Athena** or loaded into **Redshift** for warehouse analytics.

7. **Visualization:**  
   Insights are visualized using **AWS QuickSight**, **Power BI**, or **Jupyter Notebooks**.

---

## ☁️ AWS Services Used

| Category | Services |
|-----------|-----------|
| **Storage** | Amazon S3 |
| **ETL & Transformation** | AWS Glue |
| **Compute / Event Handling** | AWS Lambda |
| **Data Catalog & Query** | AWS Glue Data Catalog, AWS Athena |
| **Data Warehouse (Optional)** | Amazon Redshift |
| **Monitoring** | AWS CloudWatch |
| **Visualization** | AWS QuickSight / Power BI |

---

## 🧠 Key Features

- End-to-end automated **data pipeline** from ingestion to analytics  
- **Serverless architecture** using AWS managed services  
- **Modular ETL design** for scalability and maintenance  
- Centralized **data catalog** for metadata management  
- **SQL-based querying** and dashboard integration for analytics  
- **Real-time monitoring** and alerting with CloudWatch  

---

## 🧾 Example Use Cases

- Identify top-trending videos by region and category  
- Analyze engagement metrics (views, likes, comments)  
- Compare regional content performance and popularity  
- Automate YouTube data reporting workflows  

---

## 📊 Architecture Diagram

![YouTube AWS Data Engineering Architecture](https://private-user-images.githubusercontent.com/158104333/386010672-6414ec73-0086-4b15-9d83-7adb9d205326.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkaXNhYmxlX3JlZ2lvbnMiOltdLCJleHAiOjE3NDUwODcwNTIsImNvbnRlbnRfdHlwZSI6ImltYWdlL3BuZyIsInJlc291cmNlX2lkIjoiMTU4MTA0MzMzLzM4NjAxMDY3Mi02NDE0ZWM3My0wMDg2LTRiMTUtOWQ4My03YWRiOWQyMDUzMjYucG5nIiwicmVwb19pZCI6IlByaXZhdGVVc2VySW1hZ2VzIiwidXNlcl9pZCI6IjE1ODEwNDMzMyIsIm9yaWdpbmFsX3JlcXVlc3QiOnRydWUsImlhdCI6MTc0NTA4Njc1Mn0.DIRCh3WDXHwTG-tzcbnm3EByMNXfTgK98CBJaWj3vHw)

---

## 📈 Monitoring and Alerts

- **AWS CloudWatch** tracks the health of Glue and Lambda jobs.  
- Alerts are triggered on job failures, delays, or threshold breaches.  
- Logs are retained for pipeline debugging and optimization.

---

## 🧩 Future Enhancements

- Integrate **Airflow or Step Functions** for workflow orchestration.  
- Implement **CI/CD pipelines** using AWS CodePipeline for ETL deployments.  
- Add **data quality checks** and validation scripts.  
- Enable **real-time ingestion** using YouTube Data API v3 and Kinesis.  
- Expand visualization with **interactive dashboards**.

---

## 📚 References

- [Trending YouTube Video Statistics – Kaggle](https://www.kaggle.com/datasets/datasnaek/youtube-new)  
- [AWS Glue Documentation](https://docs.aws.amazon.com/glue/latest/dg/what-is-glue.html)  
- [AWS Athena Documentation](https://docs.aws.amazon.com/athena/latest/ug/what-is.html)  
- [AWS Lambda Documentation](https://docs.aws.amazon.com/lambda/latest/dg/welcome.html)

---

## 👨‍💻 Author

**Baby** — *Data Engineer / Data Analyst*  
📧 your.email@example.com  
🔗 [GitHub Profile](https://github.com/yourusername)

---

### 🟢 Repository Description (for GitHub)
> End-to-end YouTube trending videos data engineering pipeline using AWS S3, Glue, Lambda, and Athena.


