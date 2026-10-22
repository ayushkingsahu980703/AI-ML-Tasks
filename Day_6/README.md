# Day 5 — Data Analysis with Pandas

**Date:** 9 October 2026  
**Program:** AI/ML Internship

## Overview

Day 5 focused on using Pandas for data manipulation and analysis. The task involved loading a Walmart sales dataset, inspecting its structure, examining missing and duplicate values, converting data types, and filtering records using specific conditions.

## Learning Objectives

- Load CSV datasets using Pandas.
- Inspect the structure and dimensions of a DataFrame.
- Understand data types and convert columns when necessary.
- Identify and handle missing values.
- Detect and remove duplicate records.
- Filter datasets using conditional expressions.
- Generate descriptive statistics.

## Dataset

**Dataset:** `Walmart.csv`

The notebook uses Walmart sales data to practice data inspection and filtering.

The columns referenced in the notebook include:

- `Date`
- `Weekly_Sales`
- `Fuel_Price`
- `Temperature`

## Tasks Completed

### 1. Loading and Inspecting Data

Loaded the CSV dataset into a Pandas DataFrame.

```python
import pandas as pd

df = pd.read_csv('Walmart.csv')
```

Explored the dataset using:

- `df.shape` — checks the number of rows and columns.
- `df.info()` — displays column data types and non-null counts.
- `df.columns` — lists column names.
- `df.head()` — displays the first five rows.
- `df.tail()` — displays the last five rows.
- `df.describe()` — generates descriptive statistics for numerical columns.

### 2. Data Type Conversion

Converted the `Date` column into a datetime format for date-related analysis.

```python
df['Date'] = pd.to_datetime(df['Date'], dayfirst=True)
```

The `dayfirst=True` argument specifies day-first date interpretation.

### 3. Missing Value Analysis

Identified missing values using:

```python
df.isnull()
df.isnull().sum()
```

Calculated the percentage of missing values and practiced removing incomplete records using `dropna()`.

The notebook also introduced `fillna()` for handling missing values.

### 4. Duplicate Detection and Removal

Checked for duplicate records and removed them using:

```python
df.duplicated().sum()
df = df.drop_duplicates()
```

This helped practice identifying repeated rows during data cleaning.

### 5. Data Filtering

Applied conditional filtering to identify records based on sales, fuel prices, and temperature.

**Examples from the notebook:**

```python
df.query('Weekly_Sales > 1409727').head()
```

```python
df[(df['Weekly_Sales'] > 1400000)].head(2)
```

```python
df.query('Weekly_Sales > 1400000 and Fuel_Price > 2').head()
```

Also practiced combining multiple conditions using Boolean indexing with the `&` operator.

## Technologies Used

- **Python 3**
- **Pandas**
- **Jupyter Notebook**
- **CSV data**

## Key Learnings

- Loading structured data into a DataFrame.
- Inspecting dataset dimensions, columns, and data types.
- Generating descriptive statistics for numerical data.
- Converting string-based date values into datetime objects.
- Identifying and handling missing values.
- Detecting and removing duplicate records.
- Applying single and multiple filtering conditions.
- Understanding the importance of data cleaning before further analysis.

## Conclusion

Day 5 introduced practical data analysis with Pandas using a Walmart sales dataset. The exercises covered data inspection, type conversion, missing-value analysis, duplicate handling, and conditional filtering. These skills form an important foundation for exploratory data analysis and machine learning workflows.

---

**Internship Task:** Day 5 — Pandas Fundamentals  
**Status:** Completed
