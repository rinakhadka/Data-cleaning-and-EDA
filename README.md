# Data Cleaning & Exploratory Data Analysis with SQL

## Overview

This repository contains SQL projects focused on **data cleaning, transformation, and exploratory data analysis (EDA)** using real-world datasets.

The projects demonstrate how raw and inconsistent datasets can be transformed into structured, analysis-ready data using SQL.

The repository currently includes two projects:

1. **Global Layoffs Data Cleaning & EDA**
2. **Nashville Housing Data Cleaning**

---

# Project 1: Global Layoffs Data Cleaning & EDA

## Project Overview

This project focuses on cleaning and analyzing a global layoffs dataset containing information about companies, industries, locations, countries, dates, and the number of employees affected by layoffs.

The objective was to transform the raw dataset into a cleaner and more consistent dataset and then perform exploratory analysis to identify trends and patterns in layoffs.

### Business Questions

The analysis explores questions such as:

- Which companies had the highest number of layoffs?
- Which industries were affected the most?
- Which countries experienced the highest number of layoffs?
- Which locations had the most layoffs?
- How did layoffs change over time?
- Which company stages experienced the most layoffs?
- Which companies had the highest layoffs in each year?
- How did cumulative layoffs change over time?

## Data Cleaning

The cleaning process included:

- Creating a staging table to preserve the original dataset
- Identifying duplicate records
- Removing duplicate records using `ROW_NUMBER()`
- Standardizing inconsistent industry values
- Handling missing and NULL values
- Populating missing industry values where possible
- Standardizing country names
- Converting date values into the appropriate date format
- Removing records that could not contribute meaningfully to the analysis
- Removing temporary columns after cleaning

## Exploratory Data Analysis

After cleaning the data, SQL was used to analyze:

- Total layoffs by company
- Total layoffs by industry
- Total layoffs by country
- Total layoffs by location
- Layoffs by year
- Layoffs by company stage
- Top companies by yearly layoffs
- Rolling totals over time

## SQL Techniques Used

- `SELECT`
- `WHERE`
- `GROUP BY`
- Aggregate functions
- `JOIN`
- `UPDATE`
- `DELETE`
- `ALTER TABLE`
- `CASE`
- String functions
- Date functions
- Common Table Expressions (CTEs)
- Temporary tables
- `ROW_NUMBER()`
- `DENSE_RANK()`
- Window functions
- Rolling calculations
- NULL handling
- Data type conversion

## Key Skills Demonstrated

This project demonstrates my ability to:

- Work with messy real-world datasets
- Identify data-quality issues
- Clean and standardize data using SQL
- Detect and remove duplicate records
- Handle missing values
- Transform data into analysis-ready formats
- Use advanced SQL techniques for analysis
- Translate business questions into SQL queries
- Identify trends and patterns from data

---

# Project 2: Nashville Housing Data Cleaning

## Project Overview

This project focuses on cleaning a Nashville housing dataset using SQL.

The objective was to transform raw housing data into a more structured and consistent dataset suitable for further analysis.

## Data Cleaning Tasks

The project includes SQL techniques for:

- Standardizing property addresses
- Splitting address information into separate columns
- Converting data into appropriate formats
- Handling NULL values
- Standardizing categorical values
- Removing duplicate records
- Removing unnecessary columns
- Improving the overall structure and consistency of the dataset

## SQL Techniques Used

- `UPDATE`
- `ALTER TABLE`
- `DELETE`
- `JOIN`
- `CASE`
- String functions
- `SUBSTRING`
- `PARSENAME`
- `ISNULL`
- CTEs
- Duplicate detection
- Data type conversion

## Key Skills Demonstrated

This project helped strengthen my ability to:

- Work with imperfect real-world datasets
- Identify common data-quality problems
- Transform unstructured information into useful columns
- Standardize inconsistent data
- Prepare datasets for analysis

---

