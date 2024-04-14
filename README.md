# Realtime Data Streaming | Data Engineering Project

## Introduction

This project aims to be my learning about how to building an end-to-end data engineering pipeline. It encompasses every stage, starting from data ingestion, proceeding to processing, and culminating in storage. The project leverages a robust technology stack, including Apache Airflow, Python, Apache Kafka, Apache Zookeeper, Apache Spark, and Cassandra. All components are containerized using Docker for streamlined deployment and scalability.

## System Architecture

![System Architecture](./data-eng-arch.png)

The project is designed with the following components:

- **Data Source:** Using the `randomuser.me` API to generate randomized user data for integration into the pipeline.
- **Apache Airflow:** Orchestrates the entire pipeline and stores fetched data in a PostgreSQL database.
- **Apache Kafka and Zookeeper:** Facilitates streaming data from PostgreSQL to the processing engine.
- **Control Center and Schema Registry:** Enables efficient monitoring and schema management of Kafka streams.
- **Apache Spark:** Engaged for data processing via its master and worker nodes.
- **Cassandra:** Serves as the data storage for the processed data.

## Learning Outcomes
Through this project, I'm aiming to learn as much as possible:
- Establishing a robust data pipeline with Apache Airflow.
- Implementing real-time data streaming using Apache Kafka.
- Orchestrating distributed synchronization with Apache Zookeeper.
- Trying to employ advanced data processing techniques with Apache Spark.
- Utilizing both Cassandra and PostgreSQL for efficient data storage solutions.
- Get in touch with containerizing the entire data engineering infrastructure with Docker for enhanced manageability.

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/DangBaoTin/realtime-data-stream.git
    ```

2. Navigate to the project directory:
    ```bash
    cd realtime-data-stream
    ```

3. Run Docker Compose to spin up the services:
    ```bash
    docker-compose up
    ```
## Additional installations
For easy running, first we will initialize the virtual environment for python:
```bash
python3 -m venv virtenv
```
Then we enable our virtual environment:
```bash
source virtenv/bin/activate
```
After setting up the environment, we can install supported libraries for the `virtenv` (copy each line to the terminal):
```bash
pip install pandas
pip install apache-airflow
pip install spark pyspark
```
In the `virtenv/lib` folder, look for `pyspark` > `jars` and install additional `.jar` files to the selected folder. Go to [MVN Repository](https://mvnrepository.com/) and download the following files:
- Spark Cassandra Connector ver 3.4.1
- Kafka 0.10+ Source For Structured Streaming ver 3.4.1

And then insert these `.jar` files into the destination folder.