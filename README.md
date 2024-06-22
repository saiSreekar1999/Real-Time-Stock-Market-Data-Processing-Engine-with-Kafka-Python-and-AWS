# Real-Time-Stock-Market-Data-Processing-Engine-with-Kafka-Python-and-AWS
Real-time stock market data pipeline using Kafka and AWS. Python scripts simulate streaming stock data, ingested by Kafka, then stored in S3. AWS Glue and Athena enable analysis of the live data.

# Real-Time Stock Market Data Processing Pipeline
This project demonstrates a scalable, real-time data processing pipeline for stock market data, leveraging Apache Kafka and AWS services.

# Overview
The pipeline simulates a real-time stock market data stream, processes it using Kafka, and stores the data in Amazon S3 for further analysis. It showcases the following:

Real-Time Data Ingestion: Python scripts simulate streaming stock data, mimicking a live feed.
Kafka Streaming: Apache Kafka handles the real-time data stream, ensuring reliable and scalable processing.
S3 Data Storage: Stock data is continuously written to Amazon S3 in a structured format.
AWS Glue Crawler: Automatically discovers and catalogs the schema of the S3 data.
Amazon Athena Analysis: Enables real-time querying and analysis of the stock data using SQL.

# Architecture
Stock Data Simulation (Python) -> Kafka Producer -> Kafka Cluster -> Kafka Consumer -> S3 -> Glue Crawler -> Athena

# Prerequisites
AWS Account (with S3, Glue, and Athena access)
EC2 Instance (for Kafka deployment)
Python 3.x
Kafka Python Client
AWS CLI (configured with credentials)

# Installation and Setup
Kafka Deployment: Follow the instructions in kafka_setup.sh to deploy Kafka on the EC2 instance.
Python Environment: Install required Python libraries using pip install -r requirements.txt.
AWS Configuration: Configure AWS CLI with your credentials and set up the S3 bucket.
Usage
Start Kafka: Execute kafka_start.sh on the EC2 instance.
Run Producer: Execute producer.py to simulate and send stock data to Kafka.
Run Consumer: Execute consumer.py to consume data from Kafka and store it in S3.
Run Glue Crawler: Trigger the Glue crawler to catalog the S3 data.
Query with Athena: Use Athena to query the stock data (sample queries in athena_queries.sql).
