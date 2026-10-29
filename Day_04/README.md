# Day 4 — NumPy for Data Science

**Date:** 8 October 2026  
**Program:** AI/ML Internship

## Overview

Day 4 focused on NumPy (Numerical Python), a fundamental Python library for numerical computing. The task involved creating arrays, performing indexing and slicing, applying mathematical operations, and comparing NumPy arrays with standard Python lists.

A practical Student Marks Analysis exercise was also implemented to apply NumPy operations to numerical data.

## Learning Objectives

- Understand the importance of NumPy in AI/ML.
- Create and manipulate one-dimensional and two-dimensional arrays.
- Perform indexing and slicing on arrays.
- Apply mathematical and statistical operations.
- Understand vectorized operations and their advantages over Python lists.
- Analyze numerical data using NumPy.

## Topics Covered

### 1. NumPy Arrays

Created one-dimensional and two-dimensional arrays using `np.array()`.

```python
import numpy as np

marks = np.array([85, 72, 90, 65, 78])

data = np.array([
    [85, 72, 90],
    [65, 78, 88]
])
```

### 2. Indexing and Slicing

Practiced accessing individual elements and extracting portions of an array.

- Positive and negative indexing
- Slicing using start and end positions
- Accessing the first and last elements

### 3. Mathematical Operations

Used NumPy functions to perform numerical calculations:

- `np.sum()` — calculates the sum.
- `np.mean()` — calculates the average.
- `np.max()` — returns the maximum value.
- `np.min()` — returns the minimum value.
- `np.sqrt()` — calculates square roots.

Also practiced element-wise arithmetic operations such as addition and multiplication.

### 4. Vectorized Operations

Compared Python lists with NumPy arrays when performing mathematical operations.

```python
marks = [10, 20, 30]
print([x * 2 for x in marks])

marks_np = np.array([10, 20, 30])
print(marks_np * 2)
```

NumPy supports direct element-wise operations on arrays without requiring an explicit Python loop for each element.

## Practical Exercise: Student Marks Analysis

Used a NumPy array containing ten students' marks to perform basic statistical analysis.

**Features implemented:**

- Displayed the marks array.
- Calculated total marks.
- Calculated average marks.
- Identified the highest and lowest marks.
- Filtered marks that were above the average.

This exercise demonstrated how NumPy can simplify numerical analysis and data filtering.

## Technologies Used

- **Python 3**
- **NumPy**
- **Jupyter Notebook**

## Key Learnings

- NumPy provides efficient tools for numerical computing.
- Arrays can represent both one-dimensional and multidimensional data.
- Indexing and slicing allow selective access to array elements.
- Built-in mathematical functions simplify statistical calculations.
- Vectorized operations make numerical code more concise.
- Boolean indexing can filter values based on conditions.

## Conclusion

Day 4 introduced NumPy as a core tool for data science and machine learning. Through array manipulation, mathematical calculations, vectorized operations, and student marks analysis, the task established practical foundations for working with numerical datasets.

---

**Internship Task:** Day 4 — NumPy Fundamentals  
**Status:** Completed
