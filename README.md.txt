# USA Housing Price Prediction using Linear Regression

## Project Overview

This project involves building and evaluating a Linear Regression model to predict housing prices in the USA based on various features. The analysis covers data loading, exploratory data analysis (EDA), model training, and a detailed evaluation of the model's performance.

## Dataset

The dataset used for this analysis is `USA_Housing.csv`. It contains the following features:

*   `Avg. Area Income`: Average income of residents in the city where the house is located.
*   `Avg. Area House Age`: Average age of houses in the city.
*   `Avg. Area Number of Rooms`: Average number of rooms for houses in the same city.
*   `Avg. Area Number of Bedrooms`: Average number of bedrooms for houses in the same city.
*   `Area Population`: Population of the city.
*   `Price`: Price of the house (Target Variable).
*   `Address`: Address of the house (excluded from the model).

## Analysis Steps

1.  **Data Loading and Initial Inspection**: Loaded the dataset and performed initial checks using `head()`, `info()`, `shape()`, `describe()`, `isnull().sum()`, and `duplicated().sum()`.
2.  **Feature Engineering and Preprocessing**: Separated features (X) from the target variable (Y, Price). The 'Address' column was dropped. The data was then split into training and testing sets.
3.  **Model Training**: A `LinearRegression` model from `sklearn.linear_model` was trained on the preprocessed training data.
4.  **Model Evaluation**: The model's performance was assessed using:
    *   **R-squared (Coefficient of Determination)**: Measures the proportion of the variance in the dependent variable that is predictable from the independent variables.
    *   **Mean Absolute Error (MAE)**: The average of the absolute differences between predictions and actual values.
    *   **Mean Squared Error (MSE)**: The average of the squared differences between predictions and actual values.
    *   **Root Mean Squared Error (RMSE)**: The square root of the MSE, providing an error metric in the same units as the target variable.
5.  **Visualizations**: Generated scatter plots of individual features against price with linear fits, a correlation matrix heatmap, and a plot comparing actual vs. predicted prices.

## Key Findings & Model Performance

The Linear Regression model achieved an R-squared score of approximately **0.918** on the test set, indicating that about 91.8% of the variance in house prices can be explained by the features in the model. This suggests a strong fit.

*   **R-squared**: 0.918
*   **MAE**: ~$80,879
*   **MSE**: ~10,089,009,300
*   **RMSE**: ~$100,444

While MAE and RMSE values might seem large in isolation, they are reasonable when considered against the scale of the house prices in the dataset (mean price ~$1.23 million, standard deviation ~$353,117). The model's typical prediction error (~$100k) is significantly less than the natural variation in house prices, demonstrating a highly effective predictive capability.

## How to Run the Notebook

This analysis can be run in a Python environment with the following libraries installed:

*   pandas
*   numpy
*   matplotlib
*   seaborn
*   scikit-learn

Download the `USA_Housing.csv` dataset and place it in the same directory as the Jupyter notebook. Then, simply execute the cells sequentially.