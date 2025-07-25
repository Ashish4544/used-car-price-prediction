# used-car-price-prediction
# 🚗 Used Car Price Prediction

This project predicts the price of used cars using a large and complex dataset with high-cardinality categorical features and various numeric attributes.
Dataset Source: (Kaggle used car listings)
---

## 📌 Overview

- **Categorical Handling**:  
  - High-cardinality features like `brand` and `model` were handled using **target encoding**.  
  - Features like `fuel_type` and `transmission` were **label encoded**.  
  - Complex columns like `exterior color` were grouped and one-hot encoded to reduce noise.

- **Feature Engineering**:  
  - Extracted `car_age`, `horsepower`, and interaction features like `age × mileage`.  
  - Created binary flags like `has_accident` and `clean_title`.

- **Modeling & Tuning**:  
  - Built and compared **Linear Regression**, **Random Forest**, and **Gradient Boosting**.  
  - Applied **GridSearchCV** to tune hyperparameters of ensemble models.

- **Performance**:  
  - Achieved **~94% R²** using Random forest with MAE of 4000 on test data.  
  - MAE was ~4,000 units — strong performance considering dataset scale and complexity.
 
---

## 🔍 Challenges & How I Overcame Them

### ⚠️ 1. Complex and Messy Data
- Columns had inconsistent formats (e.g., `milage` with commas and "mi.", `price` with `$`).
- Missing values in horsepower and categorical columns.

✅ **Solution**: Cleaned all numerical columns, filled missing horsepower using **brand-wise median**, and dropped or simplified low-impact categorical features.

---

### 🔁 2. High Cardinality Categorical Features
- `model` had nearly **1900 unique values**.
- `brand` also had many distinct entries.

✅ **Solution**:  
- Used **target encoding** for `brand` and `model` to reduce dimensionality without losing predictive power.

---

---
## 🚀 Tools/Libraries Used:

- Python, Pandas, NumPy
- Scikit-learn (modeling, scaling, encoding)
- Seaborn & Matplotlib (EDA)
- VS Code
