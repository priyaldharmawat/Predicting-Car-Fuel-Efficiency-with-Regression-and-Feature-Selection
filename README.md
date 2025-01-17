# Predicting-Car-Fuel-Efficiency-with-Regression-and-Feature-Selection

# Car Dataset Analysis and Linear Regression Model

This project involves cleaning and analyzing a car dataset and building a Linear Regression model to predict the `MPG` (Miles Per Gallon) of cars based on other features. Below is an explanation of the steps performed in this analysis.

## Table of Contents
- [Project Overview](#project-overview)
- [Dataset Information](#dataset-information)
- [Steps Performed](#steps-performed)
  - [Data Cleaning](#data-cleaning)
  - [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
  - [Outlier Detection and Handling](#outlier-detection-and-handling)
  - [Linear Regression Model](#linear-regression-model)
  - [Feature Selection](#feature-selection)
- [Evaluation Metrics](#evaluation-metrics)
- [Results](#results)
- [How to Run the Project](#how-to-run-the-project)

## Project Overview
The primary goal of this project is to preprocess a car dataset, explore it for insights, and build a predictive model using Linear Regression to estimate `MPG` based on other attributes.

## Dataset Information
The dataset is loaded from a CSV file named `car.csv`. Missing values are represented by `?`. The dataset contains numeric and categorical columns, and the target variable is `MPG`.

## Steps Performed

### Data Cleaning
1. **Missing Values**: 
   - Identified missing values in the `Horsepower` column and imputed them with the median value.
   - Rechecked the dataset to ensure no missing values remained.

2. **Duplicate Rows**: 
   - Checked and removed any duplicate rows.

### Exploratory Data Analysis (EDA)
1. Visualized the distribution of numeric columns using boxplots to identify outliers.
2. Generated descriptive statistics for all numeric features to understand the data better.

### Outlier Detection and Handling
1. **Outlier Detection**:
   - Calculated the Interquartile Range (IQR) for numeric columns to identify outliers.

2. **Outlier Handling**:
   - Capped and floored outliers to the nearest non-outlier values.
   - Rechecked the dataset to ensure effective outlier handling.

### Linear Regression Model
1. **Splitting Data**:
   - Separated the dataset into features (`X`) and target variable (`y`).
   - Split the dataset into training (80%) and testing (20%) sets.

2. **Model Building**:
   - Built a Linear Regression model using the training data.

3. **Model Evaluation**:
   - Evaluated the model using metrics such as Mean Squared Error (MSE), Root Mean Squared Error (RMSE), and R-squared (R²).

### Feature Selection
1. **Sequential Forward Selection (SFS)**:
   - Used SFS to select the best subset of features for predicting `MPG`.
   - Built a new Linear Regression model using the selected features and compared its performance with the original model.

## Evaluation Metrics
The following metrics were used to evaluate the model:
- **Mean Squared Error (MSE)**: Measures the average squared difference between actual and predicted values.
- **Root Mean Squared Error (RMSE)**: Square root of MSE, representing prediction error in the same unit as the target variable.
- **R-squared (R²)**: Represents the proportion of variance in the target variable explained by the model.

## Results
### Initial Model:
- MSE: _value_
- RMSE: _value_
- R²: _value_

### Model with Selected Features:
- MSE: _value_
- RMSE: _value_
- R²: _value_

Feature selection improved the model performance slightly by reducing error and increasing R².

## How to Run the Project
1. Clone this repository:
   ```bash
   git clone <repository_url>
   ```
2. Install the required Python libraries:
   ```bash
   pip install pandas numpy scikit-learn matplotlib seaborn mlxtend
   ```
3. Place the `car.csv` file in the project directory.
4. Run the script:
   ```bash
   python car_analysis.py
   ```
5. Check the outputs and visualizations for insights.

## Future Work
- Include polynomial or other non-linear models to improve predictions.
- Use additional feature engineering techniques.
- Experiment with more advanced feature selection methods.
