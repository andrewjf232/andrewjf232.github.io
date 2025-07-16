

# Currency Data ETL Pipeline

This project is a robust and automated ETL (Extract, Transform, Load) pipeline built to process financial data. It efficiently fetches currency pair information from the Polygon.IO API, cleans and transforms the data for consistency, and loads it into a time-series database for analysis.

The entire system is designed for high reliability, automation, and ease of maintenance, showcasing a practical application of data engineering principles.

**Project Link:** [Curreny Data ETL Pipeline](https://github.com/Bettr-Trading/bettr.trading)

**Note:** This is a private repository for security reasons. Please reach out to me for a demo. 


---

## Key Features

* **Automated Data Extraction**: Uses FastAPI and Python to create a service that fetches currency pair data from the Polygon.IO API.
* **Data Transformation**: Implements data cleaning and validation to ensure the accuracy and consistency of the financial data before storage.
* **Scalable Data Loading**: Efficiently handles and loads large datasets, with an initial load of approximately 2 million rows into a PostgreSQL database with the TimescaleDB extension for time-series data.
* **Cloud-Hosted & Reliable**: The entire database and application are hosted on an Ubuntu VM in Microsoft Azure, configured for continuous and reliable operation.

---

## System Architecture

The data flows through a simple, yet powerful, architecture:

`Frontend (Setting Query Params)` -> `FastAPI Endpoint Backend (GET Request URL Creation)` -> `Polygon.IO API (Data Extraction)`  -> -> `FastAPI Backend (Transform GET Response)` -> `PostgreSQL/TimescaleDB (Loading Data)`

## Frontend Display
![Frontend Display](/images/frontend.png)

---

## Technology Stack

* **Backend**: Python, FastAPI
* **Database**: PostgreSQL, TimescaleDB
* **Cloud Provider**: Microsoft Azure
* **Operating System**: Ubuntu (VM)
* **API**: Polygon.IO REST API

---

## Sampled Result Data (Azure Postgresql + TimescaleDB)
![DemoData Display](/images/demoData.jpeg)

Sampling data showing Pair, Open , High , Low, Close and other currency information on the 1st January 2024.


![timeframeData Display](/images/timeframeData.jpeg)

Sample of total counts of 15_minute segments each day over the first month of 2022.
