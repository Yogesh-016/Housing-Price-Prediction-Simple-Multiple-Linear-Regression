# 🏠 Housing Price Prediction — Simple & Multiple Linear Regression

A regression analysis project that predicts house prices using both **Simple Linear Regression** (area vs price) and **Multiple Linear Regression** (12 features), built to understand how individual and combined features influence housing prices.

## 📌 Overview

This project implements and compares two linear regression approaches on a housing dataset of 545 properties:

- **Simple Linear Regression** — predicts price using `area` alone
- **Multiple Linear Regression** — predicts price using all available features (area, bedrooms, bathrooms, stories, amenities, furnishing status, etc.)

The goal is to understand how model complexity affects predictive performance and how to interpret regression coefficients in a real-world context.

## 📊 Dataset

- **Source:** Housing.csv (545 rows, 13 columns)
- **Target variable:** `price`
- **Features:** `area`, `bedrooms`, `bathrooms`, `stories`, `mainroad`, `guestroom`, `basement`, `hotwaterheating`, `airconditioning`, `parking`, `prefarea`, `furnishingstatus`

## 🛠️ Tech Stack

- **Python**
- **Pandas** — data preprocessing
- **Scikit-learn** — model building & evaluation
- **Matplotlib** — visualization

## ⚙️ Methodology

1. **Data Preprocessing** — encoded binary categorical columns (`yes`/`no` → `1`/`0`) and one-hot encoded `furnishingstatus`
2. **Train-Test Split** — 80/20 split with `random_state=42`
3. **Model Training** — fit both simple and multiple `LinearRegression` models using `sklearn.linear_model`
4. **Evaluation** — assessed using MAE, MSE, and R²
5. **Visualization** — plotted the regression line (simple model) and actual vs predicted price (multiple model)

## 📈 Results

| Model | MAE | MSE | R² |
|---|---|---|---|
| Simple Linear Regression (area only) | ₹14,74,748 | 3.68T | 0.273 |
| Multiple Linear Regression (all features) | ₹9,70,043 | 1.75T | 0.653 |

**Key insight:** Adding more relevant features nearly doubles the R² score (0.27 → 0.65), showing that area alone explains only a fraction of price variation. `bathrooms`, `airconditioning`, and `hotwaterheating` emerged as the strongest positive price drivers.

## 📷 Visualizations

- `simple_regression_plot.png` — Price vs Area with fitted regression line
- `multiple_regression_plot.png` — Actual vs Predicted price scatter plot

## 🚀 How to Run

```bash
pip install pandas scikit-learn matplotlib
python linear_regression_housing.py
```

## 🔑 Key Learnings

- How to preprocess categorical data for regression models
- Difference in explanatory power between simple and multiple linear regression
- How to interpret regression coefficients (holding other variables constant)
- Model evaluation using MAE, MSE, and R²

## 📁 Repository Structure

```
├── Housing.csv
├── linear_regression_housing.py
├── simple_regression_plot.png
├── multiple_regression_plot.png
└── README.md
```

## 👤 Author

**Yogesh S**
[GitHub](https://github.com/Yogesh-016) • [LinkedIn](https://www.linkedin.com/in/yogesh-s-617334378)
