# CEN-4930C-Database

Database + dataset repository for CEN-4930C.

This repo currently contains a raw dataset (`deals_raw.csv`) intended to be imported into a relational database (e.g., PostgreSQL / MySQL / SQLite) for querying, cleaning, and analysis.

## Contents

- `deals_raw.csv` — raw deals dataset (source file for import)
- `README.md` — project documentation

- The CSV (deals_raw.csv) includes these columns (from the header row):
    - collected_at
    - dealID
    - title
    - storeID
    - salePrice
    - normalPrice
    - savings
    - metacriticScore
    - steamRatingPercent
    - dealRating
  
## Project goals

- Store the raw dataset in a structured SQL database
- Define a repeatable import process (CSV → table)
- Enable SQL queries for analysis (filters, joins, aggregates, etc.)
- (Optional) Normalize data into multiple tables if needed

## Requirements

Use any SQL database you want. Examples below use **PostgreSQL**.

- PostgreSQL 14+ (recommended)
- `psql` CLI (or pgAdmin)

## Quick start (PostgreSQL)

### 1) Create a database

```bash
createdb cen4930c_db
