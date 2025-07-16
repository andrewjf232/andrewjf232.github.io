

# Currency Data ETL Pipeline

This project is a robust and automated ETL (Extract, Transform, Load) pipeline built to process financial data. It efficiently fetches currency pair information from the Polygon.IO API, cleans and transforms the data for consistency, and loads it into a time-series database for analysis.

The entire system is designed for high reliability, automation, and ease of maintenance, showcasing a practical application of data engineering principles.

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
![Frontend Display Screenshot](frontend.png)

---

## Technology Stack

* **Backend**: Python, FastAPI
* **Database**: PostgreSQL, TimescaleDB
* **Cloud Provider**: Microsoft Azure
* **Operating System**: Ubuntu (VM)
* **API**: Polygon.IO REST API
