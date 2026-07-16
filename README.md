# Azure Data Factory Incremental Load Project

## Project Overview
This project demonstrates an Incremental Data Load solution using Azure Data Factory.

## Source
- SQL Server
  
## Destination
- Azure Data Lake Storage Gen2 (ADLS Gen2)
- Output Format: Parquet
  
## Project Flow
1. Parent Pipeline reads metadata from the Watermark table.
2. Lookup activity retrieves the tables to process.
3. ForEach activity loops through each table.
4. Child Pipeline is executed for each table.
5. Lookup gets the last watermark value.
6. If new records exist, the Copy Data activity copies only incremental records.
7. Stored Procedure updates the watermark value after a successful load.

## Azure Data Factory Activities Used
- Lookup
- ForEach
- Execute Pipeline
- If Condition
- Copy Data
- Stored Procedure

## Features
- Incremental Data Loading
- Watermark Table Logic
- Dynamic SQL Query
- Parameterized Pipelines
- Parent-Child Pipeline Architecture
- GitHub Integration

## Technologies Used
- Azure Data Factory
- Azure SQL Server
- Azure Data Lake Storage Gen2
- Parquet
- GitHub

## Outcome
Successfully implemented an end-to-end metadata-driven Incremental Load pipeline that copies only new records from SQL Server to ADLS Gen2 and updates the watermark after each successful execution.
