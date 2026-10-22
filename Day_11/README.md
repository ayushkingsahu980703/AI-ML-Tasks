# Day 11 — Classification Models in Machine Learning

**Date:** 16 October 2026  
**Program:** AI/ML Internship

## Overview

Day 11 focused on understanding supervised classification and training two machine learning models: Logistic Regression and Decision Tree Classifier.

Using a telecom customer churn dataset, the task involved data cleaning, categorical encoding, feature scaling, model training, and comparing classification performance using accuracy.

The notebook also includes confusion matrices and classification reports to examine model performance in more detail.

## Learning Objectives

- Understand classification problems in supervised machine learning.
- Differentiate between classification and regression.
- Prepare categorical and numerical data for classification.
- Train a Logistic Regression model.
- Train a Decision Tree Classifier.
- Compare models using accuracy.
- Interpret confusion matrices and classification reports.

## Dataset

**Dataset:** Telco Customer Churn  
**File:** `WA_Fn-UseC_-Telco-Customer-Churn.csv`

The dataset contains telecom customer information used to predict whether a customer will leave the service.

**Target variable:** `Churn`

- `0` — No churn
- `1` — Customer churned

The features include customer demographics, subscribed services, contract details, payment methods, tenure, and billing information.

## Workflow Implemented

### 1. Exploratory Data Analysis

Used Pandas to inspect the dataset and understand its structure.

Methods included:

- `head()` and `tail()`
- `shape`
- `info()`
- `describe()`
- `value_counts()`
- Missing-value and duplicate checks

### 2. Data Cleaning

- Converted `TotalCharges` to a numeric data type using `pd.to_numeric()`.
- Used `errors='coerce'` to convert invalid values into missing values.
- Removed rows containing missing values.
- Dropped `customerID`, as it is an identifier rather than a meaningful predictive feature.

### 3. Feature Engineering and Encoding

Separated the dataset into input features (`X`) and target variable (`y`).

Applied one-hot encoding to categorical input features using:

```python
X = pd.get_dummies(X, drop_first=True, dtype=int)
```

Encoded the target variable:

```python
y = y.map({"No": 0, "Yes": 1})
```

### 4. Train-Test Split

Split the data into training and testing sets using an 80:20 ratio.

- `test_size=0.2`
- `random_state=42`
- `stratify=y`

Stratification preserved the approximate target-class proportions in both sets.

### 5. Feature Scaling

Applied `StandardScaler` to the training and testing feature sets.

The scaler was fitted on the training data and then applied to the test data.

Scaling was used for Logistic Regression, while the Decision Tree was trained on the unscaled encoded features.

### 6. Logistic Regression

Trained a Logistic Regression model with `max_iter=1000`.

The model learned relationships between customer characteristics and churn probability, then predicted churn labels on the test set.

### 7. Decision Tree Classifier

Trained a Decision Tree Classifier using `random_state=42`.

The model learned decision rules from the training data and generated predictions for the test set.

### 8. Model Comparison

Compared both models using accuracy and visualized the results with a bar chart.

## Model Results

The following results are recorded in the notebook.

| Model | Accuracy |
|---|---:|
| Logistic Regression | 80.38% |
| Decision Tree | 71.86% |
| Difference | 8.52 percentage points |

Logistic Regression achieved higher test accuracy than the default Decision Tree in this experiment.

## Additional Evaluation

The notebook also calculates confusion matrices and classification reports containing precision, recall, and F1-score.

Recorded observations for the churn class:

| Metric | Logistic Regression | Decision Tree |
|---|---:|---:|
| Recall | 57% | 46% |

Logistic Regression also achieved better churn-class precision and F1-score in this experiment.

Both models missed some customers who actually churned, demonstrating why accuracy alone is insufficient for evaluating a churn prediction system.

## Technologies Used

- **Python 3** — Programming and implementation.
- **Pandas** — Data manipulation and preprocessing.
- **NumPy** — Numerical operations.
- **Matplotlib** — Visualization.
- **Seaborn** — Data exploration.
- **Scikit-learn** — Preprocessing, model training, train-test splitting, and evaluation.
- **Jupyter Notebook** — Development environment.

## Key Learnings

- Classification predicts discrete categories rather than continuous values.
- Data cleaning and categorical encoding are essential preprocessing steps.
- Train-test splitting helps evaluate performance on unseen data.
- Feature scaling is useful for Logistic Regression.
- Decision Trees can model nonlinear decision boundaries without requiring feature scaling.
- Accuracy should be considered alongside precision, recall, and F1-score.
- Recall is particularly relevant when missing actual churners has a significant business cost.

## Conclusion

Day 11 implemented and compared two classification algorithms using a telecom customer churn dataset. Logistic Regression outperformed the default Decision Tree in the recorded experiment, achieving 80.38% accuracy compared with 71.86%.

The results also highlighted the importance of evaluating the minority or positive class rather than relying exclusively on overall accuracy. Further hyperparameter tuning and validation would be required before deploying either model in a real-world customer retention system.

---

**Internship Task:** Day 11 — Classification Models  
**Status:** Completed
