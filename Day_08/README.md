# Day 8 — Data Preprocessing with Pandas

**Date:** 13 October 2026  
**Program:** AI/ML Internship

## Overview

Day 8 focused on data preprocessing using Pandas and a real-world Bike Sharing Dataset. The task involved inspecting the dataset, identifying missing values and duplicate records, renaming columns, converting data types, and exploring bike rental patterns through visualizations.

This exercise demonstrated the importance of data quality and consistency before performing further data analysis or building machine learning models.

## Learning Objectives

- Understand the importance of data preprocessing.
- Load and inspect a real-world dataset.
- Identify missing values and duplicate records.
- Rename columns for improved readability.
- Convert columns to appropriate data types.
- Explore relationships between bike rentals and different factors.
- Visualize data using Seaborn and Matplotlib.

## Dataset

**Dataset:** Bike Sharing Dataset — `hour.csv`  
**Source:** Kaggle, `lakshmi25npathi/bike-sharing-dataset`

The dataset contains **17,379 records and 17 columns** describing hourly bike rental activity.

Important columns include:

- `date` — Date of the observation.
- `season` — Season indicator.
- `hr` — Hour of the day.
- `weekday` — Day of the week.
- `workingday` — Whether the day is a working day.
- `weathersit` — Weather condition category.
- `temp` — Normalized temperature.
- `hum` — Humidity.
- `casual` — Casual users' rentals.
- `registered` — Registered users' rentals.
- `cnt` — Total bike rentals.

## Tasks Completed

### 1. Data Loading and Inspection

Loaded the hourly dataset using Pandas and KaggleHub.

Used the following methods to understand the dataset:

- `head()` — Preview records.
- `info()` — Inspect column types and non-null counts.
- `describe()` — Generate descriptive statistics.
- `columns` — Examine column names.

### 2. Missing Value Analysis

Checked for missing values using:

```python
df.isnull().sum()
```

**Result:** No missing values were found in the dataset.

### 3. Duplicate Detection

Checked for duplicate rows using:

```python
df.duplicated().sum()
```

**Result:** No duplicate records were found, so no duplicate-removal operation was necessary.

### 4. Column Renaming

Renamed the original `dteday` column to `date` to make its meaning clearer.

```python
df = df.rename(columns={'dteday': 'date'})
```

### 5. Data Type Conversion

Converted the `date` column from an object/string representation to Pandas datetime format.

```python
df['date'] = pd.to_datetime(df['date'])
```

Verified the updated data type using `df.info()`.

## Data Visualization

Created visualizations using Seaborn and Matplotlib to explore rental patterns.

### 1. Bike Rentals by Hour

A line plot examined average rental counts across different hours of the day.

### 2. Bike Rentals by Season

A bar plot compared average rental counts across the four seasonal categories.

### 3. Weather Conditions vs. Bike Rentals

A box plot compared rental-count distributions across weather categories.

### 4. Temperature vs. Bike Rentals

A scatter plot explored the relationship between temperature and total rental counts.

### 5. Registered Users: Working Day vs. Non-Working Day

A bar plot compared registered-user rentals across working-day categories.

### 6. Bike Rentals by Weekday

A bar plot compared average rental counts across the days of the week.

### 7. Bike Rentals: Holidays vs. Non-Holidays

A bar plot examined rental counts across holiday and non-holiday categories.

## Technologies Used

- **Python 3** — Programming language.
- **Pandas** — Data inspection and preprocessing.
- **NumPy** — Numerical computing.
- **Matplotlib** — Visualization.
- **Seaborn** — Statistical plotting.
- **KaggleHub** — Dataset loading.
- **Jupyter Notebook** — Interactive development environment.

## Key Learnings

- Data preprocessing is an important step in the data analysis workflow.
- Missing values and duplicate records should be checked before analysis.
- Clear column names improve code readability.
- Correct data types enable appropriate date-based operations.
- Visualizations help explore relationships between rental activity, time, weather, and working-day conditions.
- A dataset can require preprocessing even when no missing values or duplicate records are present.

## Conclusion

Day 8 applied fundamental data preprocessing techniques to an hourly bike-sharing dataset. After validating data quality, renaming the date column, and converting it to datetime format, I explored rental patterns using seven visualizations.

The task reinforced the importance of preparing structured data before conducting deeper analysis or developing machine learning models.

---

**Internship Task:** Day 8 — Data Preprocessing  
**Status:** Completed
