# Second Hand Car Price Prediction

## Table of Contents
1. [Overview](#overview)
2. [Installation](#installation)
3. [Dataset](#dataset)
4. [Exploratory Data Analysis](#exploratory-data-analysis)
5. [Feature Engineering](#feature-engineering)
6. [Modeling](#modeling)
7. [Results](#results)
8. [Accuracy Comparison](#accuracy-comparison)
9. [Conclusion](#conclusion)
10. [License](#license)

---

## Overview

This project aims to predict the price of second-hand cars based on various features such as Brand, Model, Year, Fuel Type, Transmission, and other technical specifications. The dataset is sourced from Kaggle and includes 100 entries with 13 columns.

---
## Installation

To get started, clone the repository and install the necessary dependencies:

bash
git clone https://github.com/your-username/second-hand-car-price-prediction.git
cd second-hand-car-price-prediction
pip install -r requirements.txt
---
## Dataset
The dataset used in this project is from Kaggle: Second Hand Car Price Prediction Dataset.

The dataset contains the following columns:

Car_ID: Unique ID for each car
Brand: The brand of the car
Model: The model of the car
Year: The manufacturing year
Kilometers_Driven: Distance driven in kilometers
Fuel_Type: Type of fuel used (e.g., Petrol, Diesel)
Transmission: Transmission type (e.g., Automatic, Manual)
Owner_Type: Owner type (e.g., First, Second, Third)
Mileage: Fuel efficiency of the car
Engine: Engine capacity
Power: Power output of the car
Seats: Number of seats
Price: The price of the car (target variable)
---
##  Exploratory Data Analysis
We performed several exploratory data analysis steps:

Handling Missing Values: No missing data was found in the dataset.
Duplicate Rows: There were no duplicate rows in the data.
Outlier Analysis: Outliers were identified in features such as Engine, Power, and Kilometers Driven.
Correlation Analysis: A correlation heatmap was plotted to identify relationships between numerical features and the target variable (Price).
Visualizations: Various plots such as histograms, count plots, and scatter plots were used to understand the distribution and relationships of the data.
---
## Feature Engineering
We applied the following feature engineering steps:

Encoding Categorical Features: Categorical variables like Brand, Fuel_Type, Transmission, and Model were encoded using Label Encoding or Ordinal Encoding.
Scaling Numerical Features: Features such as Year, Kilometers_Driven, Mileage, Engine, Power, and Seats were standardized using StandardScaler for model performance.
---
## Modeling
Several machine learning models were trained to predict the car prices:

  Linear Regression
  Random Forest Regressor
  Decision Tree Regressor
  XGBoost Regressor

Each model was evaluated using root mean squared error (RMSE) and R-squared (R²) metrics.
---
## Results
After training the models, we evaluated their performance on the test set. The results were as follows:

- Linear Regression
RMSE: 467,450.77
R²: 0.7328
- Random Forest Regressor
RMSE: 371,443.89
R²: 0.8313
- Decision Tree Regressor
RMSE: 454,285.15
R²: 0.7477
- XGBoost Regressor
RMSE: 300,689.84
R²: 0.8894
---
## Accuracy Comparison
- Model	Root Mean Squared Error (RMSE)	R² (R-squared)
- Linear Regression	467,450.77	0.7328
- Random Forest Regressor	371,443.89	0.8313
- Decision Tree Regressor	454,285.15	0.7477
- XGBoost Regressor	300,689.84	0.8894
---
## Conclusion
The XGBoost Regressor performed the best in predicting second-hand car prices, with the lowest RMSE and highest R² score. The project demonstrated how feature engineering, data preprocessing, and model selection can significantly improve the accuracy of predictions.
---
## License
This project is licensed under the MIT License - see the LICENSE file for details.

---

