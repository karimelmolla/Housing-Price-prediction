# USA Housing Price Prediction

## 📌 Project Overview
This project implements a machine learning pipeline to predict housing prices in the USA based on various demographic and property features. The goal is to analyze the relationship between features like income, house age, and population with the housing price and compare the performance of **Linear Regression** versus **Random Forest Regression**.

## 📂 Dataset
The project utilizes the `USA_Housing.csv` dataset, which includes the following features:
* **Avg. Area Income**: Average income of residents in the city.
* **Avg. Area House Age**: Average age of houses in the same city.
* **Avg. Area Number of Rooms**: Average number of rooms for houses in the same city.
* **Avg. Area Number of Bedrooms**: Average number of bedrooms for houses in the same city.
* **Area Population**: The population of the city where the house is located.
* **Price**: The target variable (Housing Price).
* **Address**: The address of the house (used for initial exploration but dropped for model training).

## 🛠️ Libraries & Prerequisites
The project is implemented in Python and requires the following libraries:
* **Pandas**: For data manipulation and loading.
* **NumPy**: For numerical calculations.
* **Matplotlib**: For plotting distributions and visualizations.
* **Scikit-Learn**: For model training, scaling, and evaluation.

To install the necessary dependencies, run:
```bash
pip install pandas numpy matplotlib scikit-learn

## Methodology

### Data Loading & Exploration
- Load the dataset using **Pandas**  
- Perform **Exploratory Data Analysis (EDA)** to check data structure, null values, and visualize distributions  
- Generate correlation matrices to analyze relationships between features  

### Data Preprocessing
- **Label Encoding:** Initially applied to the `Address` column (ultimately dropped)  
- **Feature Selection:** Separate target variable (`Price`) from irrelevant features (`Address`)  
- **Data Splitting:** Train-test split  
- **Scaling:** `StandardScaler` used to normalize features  

### Model Training
- **Linear Regression:** Models the linear relationship between features and target  
- **Random Forest Regressor:** Ensemble method building multiple decision trees  

---

## Results

| Model                  | MSE   | RMSE  | R² Score |
|------------------------|-------|-------|----------|
| Linear Regression      | 0.08  | 0.28  | 0.92     |
| Random Forest Regressor| 0.11  | 0.34  | 0.88     |

---

## Conclusion
The **Linear Regression** model outperformed the Random Forest Regressor for this dataset, achieving:

- **Higher R² Score** (~0.92 vs 0.88)  
- **Lower MSE and RMSE**  

This indicates that Linear Regression explains a greater proportion of the variance in housing prices and makes smaller prediction errors.


