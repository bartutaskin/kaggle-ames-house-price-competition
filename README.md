# House Price Prediction using XGBoost

## Overview
This project aims to predict the sale prices of houses in Ames, Iowa, using machine learning techniques. The dataset contains various features related to the houses such as the number of rooms, the condition of the house, and the neighborhood. The goal is to build a regression model that accurately predicts the sale price based on these features.

The model is built using XGBoost, a powerful gradient boosting algorithm, with hyperparameter tuning done using GridSearchCV to improve the model's performance.


## Data
The project uses the **Ames Housing Dataset**, which is widely used in Kaggle competitions. The dataset consists of both numerical and categorical features describing properties in Ames, Iowa. It includes the target variable `SalePrice`, which represents the sale price of each property.

### Data Files:
- **train.csv**: Contains the training data, including both the features and the target variable (`SalePrice`).
- **test.csv**: Contains the test data, used for generating predictions. The target variable `SalePrice` is not included.

## Approach

### 1. Data Preprocessing
The preprocessing steps include:
- Handling missing values by imputing them with suitable strategies such as filling with the mode for categorical variables and filling with the mean for numerical variables.
- Feature engineering to create new features that could improve model performance (e.g., total square footage, number of bathrooms).
- Encoding categorical features using ordinal encoding for features with a specific order (e.g., quality levels) and one-hot encoding for other categorical variables.
- Handling outliers by removing extreme values that could negatively impact the model.

### 2. Model Training
The model is trained using the `XGBoost` algorithm, which is a gradient boosting method known for its high performance in structured data tasks. Hyperparameter tuning is done using `GridSearchCV` with 5-fold cross-validation to find the best set of hyperparameters for the model.

### 3. Evaluation
The model's performance is evaluated using **Mean Absolute Error (MAE)** and **R² Score** on the validation set. The final model is used to predict house prices on the test dataset.

### 4. Submission
The model’s predictions are saved in a `submission.csv` file, which includes the predicted sale prices for each property in the test dataset. This file is ready for submission to Kaggle or similar platforms.

## Result
The final model achieved a **Mean Absolute Error (MAE)** of **0.13275**, meaning that the average error in predicting house prices is approximately 13.3% of the sale price.




