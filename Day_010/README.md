# Day 10 — Machine Learning with Linear Regression

**Date:** 15 October 2026  
**Program:** AI/ML Internship

## Overview

Day 10 focused on understanding the Machine Learning workflow and implementing a Linear Regression model using the California Housing dataset.

The task covered data inspection, missing-value handling, categorical encoding, feature engineering, train-test splitting, feature scaling, model training, and performance evaluation.

## Learning Objectives

- Understand the Machine Learning workflow from data collection to prediction.
- Learn how Linear Regression predicts continuous numerical values.
- Prepare real-world data for model training.
- Perform feature engineering to create meaningful input variables.
- Split data into training and testing sets.
- Train a Linear Regression model using Scikit-learn.
- Evaluate predictions using regression metrics.

## Dataset

**Dataset:** California Housing Prices  
**Source:** [Kaggle — California Housing Prices](https://www.kaggle.com/datasets/camnugent/california-housing-prices)

The dataset contains information about California housing districts, including geographic location, population, housing characteristics, median income, and median house value.

**Target variable:** `median_house_value`

The objective is to predict median house values using the available housing and demographic features.

## Workflow Implemented

### 1. Data Loading and Inspection

Loaded `housing.csv` using KaggleHub and Pandas.

Used the following methods to understand the dataset:

- `head()` and `tail()`
- `info()`
- `describe()`
- `isnull().sum()`
- `duplicated().sum()`

### 2. Data Cleaning

- Identified missing values.
- Removed rows containing missing values during the initial cleaning stage.
- Checked for duplicate records.
- Applied median imputation to the training and testing feature sets before scaling.

### 3. Categorical Encoding

Applied `OneHotEncoder` to the `ocean_proximity` column to convert categorical location information into numerical features suitable for the regression model.

### 4. Exploratory Data Analysis

Created visualizations to investigate the dataset:

- **Box plot:** Examined the distribution and potential outliers in median house values.
- **Histogram with KDE:** Explored the distribution of median house values.
- **Correlation analysis:** Examined correlations between numerical features and the target.
- **Correlation heatmap:** Visualized relationships among features.
- **Geographic scatter plot:** Displayed latitude and longitude, with color representing median house values.

### 5. Feature Engineering

Created three additional features to represent housing characteristics:

- `rooms_per_house` — Total rooms divided by households.
- `bedrooms_per_room` — Total bedrooms divided by total rooms.
- `population_per_household` — Population divided by households.

Removed the original `total_rooms`, `total_bedrooms`, `population`, and `households` columns after creating these features.

Infinite values generated during feature engineering were replaced with missing values for subsequent handling.

### 6. Train-Test Split

Separated the input features (`X`) from the target variable (`y`) and split the data into training and testing sets.

- **Training set:** 80%
- **Testing set:** 20%
- **Random state:** 20

This separation allows model performance to be evaluated on data not used for training.

### 7. Missing-Value Imputation and Feature Scaling

Used `SimpleImputer(strategy="median")` to handle missing values in the feature sets.

Applied `StandardScaler` to standardize the features before training the model.

The imputer and scaler were fitted on the training data and then applied to the testing data to avoid fitting preprocessing transformations on the test set.

### 8. Model Training

Trained a Linear Regression model using Scikit-learn.

```python
from sklearn.linear_model import LinearRegression

model = LinearRegression()
model.fit(x_train_sc, y_train)
```

The trained model learned relationships between the input features and median house values.

### 9. Prediction and Evaluation

Generated predictions on the test set and evaluated the model using three regression metrics:

- **Mean Absolute Error (MAE):** Measures the average absolute difference between actual and predicted values.
- **Root Mean Squared Error (RMSE):** Measures prediction error while penalizing larger errors more heavily.
- **R² Score:** Measures how much of the variation in the target is explained by the model.

Created an actual-versus-predicted scatter plot with a reference line for perfect predictions.

Also generated a comparison table containing actual prices, predicted prices, signed differences, and absolute differences for the first ten test observations.

## Technologies Used

- **Python 3** — Programming and model implementation.
- **Pandas** — Data manipulation and preprocessing.
- **NumPy** — Numerical computations.
- **Matplotlib** — Data visualization.
- **Seaborn** — Statistical visualization.
- **KaggleHub** — Dataset loading.
- **Scikit-learn** — Preprocessing, train-test splitting, Linear Regression, and evaluation.
- **Jupyter Notebook** — Development environment.

## Key Learnings

- Understanding the end-to-end Machine Learning workflow.
- Preparing categorical and numerical data for modeling.
- Using one-hot encoding for categorical variables.
- Engineering new features from existing columns.
- Separating training and testing data for model evaluation.
- Applying median imputation and feature scaling.
- Training a regression model and evaluating its predictions.
- Interpreting MAE, RMSE, and R².
- Visualizing prediction errors through actual-versus-predicted comparisons.

## Conclusion

Day 10 applied the fundamental Machine Learning workflow to a real-world housing dataset. The task combined data cleaning, exploratory analysis, feature engineering, preprocessing, model training, and regression evaluation in a single notebook.

This exercise established a foundation for building and evaluating more advanced Machine Learning models.

---

**Internship Task:** Day 10 — Linear Regression  
**Status:** Completed
