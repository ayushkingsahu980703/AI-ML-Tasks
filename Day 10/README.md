California Housing Price Prediction
A beginner machine learning project using Linear Regression to predict California housing prices.
Project Overview
This notebook follows a basic machine learning workflow: data inspection, exploratory data analysis (EDA), feature engineering, preprocessing, model training, and evaluation.
Dataset
- Dataset: California Housing Prices
- Source: Kaggle — California Housing Prices
- Target: median_house_value
The notebook loads housing.csv using kagglehub.
Tools and Libraries
- Python
- Pandas and NumPy
- Matplotlib and Seaborn
- Scikit-learn
- KaggleHub
Workflow
1. Load and inspect the dataset.
2. Check missing values and remove rows with missing data.
3. Encode ocean_proximity using One-Hot Encoding.
4. Explore the target distribution, feature correlations, and geographic patterns.
5. Create rooms_per_house, bedrooms_per_room, and population_per_household features.
6. Split the data into training and test sets.
7. Impute missing feature values and standardize the features.
8. Train a Linear Regression model.
9. Evaluate predictions using MAE, RMSE, and R².
10. Compare actual and predicted prices.
Evaluation
The notebook reports these metrics after it is run:
- MAE (Mean Absolute Error): average absolute prediction error.
- RMSE (Root Mean Squared Error): penalizes larger prediction errors more strongly.
- R² Score: indicates how much variation in the target is explained by the model.
Run the notebook to generate the actual metric values; results are not listed here because they depend on execution.
How to Run
1. Clone or download this repository.
2. Install the required libraries:
   pip install kagglehub pandas numpy matplotlib seaborn scikit-learn jupyter
3. Open Day_10_Cleaned.ipynb in Jupyter Notebook or JupyterLab.
4. Run the cells from top to bottom. Kaggle access or dataset download setup may be required.
Limitations
- Linear Regression may not capture complex, non-linear relationships in housing data.
- The dataset's median_house_value target is capped at $500,001, limiting what the model can learn about higher-value properties.
- Model performance should be assessed using the test metrics, not the plots alone.
Project Goal
This project is a learning exercise to practice the end-to-end workflow of a supervised machine learning regression task.
