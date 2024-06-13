# PRODIGY_ML_01_HOUSE PRICE PREDICTION USING LINEAR REGRESSION

![image](https://github.com/lekshmiij/PRODIGY_ML_01/assets/141242851/a124ca85-a004-4d2b-b7af-ee17c39626e8)


Comprehensive Overview of the Process
### 1. Loading the Dataset
The dataset is loaded using pandas from a CSV file located at 'C:/Users/lekshmi/Downloads/HousePricePrediction.xlsx - Sheet1.csv'.
### 2. Initial Exploration and Preprocessing
The dataset initially has 2919 rows and 13 columns.
Duplicate rows are checked and dropped, ensuring there are no duplicates.
The Id column is removed as it is unnecessary for the analysis.
Columns are checked for null values. The SalePrice column's null values are imputed using the mean strategy, and the remaining null values are filled with zero.
### 3. Descriptive Statistics
Descriptive statistics of the dataset are obtained to understand the data distribution and central tendency measures.
### 4. Outlier Detection and Handling
A boxplot is used to detect outliers in the LotArea column.
Outliers are handled using the Interquartile Range (IQR) method. Data points outside the range defined by 1.5 * IQR are removed.
### 5. Handling Categorical Data
Columns containing categorical data are identified and converted to string type to prepare for encoding.
OneHotEncoding is applied to the categorical columns to convert them into numerical format suitable for machine learning algorithms.
### 6. Feature Scaling
As different columns have different scales, feature scaling is performed using the MinMaxScaler to bring all values into a standard scale.
### 7. Data Splitting
The dataset is split into training and testing sets using an 80-20 split, with a random state of 100 to ensure reproducibility.
### 8. Linear Regression Model
A Linear Regression model is imported and trained on the training data.
Predictions are made on the test data, and the first few predicted values are compared with the actual values.
### 9. Model Evaluation 
The Mean Absolute Error (MAE) is calculated to evaluate the performance of the Linear Regression model.
### 10. Model Regularization
To improve the model's performance, regularization techniques are applied using Lasso and Ridge regression:
Lasso Regression: Applied with an alpha of 20, a maximum of 100 iterations, and a tolerance of 0.1.
Ridge Regression: Applied with an alpha of 50, a maximum of 100 iterations, and a tolerance of 0.1.
The MAE is recalculated for both regularized models to compare performance improvements.
