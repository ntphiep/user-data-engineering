<!-- # Realtime Data Streaming | End-to-End Data Engineering Project

## Table of Contents
- [Realtime Data Streaming | End-to-End Data Engineering Project](#realtime-data-streaming--end-to-end-data-engineering-project)
  - [Table of Contents](#table-of-contents)
  - [Introduction](#introduction)
  - [System Architecture](#system-architecture)
  - [What You'll Learn](#what-youll-learn)
  - [Technologies](#technologies)
  - [Getting Started](#getting-started)
  - [Watch the Video Tutorial](#watch-the-video-tutorial)

## Introduction

This project serves as a comprehensive guide to building an end-to-end data engineering pipeline. It covers each stage from data ingestion to processing and finally to storage, utilizing a robust tech stack that includes Apache Airflow, Python, Apache Kafka, Apache Zookeeper, Apache Spark, and Cassandra. Everything is containerized using Docker for ease of deployment and scalability.

## System Architecture

![System Architecture](imgs/../img/Data%20engineering%20architecture.png)

The project is designed with the following components:

- **Data Source**: We use `randomuser.me` API to generate random user data for our pipeline.
- **Apache Airflow**: Responsible for orchestrating the pipeline and storing fetched data in a PostgreSQL database.
- **Apache Kafka and Zookeeper**: Used for streaming data from PostgreSQL to the processing engine.
- **Control Center and Schema Registry**: Helps in monitoring and schema management of our Kafka streams.
- **Apache Spark**: For data processing with its master and worker nodes.
- **Cassandra**: Where the processed data will be stored.

## What You'll Learn

- Setting up a data pipeline with Apache Airflow
- Real-time data streaming with Apache Kafka
- Distributed synchronization with Apache Zookeeper
- Data processing techniques with Apache Spark
- Data storage solutions with Cassandra and PostgreSQL
- Containerizing your entire data engineering setup with Docker

## Technologies

- Apache Airflow
- Python
- Apache Kafka
- Apache Zookeeper
- Apache Spark
- Cassandra
- PostgreSQL
- Docker

## Getting Started

1. Clone the repository:
    ```bash
    git clone https://github.com/airscholar/e2e-data-engineering.git
    ```

2. Navigate to the project directory:
    ```bash
    cd e2e-data-engineering
    ```

3. Run Docker Compose to spin up the services:
    ```bash
    docker-compose up
    ```

For more detailed instructions, please check out the video tutorial linked below.

## Watch the Video Tutorial

For a complete walkthrough and practical demonstration, check out our [YouTube Video Tutorial](https://www.youtube.com/watch?v=GqAcTrqKcrY). -->


# Realtime Data Streaming Project

## Table of Contents

- [Realtime Data Streaming Project](#realtime-data-streaming-project)
  - [Table of Contents](#table-of-contents)
  - [Introduction](#introduction)
  - [System Architecture](#system-architecture)
  - [Technologies](#technologies)
  - [Getting Started](#getting-started)
- [References](#references)



## Introduction

This project serves as a comprehensive guide to building an end-to-end data engineering pipeline. It covers each stage from data ingestion to processing and finally to storage, utilizing a robust tech stack that includes Apache Airflow, Python, Apache Kafka, Apache Zookeeper, Apache Spark, and Cassandra. Everything is containerized using Docker for ease of deployment and scalability.


## System Architecture

![System Architecture](img/architecture.png)

The project is designed with the following components:

- **Data Source**: Getting data from this public API: https://randomuser.me/
- **Apache Airflow**: Responsible for orchestrating the pipeline. Thee pipeline has only 1 task which is to fetch data from the API and then send it to Kafka Producer.

- **Apache Kafka and Zookeeper**: Used for streaming data from API to Spark processing.
- **Control Center and Schema Registry**: Helps in monitoring and schema management of our Kafka streams.
- **Apache Spark**: For data processing with its master and worker nodes.
- **Cassandra**: Where the processed data will be stored.


## Technologies

- Apache Airflow
- Apache Kafka, Apache Zookeeper
- Apache Spark
- Cassandra
- PostgreSQL
- Docker, Docker compose
- Python



## Getting Started

Clone this repo and then run the following command to start the project:

```bash
docker-compose up -d
```

After that, you can access the following services:
- Airflow: http://localhost:8080
- Control Center: http://localhost:9021
- Spark Master: http://localhost:8081


# References
- [YouTube Video Tutorial](https://www.youtube.com/watch?v=GqAcTrqKcrY)