# Day 11: Telco Customer Churn Classification

## 📌 Project Overview

This project focuses on understanding classification problems by training and comparing two machine learning algorithms: **Logistic Regression** and **Decision Tree Classifier**.

Using the Telco Customer Churn dataset, the objective is to predict whether a customer will leave a telecommunications service based on customer demographics, subscription details, tenure, and billing information.

## 🎯 Objectives

- Understand supervised classification.
- Explore and clean a real-world customer dataset.
- Convert categorical variables into numerical features.
- Train a Logistic Regression model.
- Train a Decision Tree Classifier.
- Compare both models using accuracy.
- Evaluate predictions using a confusion matrix and classification report.

## 📊 Dataset

**Dataset:** Telco Customer Churn

**Source:** [Kaggle — Telco Customer Churn](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)

The dataset contains customer information and a target column, `Churn`, indicating whether a customer left the service.

- Original records: 7,043
- Records after cleaning: 7,032
- Features used: 30 encoded input features
- Target variable: `Churn`
- Training set: 5,625 records
- Testing set: 1,407 records

## ⚙️ Workflow

### 1. Data Exploration
- Inspected the dataset's dimensions, data types, and descriptive statistics.
- Examined churn distribution, missing values, and duplicate records.

### 2. Data Cleaning
- Converted `TotalCharges` to a numeric data type.
- Removed rows containing missing values.
- Dropped `customerID` because it is an identifier rather than a useful predictive feature.

### 3. Feature Engineering and Preprocessing
- Applied one-hot encoding using `pd.get_dummies()`.
- Converted the target variable into binary values:
  - `0` — No churn
  - `1` — Churn
- Split the data into training and testing sets using an 80:20 ratio.
- Applied `StandardScaler` to the features for Logistic Regression.

### 4. Model Training
- Logistic Regression
- Decision Tree Classifier

### 5. Model Evaluation
- Compared test accuracy.
- Visualized model performance using a bar chart.
- Examined confusion matrices, precision, recall, and F1-score.

## 📈 Model Performance

Both models were evaluated on the same test dataset.

| Model | Test Accuracy |
|---|---:|
| Logistic Regression | 80.38% |
| Decision Tree | 71.86% |

**Best-performing model by accuracy: Logistic Regression**

Logistic Regression achieved an accuracy approximately 8.52 percentage points higher than the Decision Tree in this experiment.

## 🔍 Key Observations

- Logistic Regression performed better than the default Decision Tree on the test set.
- Feature scaling was applied to Logistic Regression but was not required for the Decision Tree.
- The Decision Tree may benefit from controlling its complexity to reduce overfitting.
- Accuracy alone does not fully describe churn prediction performance because the target classes are imbalanced.
- The confusion matrix and classification report provide additional insights into how effectively each model identifies customers who churn.

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

## 📂 Project Structure

```text
ai-ml-tasks/
└── Day-11/
    ├── day_11_classification.ipynb
    └── README.md
```

## ▶️ How to Run

1. Download the dataset from the Kaggle link above.
2. Place the CSV file in the appropriate location.
3. Open `day_11_classification.ipynb` in Jupyter Notebook or Google Colab.
4. Update the dataset path in the notebook if necessary.
5. Run the cells sequentially to reproduce the preprocessing, model training, and evaluation.

## 📚 Key Learnings

- Difference between classification and regression.
- Categorical feature encoding.
- Training and testing data separation.
- Feature scaling and data leakage prevention.
- Training Logistic Regression and Decision Tree models.
- Comparing classification models using accuracy.
- Interpreting confusion matrices and classification reports.

---

**Day 11 completed:** Trained two classification models and compared their performance using the Telco Customer Churn dataset.
