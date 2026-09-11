# Data Cleaning & Exploratory Data Analysis with SQL

## Overview

This repository contains two SQL projects focused on working with real-world datasets through data cleaning, transformation, and exploratory data analysis.

The projects demonstrate how raw and inconsistent datasets can be transformed into cleaner, structured, and analysis-ready data using SQL.

### Projects

1. Global Layoffs Data Cleaning & EDA — MySQL
2. Nashville Housing Data Cleaning — SQL Server

---

# 1. Global Layoffs Data Cleaning & EDA

## Project Overview

This project analyzes a global layoffs dataset containing information about companies, industries, locations, countries, dates, company stages, and layoffs.

The project follows an end-to-end workflow:

**Raw Data → Data Cleaning → Data Transformation → Exploratory Data Analysis → Insights**

The main objective was to clean the raw dataset and explore patterns and trends in layoffs across companies, industries, locations, countries, and time.

## Data Cleaning

The cleaning process included:

- Creating staging tables to work with the raw data
- Identifying duplicate records
- Removing duplicate records using `ROW_NUMBER()`
- Standardizing inconsistent industry values
- Converting blank industry values to NULL
- Populating missing industry values where possible using a self-join
- Standardizing country values
- Converting date values into the appropriate date format
- Identifying missing values
- Removing records where both total layoffs and percentage layoffs were unavailable
- Removing temporary columns after the cleaning process

## Exploratory Data Analysis

After cleaning the dataset, SQL was used to explore trends, patterns, and potential outliers.

The analysis includes:

### Layoff Size

- Identified the largest single layoff event
- Examined the maximum and minimum percentage of employees laid off
- Investigated companies where 100% of employees were laid off
- Compared fully affected companies based on funds raised

### Company Analysis

- Identified companies with the largest individual layoff events
- Identified companies with the highest total layoffs

### Location & Country Analysis

- Ranked locations by total layoffs
- Compared total layoffs across countries

### Industry Analysis

- Compared total layoffs across different industries

### Company Stage Analysis

- Compared layoffs across different company stages

### Time Analysis

- Analyzed total layoffs by year
- Analyzed monthly layoffs
- Calculated a rolling cumulative total of layoffs over time

### Yearly Company Ranking

Used `DENSE_RANK()` to identify the top three companies with the highest layoffs for each year.

## SQL Techniques Used

- `SELECT`
- `WHERE`
- `GROUP BY`
- `ORDER BY`
- Aggregate functions such as `SUM()` and `MAX()`
- `LIMIT`
- `YEAR()`
- `SUBSTRING()`
- Common Table Expressions (CTEs)
- `ROW_NUMBER()`
- `DENSE_RANK()`
- Window functions
- Rolling calculations
- `JOIN`
- NULL handling
- Data type conversion
- Data standardization

## Key Skills Demonstrated

This project demonstrates my ability to:

- Work with messy real-world data
- Identify data-quality issues
- Clean and standardize datasets
- Detect and remove duplicate records
- Handle missing values
- Transform data into analysis-ready formats
- Use SQL window functions
- Perform exploratory data analysis
- Rank data using window functions
- Analyze trends over time
- Translate analytical questions into SQL queries
- Identify patterns and potential outliers

---

# 2. Nashville Housing Data Cleaning

## Project Overview

This project focuses on cleaning a Nashville housing dataset using SQL Server.

The objective was to improve the structure and consistency of the raw housing data so that it could be used more effectively for further analysis.

## Data Cleaning Tasks

The project includes:

### Standardizing Dates

Converted the original sale date into a proper SQL Server `DATE` format and created a converted date column.

### Populating Missing Property Addresses

Used a self-join based on `ParcelID` to populate missing property addresses where another record for the same property contained the address.

### Splitting Property Addresses

Separated property address information into:

- Property Address
- Property City

using SQL string functions.

### Splitting Owner Addresses

Used `PARSENAME()` and `REPLACE()` to separate the owner address into:

- Owner Address
- Owner City
- Owner State

### Standardizing Sold-As-Vacant Values

Converted numeric values:

- `1` → `Yes`
- `0` → `No`

to make the field easier to interpret.

### Removing Duplicates

Used `ROW_NUMBER()` with `PARTITION BY` to identify duplicate housing records.

### Removing Unused Columns

Removed columns that were no longer needed after the cleaning and transformation process.

## SQL Server Techniques Used

- `SELECT`
- `UPDATE`
- `ALTER TABLE`
- `DROP COLUMN`
- `JOIN`
- `ISNULL()`
- `CASE`
- `SUBSTRING()`
- `CHARINDEX()`
- `LEN()`
- `PARSENAME()`
- `REPLACE()`
- `ROW_NUMBER()`
- CTEs
- Data type conversion

## Key Skills Demonstrated

This project demonstrates my ability to:

- Work with real-world housing data
- Identify missing and inconsistent values
- Populate missing data using joins
- Transform address fields
- Standardize categorical values
- Detect duplicate records
- Remove unnecessary columns
- Use SQL Server string functions
- Prepare data for further analysis

---

# Tools & Technologies

### MySQL

Used for the Global Layoffs Data Cleaning & EDA project.

### SQL Server

Used for the Nashville Housing Data Cleaning project.

### GitHub

Used for project organization, documentation, and version control.

