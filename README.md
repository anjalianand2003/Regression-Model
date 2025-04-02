# Regression-Model
# 🏨 Hotel Food Spend Analysis: A Regression Approach

This project explores guest behavior in a hotel setting by modeling the relationship between **nights stayed** and **average food spend per night**. The analysis leverages **log transformations**, **correlation exploration**, and **linear regression** to interpret and predict guest spending.

## 📦 Dataset

- **Source:** `hotelsat-data.csv`
- **Observations:** Hotel guest stays
- **Key columns:**
  - `nightsStayed`: Number of nights the guest stayed
  - `avgFoodSpendPerNight`: Average food and beverage spend per night
  - `distanceTraveled`: Distance traveled to reach the hotel (in km)

---

## 🎯 Objective

- Transform and normalize skewed variables
- Examine correlations between numeric features
- Predict **food spend per night** based on **nights stayed** using linear regression
- Interpret and visualize variable relationships

---

## 🧠 Key Steps

### 1. Data Transformation

- Log-transform:
  - `distanceTraveled`
  - `nightsStayed`
  - `avgFoodSpendPerNight` (via `log1p` to handle zeros)

### 2. Correlation Analysis

- Use `corrplot` and `corrplot.mixed` to examine relationships between numerical variables

### 3. Regression Modeling

- Fit linear model:  
  `avgFoodSpendPerNight ~ nightsStayed`
- Use model to predict food spend for a 40-night guest

---

## 📈 Sample Output

```r
Predicted log(Food Spend + 1) for 40 nights: 3.25
Predicted Food Spend per Night for 40 nights: 24.8
