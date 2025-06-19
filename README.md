# End-to-End-E-commerce-Data-Pipeline-with-Azure-Medallion-Architecture
Brazillian E-commerce gaint- Olist
📦 End-to-End Big Data Engineering Project – E-commerce Data
This project demonstrates how to build a scalable, end-to-end big data pipeline using Azure services. The data source is the Brazilian E-Commerce Public Dataset by Olist, containing 100,000 orders with product, customer, and review information.

🛠️ Prerequisites
Before starting this project, ensure you have:

Motivation to learn and complete the project

A laptop and a notebook

Technical Skills: Basic knowledge of Python and SQL

An Azure Free Account

Includes $200 free credit

Requires email (Gmail supported) and a credit card (minimal charge, no autopay)

🧾 Dataset
We use the Brazilian E-Commerce Public Dataset from Olist, including the following CSV files:

olist_customers_dataset.csv

olist_geolocation_dataset.csv

olist_order_items_dataset.csv

olist_order_payments_dataset.csv

olist_order_reviews_dataset.csv

olist_orders_dataset.csv

olist_products_dataset.csv

olist_sellers_dataset.csv

product_category_name_translation.csv

🧱 Architecture Overview
Refer to the diagram on page 4 of the notes.

🔗 Workflow Components:
Data Sources: Files (CSV), SQL tables, and APIs

Azure Data Factory (ADF): For data ingestion

Azure Data Lake Storage (ADLS) Gen2: Stores raw, cleaned, and transformed data

Azure Databricks: For transformations, aggregation, and ML

Azure Synapse Analytics: For data warehousing and visualization (Power BI or Tableau)

🏗️ Medallion Architecture (Page 11)
Bronze Layer: Raw data ingestion

Silver Layer: Cleaned and transformed data

Gold Layer: Aggregated business insights

🔄 Data Pipeline Breakdown
🔹 Azure Data Factory
Collects and orchestrates data movement

Handles:

Data collection

Parameterization

For-each activities

Lookups

🔹 Azure Data Lake (ADLS Gen2)
Stores massive volumes of structured and unstructured data

Scalable, secure, and cost-efficient

🔹 Azure Databricks Workflow
Read from ADLS Gen2

Clean and transform (renaming, filtering)

Join multiple datasets

Enrich using MongoDB

Aggregate and derive insights

Write back to ADLS Gen2

🔹 Azure Synapse Analytics
Used for:

Data integration

Enterprise data warehousing

Big Data analytics

Access data from Silver Layer using OPENROWSET

Create views for simplified querying

🗃️ SQL Pool Setup
Feature	Serverless SQL Pool	Dedicated SQL Pool
Compute	On-demand	Pre-allocated
Payment Model	Pay per query	Fixed cost
Use Case	Exploration, ad hoc	Performance-intensive
Data Location	In Data Lake	In Synapse SQL DB
Setup	Very simple	More complex

Analogy: Serverless = Bus, Dedicated = Own Car (see page 19)

🔁 Data Migration to Gold Layer
Format: parquet

Method: CETAS – Create External Table As Select

Output: Cleaned and aggregated tables for analytics and reporting

📊 Visualization
You can connect Power BI or Tableau to Azure Synapse for interactive dashboards and insights.

📚 Summary
This project is a hands-on demonstration of a complete big data pipeline leveraging Azure cloud tools, focusing on:

Real-world e-commerce data

Scalable and modular design (Medallion Architecture)

Integration of ingestion, processing, storage, and analytics layers
