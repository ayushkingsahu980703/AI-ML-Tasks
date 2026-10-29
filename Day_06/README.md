# Day 6 — Data Visualization with Python

**Date:** 10 October 2026  
**Program:** AI/ML Internship

## Overview

Day 6 focused on understanding data visualization and using Python libraries to represent data graphically. Using an ODI cricket statistics dataset, I created visualizations to compare player performance, examine career run distributions, and analyze century-scoring records.

The task involved working with Matplotlib, Seaborn, and Plotly to create both static and interactive charts.

## Learning Objectives

- Understand the importance of data visualization in data analysis.
- Create bar charts, line charts, histograms, and pie charts.
- Compare player statistics using visual representations.
- Identify patterns and distributions in numerical data.
- Practice creating static and interactive visualizations.
- Draw meaningful observations from charts.

## Dataset

**Dataset:** `Cricket (1).csv`

The dataset contains ODI cricket statistics, including player names, career runs, matches, innings, batting average, and centuries.

## Visualizations Created

### 1. Bar Chart — Top 10 ODI Batters by Career Runs

Created a horizontal bar chart using Seaborn to compare the career runs of the top 10 ODI batters.

- Used `nlargest()` to select the top run-scorers.
- Used `sort_values()` to order players by career runs.
- Added chart titles and axis labels for readability.

An interactive version of the bar chart was also created using Plotly Express, with additional player statistics available on hover.

### 2. Histogram — Distribution of Career Runs

Created histograms using Seaborn and Plotly to examine the distribution of career runs across the dataset.

- Visualized the frequency distribution of player career totals.
- Used bins to group players by career runs.
- Added a KDE curve to the Seaborn histogram.
- Used a marginal box plot in Plotly to provide an additional view of the distribution.

### 3. Pie Chart — Share of Centuries Among Top 5 Players

Created a pie chart using Matplotlib to represent the distribution of centuries among the five players with the highest century counts.

- Selected the top five players based on centuries.
- Displayed player names as labels.
- Added percentage annotations to compare their contributions.

### 4. Line Chart — Player vs Career Runs

Created an interactive Plotly line chart to visualize career runs by player, using markers to identify individual data points.

This exercise provided practice with Plotly's interactive charting capabilities.

## Technologies Used

- **Python 3**
- **Pandas** — Loading and working with tabular data.
- **NumPy** — Numerical computing.
- **Matplotlib** — Static charts and plots.
- **Seaborn** — Statistical data visualization.
- **Plotly Express** — Interactive visualizations.
- **Jupyter Notebook** — Development environment.

## Key Observations

1. Sachin Tendulkar leads the dataset in career runs, with **18,426 runs**.
2. The histogram shows that most players in the selected dataset have career totals substantially lower than Tendulkar's, with a few high-scoring players extending the distribution toward higher values.
3. Sachin Tendulkar has the highest century count in the dataset, with **49 centuries**.
4. The bar chart makes comparisons among the highest run-scorers easier than examining the raw table alone.

## Key Learnings

- Selecting appropriate chart types for different analytical questions.
- Using bar charts to compare numerical values across categories.
- Using histograms to understand numerical distributions.
- Using pie charts to visualize proportions within a selected group.
- Creating interactive charts with Plotly Express.
- Improving chart readability through titles, labels, sorting, and annotations.
- Converting raw cricket statistics into interpretable visual insights.

## Conclusion

Day 6 demonstrated how data visualization can make numerical datasets easier to interpret. By exploring ODI cricket statistics through multiple chart types, I practiced comparing player performance, examining distributions, and communicating observations using Matplotlib, Seaborn, and Plotly.

---

**Internship Task:** Day 6 — Data Visualization  
**Status:** Completed
