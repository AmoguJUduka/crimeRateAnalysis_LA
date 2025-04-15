# MongoDB & PySpark Integration on Jupyter Notebook

This project demonstrates how to integrate **MongoDB** with **Apache Spark (PySpark)** for data processing and analysis using the **MongoDB Spark Connector**.

## Prerequisites

Before running the integration, ensure the following are installed on your system:

- Anaconda3-2020.02-Windows-x86_64.exe (Jupyter Notebook Installation)
- mongodb-driver-sync-4.7.2
- bson-4.7.2
- mongodb-driver-core-4.7.2
- mongodb-spark-connector_2.12-10.4.1

Make sure you move the .jar files to spark/jars directory

## Jupyter Notebook Setup

- Upon complete installation of Anaconda, navigate to "C:/../Anaconda3/Scripts/" and run "conda list anaconda$"
- Also navigate to "C:/Users/.../.." and run "conda install -c conda-forge findspark" 

## MongoDB Setup

- MongoDB must be running locally on port `27018`.
- The database used is `ece_Project`.
- The collection accessed is `weatherdata`.

Ensure MongoDB is populated with the necessary documents in this collection before running Spark.
