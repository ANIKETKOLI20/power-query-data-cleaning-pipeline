# Data Cleaning Pipeline using Power Query (Production-Style ETL)

## Project Overview

This project demonstrates a structured ETL pipeline using Power Query to clean and validate raw order data.

The goal was to simulate a real-world data cleaning workflow with audit tracking and data quality reporting.

---

## Dataset Issues Identified

The raw dataset contained multiple data quality problems:

- Duplicate OrderIDs
- Invalid Age values (negative, text, out-of-range)
- Null Customer records
- Inconsistent formatting

These issues make downstream analysis unreliable.

---

## ETL Architecture

The pipeline follows a layered architecture:

Raw Layer:

- raw_data
- Preserves original source

Staging Layer:

- stg_orders
- Standardizes formatting and data types

Validation Layer:

- val_orders
- Flags:
    - Duplicate records
    - Invalid age values
    - Null customer records

Clean Layer:

- clean_data
- Contains only valid records

Rejected Layer:

- error_log_table
- Stores invalid records for audit tracking

Reporting Layer:

- data_quality_summary
- Tracks cleaning metrics

---

## Data Quality Results

| Metric | Value |
| --- | --- |
| Total Rows Before | 10 |
| Total Rows After | 4 |
| Rows Removed | 6 |
| Duplicate Records | 1 |
| Invalid Age Records | 4 |
| Null Customer Records | 1 |

---

## Tools Used

- Microsoft Excel
- Power Query
- ETL Design Principles

---

## Key Skills Demonstrated

- Data Cleaning
- Data Validation
- ETL Pipeline Design
- Data Quality Monitoring
- Power Query

---

## Project Files

power_query_data_cleaning.xlsx

---

## Author

Aniket Koli

Aspiring Data Analyst
