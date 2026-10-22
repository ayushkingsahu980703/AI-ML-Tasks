# Day 12 — Model Evaluation Metrics

**Date:** 17 October 2026  
**Program:** AI/ML Internship

## Overview

Day 12 focused on evaluating the classification models developed on Day 11 using the Telco Customer Churn dataset. The task involved calculating accuracy, precision, recall, and F1-score, generating confusion matrices, and determining which evaluation metric is most useful for the dataset.

The Logistic Regression and Decision Tree models were compared to understand their ability to identify customers likely to churn.

## Learning Objectives

- Understand the importance of classification model evaluation.
- Calculate and interpret accuracy, precision, recall, and F1-score.
- Generate and interpret confusion matrices.
- Compare the performance of Logistic Regression and Decision Tree classifiers.
- Identify an appropriate evaluation metric for customer churn prediction.

## Dataset and Models

**Dataset:** Telco Customer Churn

**Target variable:** `Churn`

Two classification models from Day 11 were evaluated:

- Logistic Regression
- Decision Tree Classifier

## Evaluation Metrics

### 1. Accuracy

Measures the proportion of all predictions that are correct.

\[
\text{Accuracy}=\frac{TP+TN}{TP+TN+FP+FN}
\]

### 2. Precision

Measures the proportion of predicted positive cases that are actually positive.

\[
\text{Precision}=\frac{TP}{TP+FP}
\]

For this task, precision indicates how many customers predicted to churn actually churned.

### 3. Recall

Measures the proportion of actual positive cases correctly identified.

\[
\text{Recall}=\frac{TP}{TP+FN}
\]

Recall indicates how effectively the model identifies customers who actually churn.

### 4. F1-Score

The harmonic mean of precision and recall.

\[
F1=2\times\frac{\text{Precision}\times\text{Recall}}{\text{Precision}+\text{Recall}}
\]

F1-score balances precision and recall, making it useful when both false positives and false negatives matter.

### 5. Confusion Matrix

A confusion matrix compares actual labels with predicted labels.

- **True Positive (TP):** Correctly predicted churn.
- **True Negative (TN):** Correctly predicted non-churn.
- **False Positive (FP):** Predicted churn when the customer did not churn.
- **False Negative (FN):** Failed to identify a customer who churned.

## Results

The following results are taken from the classification reports in the task document.

| Metric | Logistic Regression | Decision Tree |
|---|---:|---:|
| Accuracy | 80% | 72% |
| Churn Precision (Class 1) | 65% | 47% |
| Churn Recall (Class 1) | 57% | 46% |
| Churn F1-Score (Class 1) | 61% | 47% |
| Weighted F1-Score | 80% | 72% |

*Classification report values are rounded to two decimal places in the source output.*

## Confusion Matrices

### Logistic Regression

```text
[[916, 117],
 [159, 215]]
```

| | Predicted: No Churn | Predicted: Churn |
|---|---:|---:|
| Actual: No Churn | 916 | 117 |
| Actual: Churn | 159 | 215 |

The model correctly identified 215 churn cases but missed 159 actual churners.

### Decision Tree

```text
[[838, 195],
 [201, 173]]
```

| | Predicted: No Churn | Predicted: Churn |
|---|---:|---:|
| Actual: No Churn | 838 | 195 |
| Actual: Churn | 201 | 173 |

The model correctly identified 173 churn cases but missed 201 actual churners.

## Which Metric Is Most Useful?

**Recall is particularly important for customer churn prediction.**

The business objective is to identify customers who are likely to leave so that the company can take retention measures. A false negative means an actual churner is missed, potentially resulting in a lost customer.

The Logistic Regression model achieved a churn recall of **57%**, compared with **46%** for the Decision Tree.

However, recall should not be considered in isolation. Precision also matters because retention campaigns have costs. The F1-score helps balance these two metrics, while accuracy provides an overall measure of correct predictions.

The most appropriate metric ultimately depends on the relative costs of missed churners and unnecessary retention interventions.

## Model Comparison and Findings

- Logistic Regression achieved higher overall accuracy than the Decision Tree.
- Logistic Regression also achieved better churn precision, recall, and F1-score.
- The Decision Tree missed more actual churners, with 201 false negatives compared with 159 for Logistic Regression.
- Both models still missed a substantial proportion of actual churners, indicating room for improvement.
- Class-specific metrics provide more useful information than accuracy alone when evaluating churn prediction.

## Technologies Used

- **Python 3**
- **Pandas**
- **NumPy**
- **Scikit-learn**
- **Matplotlib**
- **Seaborn**
- **Jupyter Notebook**

## Key Learnings

- Accuracy alone may hide weaknesses in identifying a specific class.
- Precision measures the reliability of positive predictions.
- Recall measures how many actual positive cases are detected.
- F1-score balances precision and recall.
- Confusion matrices reveal false positives and false negatives.
- Metric selection should reflect the business objective and the cost of prediction errors.

## Conclusion

Day 12 evaluated the Logistic Regression and Decision Tree models developed on Day 11. Logistic Regression performed better across the reported evaluation metrics, including churn recall and F1-score.

The exercise demonstrated why selecting appropriate evaluation metrics is essential for classification problems, particularly when the objective is to identify customers at risk of leaving a service.

---

**Internship Task:** Day 12 — Classification Model Evaluation  
**Status:** Completed
