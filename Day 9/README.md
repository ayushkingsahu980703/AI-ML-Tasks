# Day 9: Exploratory Data Analysis (EDA) — Bike Sharing Dataset

## 📌 Project Overview

As part of my AI/ML internship, I performed Exploratory Data Analysis (EDA) on a Bike Sharing Dataset to understand rental demand, identify trends and patterns, and derive meaningful business insights.

The objective was to explore the dataset before moving towards machine learning and understand how factors such as time, season, and customer type relate to bike rental demand.

## 🎯 Objectives

- Perform descriptive statistical analysis.
- Inspect data quality, missing values, and duplicate records.
- Identify hourly and monthly rental patterns.
- Compare average bike rentals across seasons.
- Analyze registered and casual user behavior.
- Create meaningful data visualizations.
- Derive actionable business insights.

## 🛠️ Tools & Technologies

- **Python** — Data analysis
- **Pandas & NumPy** — Data manipulation and numerical analysis
- **Matplotlib & Seaborn** — Data visualization
- **Jupyter Notebook** — Analysis and documentation

## 📂 Dataset

The project uses the Bike Sharing Dataset from Kaggle, specifically the hourly rental data (`hour.csv`).

Dataset source: [Bike Sharing Dataset — Kaggle](https://www.kaggle.com/datasets/lakshmi25npathi/bike-sharing-dataset)

### Key Features

| Feature | Description |
|---|---|
| `date` | Rental date, renamed from `dteday` |
| `hr` | Hour of the day |
| `season` | Season code |
| `mnth` | Month |
| `workingday` | Indicates whether the day is a working day |
| `casual` | Number of casual user rentals |
| `registered` | Number of registered user rentals |
| `cnt` | Total bike rentals |

## 🔍 Analysis Performed

### 1. Descriptive Statistics
- Examined numerical summaries using `describe()`.
- Inspected dataset structure and column data types.
- Checked for missing values and duplicate records.
- Converted the date column to datetime format.

### 2. Data Visualization

Four visualizations were created to explore rental patterns:

- **Average Bike Rentals by Season:** Compares average rental demand across seasons.
- **Average Bike Rentals by Hour:** Identifies peak and low-demand hours.
- **Average Bike Rentals by Month:** Examines monthly variations in rental demand.
- **Registered vs. Casual Users:** Compares customer segments across working and non-working days.

## 💡 Business Insights

1. **Fleet Optimization:** Hourly demand patterns can help allocate bikes during peak periods and schedule maintenance during quieter hours.
2. **Seasonal Planning:** Seasonal rental trends can support fleet planning, staffing, and marketing decisions.
3. **Demand Forecasting:** Historical time-based patterns can be used as inputs for forecasting future bike rental demand.
4. **Customer Segmentation:** Comparing registered and casual users can help develop targeted membership and customer retention strategies.
5. **Operational Efficiency:** Understanding demand fluctuations can help reduce bike shortages during busy periods and underutilization during quieter periods.

## 📈 Key Learning Outcomes

- Learned how to explore a dataset before training machine learning models.
- Practiced descriptive statistics and data quality checks.
- Improved my ability to identify patterns through data visualization.
- Understood how exploratory analysis can support business decisions.
- Practiced communicating analytical findings as actionable insights.

## 📁 Project Files

- `Day_9.ipynb` — Jupyter Notebook containing the analysis, visualizations, interpretations, and business insights.

**Part of my AI/ML Internship learning journey — Day 9 completed!** 🚀

#Python #EDA #DataAnalysis #DataVisualization #MachineLearning
