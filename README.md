# Data Cleaning & Exploratory Data Analysis with SQL

This repository contains SQL projects focused on **data cleaning, data transformation, and exploratory data analysis (EDA)** using real-world datasets.

The projects demonstrate how raw and inconsistent data can be transformed into cleaner, structured, and analysis-ready data using SQL.

---

## Projects

### 1. Global Layoffs Data Cleaning & EDA
**Database:** MySQL

An end-to-end SQL project that cleans and analyzes a global layoffs dataset.

**Workflow:**

Raw Data → Data Cleaning → Data Transformation → Exploratory Data Analysis → Insights

### 2. Nashville Housing Data Cleaning
**Database:** SQL Server

A data-cleaning project focused on preparing a Nashville housing dataset for further analysis.

---

# 1. Global Layoffs Data Cleaning & EDA

## Project Overview

The Global Layoffs project analyzes a dataset containing information about company layoffs, including:

- Companies
- Industries
- Locations
- Countries
- Layoff numbers
- Percentage of employees laid off
- Dates
- Company stages
- Funds raised

The main goal was to identify data-quality issues, clean the dataset, and perform exploratory analysis to understand patterns in layoffs across companies, industries, locations, countries, and time.

---

## Data Cleaning

The raw dataset contained duplicate records, missing values, inconsistent categories, and incorrectly formatted dates.

The cleaning process included:

- Creating staging tables to preserve the raw dataset
- Identifying duplicate records
- Removing duplicate records using `ROW_NUMBER()`
- Standardizing inconsistent industry values
- Converting blank industry values to `NULL`
- Filling missing industry values using a self-join where possible
- Standardizing country names
- Removing unwanted characters from country values
- Converting text dates into proper date format
- Investigating missing values
- Removing records where both total layoffs and percentage layoffs were unavailable
- Removing temporary columns after cleaning

---

## Exploratory Data Analysis

After cleaning the dataset, SQL was used to investigate different aspects of global layoffs.

### Layoff Size

- Identified the largest single layoff event
- Found the maximum and minimum percentage of employees laid off
- Identified companies where 100% of employees were laid off
- Compared fully affected companies based on funds raised

### Company Analysis

- Identified companies with the largest individual layoff events
- Ranked companies by total layoffs

### Location & Country Analysis

- Ranked locations by total layoffs
- Compared total layoffs across countries

### Industry Analysis

- Analyzed total layoffs across different industries

### Company Stage Analysis

- Compared layoffs across different company stages

### Time Analysis

- Analyzed layoffs by year
- Analyzed layoffs by month
- Calculated rolling cumulative layoffs over time

### Yearly Company Ranking

Used `DENSE_RANK()` to identify the top three companies with the highest number of layoffs for each year.

---

## SQL Techniques Used

This project demonstrates practical SQL skills including:

- `SELECT`
- `WHERE`
- `GROUP BY`
- `ORDER BY`
- Aggregate functions such as `SUM()` and `MAX()`
- `JOIN`
- Self-joins
- Common Table Expressions (CTEs)
- `ROW_NUMBER()`
- `DENSE_RANK()`
- Window functions
- Rolling calculations
- `CASE`
- NULL handling
- Date conversion
- String manipulation
- Data standardization

---

## Key Skills Demonstrated

Through this project, I practiced:

- Working with messy real-world data
- Identifying data-quality problems
- Removing duplicate records
- Handling missing values
- Standardizing inconsistent data
- Transforming raw data into analysis-ready data
- Writing analytical SQL queries
- Using SQL window functions
- Ranking data
- Performing time-based analysis
- Extracting insights from datasets

---

# 2. Nashville Housing Data Cleaning

## Project Overview

This project focuses on cleaning and transforming a Nashville housing dataset using **SQL Server**.

The objective was to improve the consistency and structure of the raw housing data so that it could be used for further analysis.

---

## Data Cleaning Tasks

### Standardizing Dates

Converted the original sale date into a proper SQL Server `DATE` format.

### Handling Missing Property Addresses

Used a self-join based on `ParcelID` to populate missing property addresses when another record for the same property contained the address.

### Splitting Property Addresses

Separated the property address into:

- Property Address
- Property City

using SQL string functions.

### Splitting Owner Addresses

Separated the owner address into:

- Owner Address
- Owner City
- Owner State

using `PARSENAME()` and `REPLACE()`.

### Standardizing Sold-As-Vacant Values

Converted:

- `1` → `Yes`
- `0` → `No`

to make the categorical values easier to understand.

### Removing Duplicates

Used `ROW_NUMBER()` with `PARTITION BY` to identify duplicate housing records.

### Removing Unused Columns

Removed columns that were no longer required after the cleaning and transformation process.

---

## SQL Server Techniques Used

- `SELECT`
- `UPDATE`
- `ALTER TABLE`
- `DROP COLUMN`
- `JOIN`
- Self-joins
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

---

# Tools & Technologies

| Project | Database | Focus |
|---|---|---|
| Global Layoffs | MySQL | Data Cleaning + EDA |
| Nashville Housing | SQL Server | Data Cleaning |

**Tools:** SQL, MySQL, SQL Server, GitHub

---
