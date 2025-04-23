# 🧱 Medallion Architecture Data Pipeline (Bronze → Silver → Gold)

This project demonstrates a simple data engineering pipeline using Delta Lake and the Medallion architecture on Databricks.

## 📂 Layers

- **Bronze Layer**: Raw data ingested directly from a CSV.
- **Silver Layer**: Cleaned and transformed data. Array-like strings are parsed and split into individual columns.
- **Gold Layer**: Aggregated and business-level metrics (e.g., counts and averages).

## 📁 Project Structure

- `large_array_data.csv`: Sample input data with complex arrays and nested formats.
- `notebook.ipynb`: Full ETL pipeline implementation using PySpark and Delta Lake.
- Delta tables are saved in Databricks (not included in repo).

## 🔧 Key Features

- Identifies and splits array columns from stringified JSON arrays.
- Implements Medallion architecture:
  - Save raw data → Bronze table
  - Clean and normalize → Silver table
  - Aggregate → Gold table
- Uses Delta Lake format for reliability and performance.

## 🧪 How to Run

1. Upload the notebook to your Databricks workspace.
2. Upload `large_array_data.csv` to DBFS (e.g., `/FileStore/tables/`).
3. Run the notebook step-by-step to build all layers.

