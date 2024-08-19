# Instagram_BigData_ELT_With_AWS

1. Ingestion
   
Big Data Source: Instagram Graph API

Role: Acts as the primary data source where you pull data from Instagram.
Details: Instagram Graph API provides access to various types of data such as user posts, stories, comments, etc. You'll need to handle API rate limits and data fetching logic.

Ingestion Tool: Apache Kafka

Role: Captures and streams the data from the Instagram API.
Details: Kafka serves as a buffer and real-time data ingestion system, allowing you to decouple data producers from consumers and manage high-throughput data ingestion.

2. Data Streaming

Data Stream: AWS Kinesis Firehose

Role: Facilitates the continuous streaming of data from Kafka to S3.
Details: Kinesis Firehose is used to load data streams into data lakes (S3 in this case) with minimal setup and configuration. It handles data transformation and delivery.

S3 Bucket: Preliminary Repository/Data Lake

Role: Acts as a storage solution for raw data.
Details: S3 stores data in its raw format as it is streamed. It serves as a staging area for further processing.

3. Data Processing
   
Processing Service: AWS Glue

Role: Manages ETL (Extract, Transform, Load) operations.
Details: AWS Glue uses Apache Spark to process and transform data stored in S3. It automates data discovery, schema management, and job scheduling.

Data Integration Engine: Apache Spark

Role: Performs data transformations and processing.
Details: Spark handles large-scale data processing tasks, such as filtering, aggregating, and transforming data from the S3 bucket.

4. Data Loading
   
Database Hosting: EC2

Role: Hosts the NoSQL database (MongoDB).
Details: EC2 provides the compute resources for hosting MongoDB, allowing you to manage the database instance as needed.

NoSQL Database: MongoDB

Role: Stores processed and structured data.
Details: MongoDB, as a NoSQL database, handles flexible, JSON-like document storage, making it suitable for big data applications and unstructured data.

5. Data Visualization
   
Dashboard Service: Tableau Cloud

Role: Provides data visualization and dashboard capabilities.
Details: Tableau Cloud offers a fully managed, cloud-based service to create and share interactive dashboards and visualizations, accessible from anywhere.


<img width="1728" alt="Screenshot 2024-08-18 at 9 43 12 PM" src="https://github.com/user-attachments/assets/51bdd572-951b-4581-917c-12b6195f24da">
