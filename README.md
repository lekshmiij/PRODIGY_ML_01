# PRODIGY_ML_01_HOUSE PRICE PREDICTION USING LINEAR REGRESSION

![image](https://github.com/lekshmiij/PRODIGY_ML_01/assets/141242851/a124ca85-a004-4d2b-b7af-ee17c39626e8)


Comprehensive Overview of the Process
Overview of the Process
### Importing Libraries:
Essential libraries are imported, including pandas and numpy for data manipulation, scikit-learn for model training, preprocessing, and evaluation, and SelectFromModel for feature selection.
### Loading the Dataset:
The dataset is loaded from a CSV file into a pandas DataFrame.
### Data Preprocessing:
Removing Duplicates: Duplicate rows are dropped to ensure the dataset contains unique entries.
Dropping Unnecessary Columns: The 'Id' column is dropped as it does not contribute to the prediction.
### Handling Missing Values:
Numerical Columns: Missing values in numerical columns are filled with the median of each column.
Categorical Columns: Missing values in categorical columns are filled with the mode (most frequent value) of each column.
### Feature Engineering:
A new feature 'TotalBathrooms' is created by summing up 'FullBath' and 'HalfBath' columns to capture the total number of bathrooms in the house.
### Splitting Data into Features and Target Variable:
Features (X): The features selected are 'GrLivArea' (above-ground living area square footage), 'BedroomAbvGr' (number of bedrooms above ground), and the newly created 'TotalBathrooms'.
Target Variable (y): The target variable is 'SalePrice'.
### Splitting Data into Training and Test Sets:
The data is split into training (80%) and test (20%) sets using train_test_split with a random state for reproducibility.
### Standardizing Features:
The features are standardized using StandardScaler to ensure they have a mean of 0 and a standard deviation of 1, which helps improve model performance.
### Adding Polynomial Features:
Polynomial features of degree 2 are added to capture non-linear relationships between the features.
### Feature Selection using Lasso Regularization:
Lasso Regression: Lasso regularization is applied to select the most important features by setting the regularization parameter alpha to 0.001. This step helps in reducing overfitting and improving model generalization.
SelectFromModel: The SelectFromModel class is used to select the features deemed important by the Lasso model.
### Training the Linear Regression Model:
A LinearRegression model is trained using the selected features from the training set.
### Making Predictions:
Predictions are made on the test set using the trained Linear Regression model.
### Evaluating the Model:
The performance of the model is evaluated using the following metrics:
Mean Squared Error (MSE): Measures the average squared difference between actual and predicted values.
Root Mean Squared Error (RMSE): The square root of MSE, providing an error metric in the same units as the target variable.
R-squared (R2) Score: Indicates the proportion of variance in the target variable that can be explained by the model. An R2 score closer to 1 indicates a better fit.
