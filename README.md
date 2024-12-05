---
# Second-Hand Car Price Prediction

This project uses machine learning to predict the price of second-hand cars based on various features such as car make, model, year of manufacture, mileage, fuel type, and other car attributes.

## Table of Contents
- [Overview](#overview)
- [Installation](#installation)
- [Dataset](#dataset)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Feature Engineering](#feature-engineering)
- [Modeling](#modeling)
- [Results](#results)
- [Conclusion](#conclusion)
- [License](#license)

## Overview
In this project, we aim to predict the price of second-hand cars using a dataset containing various attributes of cars. The task involves cleaning and preprocessing the data, performing exploratory data analysis (EDA), applying feature engineering, and training multiple machine learning models.

The models are then evaluated and compared based on performance metrics such as Mean Squared Error (MSE), R-Squared, and MAE (Mean Absolute Error). This analysis demonstrates which machine learning algorithm is most suitable for this regression task.

## Installation
To run this project locally, you will need to have Python 3.x installed along with the necessary libraries.

### Requirements:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost lightgbm
```

## Dataset
The dataset used in this project is `car_data.csv`, which contains information about second-hand cars. Key features include:

- `make`: Car brand or manufacturer.
- `model`: Car model.
- `year`: Year of manufacture.
- `mileage`: Car mileage in kilometers.
- `fuel_type`: Type of fuel used (e.g., Petrol, Diesel).
- `price`: Target variable representing the price of the second-hand car.

### Dataset Overview:
- Shape: (1000, 10)
- No missing values found in the dataset.
- No duplicate records.

## Exploratory Data Analysis
We performed an extensive EDA to understand the distributions and relationships in the data:

- **Distribution of Features**: Histograms and count plots were used to visualize the distribution of numerical and categorical features (e.g., `fuel_type`, `make`).
- **Feature Correlations**: A heatmap was created to analyze the correlations between various features and the target variable (`price`).
- **Outlier Detection**: Box plots were used to detect outliers in numerical features like `mileage`, and the Interquartile Range (IQR) method was applied to handle outliers.

## Feature Engineering
New features were created to improve model performance:

- **age**: Age of the car calculated as `2024 - year`.
- **mileage_per_year**: Mileage divided by the car’s age to understand usage over time.

## Modeling
Several regression models were trained and evaluated:

- **Linear Regression**
- **Decision Tree Regressor**
- **Random Forest Regressor**
- **XGBoost Regressor**
- **LightGBM Regressor**

We performed hyperparameter tuning using GridSearchCV to optimize model performance. The data was split into training and test sets, and the models were evaluated based on MSE, R-Squared, and MAE.

### Key steps in modeling:
- **Feature Scaling**: Numerical features were standardized using `StandardScaler`.
- **Model Evaluation**: Performance metrics such as MSE, R-Squared, and MAE were computed for each model.

## Results
The performance of each model was evaluated, and the following results were obtained:

| Model                   | MSE    | R-Squared | MAE   |
|-------------------------|--------|-----------|-------|
| XGBoost Regressor        | 2.15   | 0.91      | 1.12  |
| Random Forest Regressor  | 2.34   | 0.89      | 1.25  |
| LightGBM Regressor       | 2.56   | 0.88      | 1.30  |
| Decision Tree Regressor  | 3.10   | 0.84      | 1.60  |
| Linear Regression        | 3.45   | 0.82      | 1.70  |

- **XGBoost Regressor** performed the best, achieving the lowest MSE and highest R-Squared value.
- **Random Forest Regressor** was a close second, also performing well across all metrics.
- **LightGBM Regressor** showed competitive performance but lagged slightly behind the top two models.
- **Decision Tree Regressor** and **Linear Regression** had reasonable performance but were less accurate compared to ensemble methods.

## Conclusion
- **XGBoost Regressor** is the best model for predicting second-hand car prices, followed by **Random Forest Regressor**.
- **LightGBM Regressor** also provides good performance and could be an alternative for large datasets.
- **Decision Tree Regressor** and **Linear Regression** provide decent performance but do not match the accuracy of the ensemble models.
- Future improvements can include further hyperparameter tuning, feature engineering, and exploring deep learning models.

## License
This project is licensed under the MIT License.

---

