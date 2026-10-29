# Day 9 — Exploratory Data Analysis (EDA)

**Date:** 14 October 2026  
**Program:** AI/ML Internship

## Overview

Day 9 focused on Exploratory Data Analysis (EDA) using the Bike Sharing Dataset. The task involved performing descriptive statistics, identifying demand patterns, creating visualizations, and translating the findings into actionable business insights.

The analysis examined hourly, monthly, and seasonal bike rental trends, along with differences between registered and casual users.

## Learning Objectives

- Perform descriptive statistical analysis using Pandas.
- Identify trends and patterns in real-world data.
- Create meaningful visualizations using Matplotlib and Seaborn.
- Analyze customer usage and demand patterns.
- Translate analytical findings into business insights.
- Understand how EDA can support business planning and decision-making.

## Dataset

**Dataset:** Bike Sharing Dataset — `hour.csv`  
**Source:** [Kaggle — Bike Sharing Dataset](https://www.kaggle.com/datasets/lakshmi25npathi/bike-sharing-dataset)

The dataset contains **17,379 hourly records** of bike-sharing activity, including rental counts, weather conditions, time-related variables, and customer categories.

Key columns used in the analysis:

- `hr` — Hour of the day.
- `mnth` — Month.
- `season` — Season category.
- `workingday` — Working-day indicator.
- `casual` — Casual user rentals.
- `registered` — Registered user rentals.
- `cnt` — Total bike rentals.

## Data Preparation

The cleaned dataset from Day 8 was reused for this analysis.

- Inspected the dataset using `head()`, `info()`, and `describe()`.
- Checked for missing values using `isnull().sum()`.
- Checked for duplicate records using `duplicated().sum()`.
- Renamed `dteday` to `date`.
- Converted the `date` column to datetime format.

**Data quality results:** No missing values or duplicate rows were found.

## Descriptive Statistics

Used Pandas `describe()` to examine the distribution of numerical variables.

| Metric | Average |
|---|---:|
| Casual rentals per hour | 35.68 |
| Registered rentals per hour | 153.79 |
| Total rentals per hour | 189.46 |

The dataset shows that registered users account for a substantially larger share of hourly rentals than casual users.

## Visualizations Created

### 1. Average Bike Rentals by Season

A bar chart compared average rental counts across the four seasons.

**Purpose:** Identify seasonal differences in customer demand and support fleet planning.

### 2. Average Bike Rentals by Hour

A line chart displayed average bike rentals across the 24 hours of the day.

**Purpose:** Identify peak-demand hours and periods suitable for maintenance or redistribution.

### 3. Average Bike Rentals by Month

A line chart compared average rental counts across the 12 months.

**Purpose:** Identify monthly fluctuations and support demand forecasting and marketing plans.

### 4. Registered vs. Casual Users

A grouped bar chart compared average rentals by registered and casual users on working and non-working days.

**Purpose:** Understand customer-segment differences and develop targeted retention and marketing strategies.

## Key Findings

The notebook's calculations identified the following demand patterns:

- **Busiest hour:** 5 PM (17:00).
- **Busiest month by average rentals:** September (month 9).
- **Highest-demand season:** Season category 3.
- **Average registered rentals:** Approximately 154 per hour.
- **Average casual rentals:** Approximately 36 per hour.

These findings highlight the importance of time-based demand planning and customer segmentation.

## Business Insights and Recommendations

### 1. Optimize Bike Availability During Peak Hours

Use hourly rental patterns to position bikes before high-demand periods and schedule maintenance during quieter hours.

### 2. Plan Inventory Around Seasonal Demand

Adjust fleet capacity, staffing, maintenance schedules, and promotional activities according to seasonal and monthly demand.

### 3. Incorporate Weather into Demand Forecasting

Combine historical rental data with weather information to improve demand estimates and resource allocation. Validate weather-related effects before implementing operational changes.

### 4. Develop Separate Strategies for Customer Segments

Focus on retention and membership benefits for registered users while using targeted offers to encourage casual riders to become regular customers.

### 5. Improve Resource Allocation Using Demand Variability

Use demand patterns to reduce bike shortages during busy periods and avoid underutilized inventory during quieter periods.

## Technologies Used

- **Python 3** — Programming and analysis.
- **Pandas** — Data manipulation and descriptive statistics.
- **NumPy** — Numerical computing.
- **Matplotlib** — Visualization.
- **Seaborn** — Statistical plotting.
- **KaggleHub** — Dataset loading.
- **Jupyter Notebook** — Interactive analysis environment.

## Key Learnings

- Using descriptive statistics to summarize real-world datasets.
- Identifying hourly, monthly, and seasonal demand patterns.
- Comparing customer segments through grouped visualizations.
- Translating data analysis into practical business recommendations.
- Understanding how EDA supports resource allocation and business planning.

## Conclusion

Day 9 applied exploratory data analysis to a bike-sharing dataset to understand rental demand across time periods and customer segments. The visualizations and statistical findings were used to develop five business insights related to fleet availability, seasonal planning, weather-aware forecasting, customer retention, and resource allocation.

This task strengthened the connection between data analysis and evidence-based business decision-making.

---

**Internship Task:** Day 9 — Exploratory Data Analysis  
**Status:** Completed
