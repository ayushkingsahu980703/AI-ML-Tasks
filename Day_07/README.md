# Day 7 — Sports Statistics Analysis

**Date:** 12 October 2026  
**Program:** AI/ML Internship

## Overview

Day 7 focused on exploratory data analysis (EDA) and data visualization using ODI cricket statistics. The task involved loading a real-world dataset, inspecting and cleaning the data, engineering features from players' career spans, and creating visualizations to identify patterns in batting performance.

The analysis used Python libraries to explore career runs, batting averages, strike rates, career longevity, and century-scoring records.

## Learning Objectives

- Load and inspect a real-world CSV dataset.
- Identify missing values and duplicate records.
- Clean data and convert columns into appropriate data types.
- Perform feature engineering using existing columns.
- Create statistical visualizations using Seaborn and Matplotlib.
- Interpret distributions and summarize findings through data-driven insights.

## Dataset

**Dataset:** `Cricket (1).csv`

The dataset contains ODI cricket statistics for 79 players across 13 original columns.

Key attributes include:

- `Player` — Player name and associated team information.
- `Mat` — Matches played.
- `Inns` — Innings played.
- `NO` — Not-out innings.
- `Runs` — Total career runs.
- `HS` — Highest score.
- `Ave` — Batting average.
- `BF` — Balls faced.
- `SR` — Batting strike rate.
- `100` — Centuries scored.
- `50` — Half-centuries scored.
- `0` — Ducks recorded.
- `Span` — Career period.

## Data Cleaning and Feature Engineering

### 1. Data Inspection

Used Pandas to examine the dataset's structure, column types, and descriptive statistics.

Methods included:

- `head()` and `tail()`
- `info()`
- `describe()`
- `isnull().sum()`
- `duplicated().sum()`

The dataset contained **79 records, no missing values, and no duplicate rows**.

### 2. Career Span Feature Engineering

Split the `Span` column into starting and ending years, converted both values to integers, and calculated career span:

```python
df[['start', 'end']] = df['Span'].str.split('-', expand=True)

df['start'] = df['start'].astype(int)
df['end'] = df['end'].astype(int)

df['experience'] = df['end'] - df['start']
```

The original `Span`, `start`, and `end` columns were subsequently dropped after creating the `experience` feature.

### 3. Highest Score Conversion

The `HS` column contained values such as `200*`, where the asterisk denotes an unbeaten innings. The asterisk was removed so the column could be converted to an integer for numerical analysis.

```python
df['HS'] = df['HS'].str.replace('*', '', regex=False)
df['HS'] = df['HS'].astype(int)
```

## Exploratory Data Analysis and Visualizations

Five visualizations were created using Seaborn and Matplotlib.

### 1. Distribution of Career Runs

Created a histogram with a KDE curve to examine the distribution of total career runs among the selected players.

### 2. Distribution of Batting Average

Visualized batting averages using a histogram with 12 bins and a KDE curve to examine the distribution of player averages.

### 3. Distribution of Strike Rate

Created a histogram with a KDE curve to explore variation in scoring rates across the dataset.

### 4. Distribution of Career Span

Visualized the engineered `experience` feature using a histogram with five bins to understand differences in career longevity.

### 5. Distribution of Centuries

Used a count plot to examine how many players fall into different century-count values.

## Key Insights

1. **Sachin Tendulkar leads career run-scoring:** He has 18,426 ODI runs across 463 matches, substantially above the dataset's mean of approximately 7,618 runs per player.

2. **Batting averages cluster around the high 30s:** The mean batting average is 38.52, while the median is 37.87.

3. **Strike rates vary considerably:** The average strike rate is 79.30, with values ranging from 60.57 to 117.00.

4. **Century production is unevenly distributed:** Players have a mean of 11.56 centuries, a median of 10, and a maximum of 49.

5. **Career longevity matters when comparing cumulative records:** Longer careers provide more opportunities to accumulate runs and centuries. Tendulkar's career span in the dataset is approximately 23 years.

## Technologies Used

- **Python 3** — Programming and analysis.
- **Pandas** — Data loading, cleaning, and manipulation.
- **NumPy** — Numerical computing.
- **Matplotlib** — Chart creation and customization.
- **Seaborn** — Statistical data visualization.
- **Jupyter Notebook** — Interactive analysis environment.

## Key Learnings

- Inspecting and validating real-world datasets before analysis.
- Converting text-based fields into usable numerical features.
- Applying feature engineering to derive career duration.
- Selecting suitable visualizations for numerical distributions.
- Interpreting descriptive statistics alongside charts.
- Communicating analytical findings through concise, evidence-based insights.

## Conclusion

Day 7 applied data cleaning, feature engineering, exploratory data analysis, and visualization to ODI cricket statistics. The project demonstrated how raw player records can be transformed into meaningful insights about career performance, batting consistency, scoring rates, and longevity.

---

**Internship Task:** Day 7 — Sports Statistics Analysis  
**Status:** Completed
