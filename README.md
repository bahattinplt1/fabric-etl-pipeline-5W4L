Project Title: Microsoft Fabric – ETL Pipeline with Lakehouse

Description:
This project demonstrates how to build an end-to-end ETL (Extract, Transform, Load) pipeline using Microsoft Fabric. 
The data is ingested from a public HTTP source, transformed using a Spark notebook, and stored in a Lakehouse table.

Tools Used:
- Microsoft Fabric (Trial)
- Lakehouse (OneLake)
- Apache Spark (Notebook)
- Data Pipeline

Source Data:
We use a single CSV file available publicly:
https://raw.githubusercontent.com/MicrosoftLearning/dp-data/main/sales.csv

👉 This is the only external file needed for the project. Nothing else is required.

Project Steps:
1. Created a Microsoft Fabric workspace (trial enabled)
2. Created a Lakehouse and added a 'new_data' folder under Files
3. Built a data pipeline:
   - Used HTTP source to ingest 'sales.csv'
   - Saved it to 'new_data' folder
4. Created a Spark notebook:
   - Transformed data by adding Year, Month, FirstName, LastName columns
   - Saved the result as a table named 'sales'
5. Enhanced the pipeline:
   - Added 'Delete data' activity to remove existing .csv files
   - Added 'Notebook' activity to run the transformation with a parameter table_name = new_sales

Screenshots:
All steps are documented with screenshots included in the repository:
- workspace_creation.png
- pipeline_config.png
- notebook_run.png
- table_preview.png

Result:
After running the pipeline, a table called 'new_sales' is created in the Lakehouse with clean and enriched sales data.

License:
MIT License
