# used-car-price-prediction
# 🚗 Used Car Price Prediction

This project predicts the price of used cars using a large and complex dataset with high-cardinality categorical features and various numeric attributes.

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
  - Achieved **~94% R²** using Gradient Boosting on test data.  
  - MAE was ~4,000 units — strong performance considering dataset scale and complexity.

---
## 🚀 Tools/Libraries Used:

- Python, Pandas, NumPy
- Scikit-learn (modeling, scaling, encoding)
- Seaborn & Matplotlib (EDA)
- VS Code
