# 🎬 Movie Data Pipeline using AWS S3, Snowflake, dbt & Power BI

## 📌 Project Overview

This project demonstrates a modern ELT (Extract, Load, Transform) data pipeline built using AWS S3, Snowflake, and dbt. Raw movie datasets are first stored in Amazon S3, then loaded into Snowflake's raw layer. dbt is used to clean, transform, and model the data into analytics-ready tables, which are stored back in the Snowflake warehouse for reporting and business intelligence.

The transformed data can be consumed by visualization tools such as Power BI to generate dashboards and insights.

---

## 🏗️ Architecture

```
Raw CSV Files
       │
       ▼
 Amazon S3 (Data Lake)
       │
       ▼
Snowflake Raw Layer
       │
       ▼
 dbt Staging Models
       │
       ▼
 dbt Transformations
       │
       ▼
Snowflake Analytics Warehouse
       │
       ▼
 Power BI Dashboard
```

---

## 🚀 Technologies Used

* AWS S3
* Snowflake Data Warehouse
* dbt Core
* SQL
* Git & GitHub
* Power BI

---

## 📂 Project Workflow

### Step 1: Data Ingestion

* Raw movie datasets are uploaded to Amazon S3.
* Snowflake creates external/internal stages to access the files.
* Data is loaded into raw tables using Snowflake's loading capabilities.

### Step 2: Raw Data Storage

The raw data is stored in Snowflake without any modifications.

Example datasets include:

* Movies
* Ratings
* Tags
* Links

---

### Step 3: Data Transformation with dbt

dbt performs all business transformations, including:

* Data cleaning
* Removing duplicates
* Standardizing column names
* Handling null values
* Creating surrogate keys
* Splitting movie genres
* Building staging models
* Creating fact and dimension tables
* Applying data quality tests
* Generating documentation

---

### Step 4: Analytics Layer

The transformed models are materialized back into Snowflake as analytics-ready tables.

Example models:

#### Dimension Tables

* `dim_movies`
* `dim_users`
* `dim_genres`

#### Fact Tables

* `fct_ratings`
* `fct_tags`

These tables follow a star schema and are optimized for reporting and analytics.

---

### Step 5: Reporting

The analytics tables stored in Snowflake can be connected directly to Power BI for creating interactive dashboards and reports.

Example insights include:

* Highest-rated movies
* Genre popularity
* User rating trends
* Ratings over time
* Movies with the most tags

---

## 📁 Project Structure

```
movie-data-pipeline/
│
├── models/
│   ├── staging/
│   ├── intermediate/
│   ├── marts/
│
├── snapshots/
│
├── tests/
│
├── macros/
│
├── seeds/
│
├── analyses/
│
├── dbt_project.yml
│
└── README.md
```

---

## ✅ Data Quality Testing

dbt tests are implemented to ensure data quality.

Tests include:

* `not_null`
* `unique`
* `relationships`
* `accepted_values`

These tests help maintain reliable and consistent data throughout the pipeline.

---

## 📊 Benefits

* Automated ELT pipeline
* Scalable cloud-based architecture
* Modular SQL transformations using dbt
* Reliable data quality through automated testing
* Analytics-ready star schema
* Easy integration with Power BI
* Version-controlled development using GitHub

---

## 📌 Future Enhancements

* Automate data ingestion using Snowpipe
* Schedule dbt runs with Apache Airflow
* Implement CI/CD with GitHub Actions
* Add incremental models
* Add dbt snapshots for Slowly Changing Dimensions (SCD)
* Monitor pipeline execution and data freshness

---

## 👨‍💻 Author

**Abhay Zala**

Aspiring Data Engineer with experience in SQL, PL/SQL, Snowflake, dbt, ETL, Python, and Power BI.
