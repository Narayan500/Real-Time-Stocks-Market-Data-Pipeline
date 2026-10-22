# Real-Time Stocks Market Data Pipeline

![Snowflake](https://img.shields.io/badge/Snowflake-29B5E8?logo=snowflake&logoColor=white)
![DBT](https://img.shields.io/badge/dbt-FF694B?logo=dbt&logoColor=white)
![Apache Airflow](https://img.shields.io/badge/Apache%20Airflow-017CEE?logo=apacheairflow&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![Kafka](https://img.shields.io/badge/Apache%20Kafka-231F20?logo=apachekafka&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white)
![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?logo=powerbi&logoColor=black)

---

## 📌 Project Overview
This project demonstrates an **end-to-end real-time data pipeline** using the **Modern Data Stack**.  
We capture **live stock market data** from an external API, stream it in real time, orchestrate transformations, and deliver analytics-ready insights — all in one unified project.

---

## ⚡ Tech Stack
- **Snowflake** → Cloud Data Warehouse  
- **dbt** → SQL-based Transformations  
- **Apache Airflow** → Workflow Orchestration  
- **Apache Kafka** → Real-time Streaming  
- **Python** → Data Fetching & API Integration  
- **Docker** → Containerization  
- **Power BI** → Data Visualization  

---

## ✅ Key Features
- Fetching **live stock market data** from Finnhub API  
- Real-time streaming pipeline using **Apache Kafka**  
- Storage in S3-compatible **MinIO** object storage  
- Orchestrated ETL workflow using **Apache Airflow**  
- Transformations using **dbt** inside Snowflake  
- Scalable cloud data warehouse powered by **Snowflake**  
- Analytics-ready **Power BI dashboards**  

---

## 📂 Repository Structure

```text
Stock_Market/
├── consumer/                     # Kafka consumer (MinIO sink)
│   └── consumer.py
├── dags/                         # Airflow DAGs
│   └── minio_to_snowflake.py
├── dbt_stocks/                   # dbt transformation project
│   ├── models/
│   │   ├── bronze/
│   │   │   ├── bronze_stg_stock_quotes.sql
│   │   │   └── sources.yml
│   │   ├── silver/
│   │   │   └── silver_clean_stock_quotes.sql
│   │   └── gold/
│   │       ├── gold_candlestick.sql
│   │       ├── gold_kpi.sql
│   │       └── gold_treechart.sql
│   └── dbt_project.yml
├── producer/                     # Kafka producer (Finnhub API)
│   └── producer.py
├── infra/                        # Infrastructure / Docker configs
│   └── docker-compose.yml
├── requirements.txt              # Project dependencies
└── README.md                     # Project documentation
