# **GadgetValuator - Smart Pricing Model for Consumer Electronics**

## **Overview**
The **GadgetValuator** project is a comprehensive, data-driven solution for predicting optimal prices for various consumer electronics, including **laptops, smartphones, and smartwatches**. By analyzing device specifications, brand reputation, and market trends, this model helps buyers and sellers make informed pricing decisions.

The workflow includes:
- **Data preprocessing**
- **Exploratory analysis**
- **Model training and evaluation**

This project is fully documented, covering the challenges faced, methodologies adopted, and the rationale behind selecting final models for each device category.

---

## **Project Analysis**

### **Laptop Pricing Model**
- **Objective**: Predict laptop prices with high accuracy.
- **Best Model**: **CatBoost Regressor**
- **Performance**: 
  - **R² Score**: **0.87**

#### **Libraries Used**
- `Pandas`, `NumPy`: Data manipulation and analysis.
- `Matplotlib`, `Seaborn`: Data visualization.
- `Scikit-learn`: Preprocessing, feature scaling, and model evaluation.
- `CatBoost Regressor`: Final model due to its robust performance.

#### **Key Steps**
1. **Feature Scaling**: Applied `StandardScaler` for numerical features.
2. **One-Hot Encoding**: Categorical variables such as brand, operating system, and GPU type were encoded.
3. **Data Cleaning**: 
   - Missing values handled with **median imputation**.
   - Outliers removed using the **Interquartile Range (IQR)** method.

#### **Models Tested**
- Linear Regression, Ridge, Lasso, Polynomial Features, SVR, KNeighborsRegressor, DecisionTreeRegressor, RandomForestRegressor, XGBRegressor.
- **Final Selection**: CatBoost Regressor.

---

### **Smartphone Pricing Model**
- **Objective**: Develop a reliable pricing model for smartphones.
- **Best Model**: **XGBoost Regressor**
- **Performance**: 
  - **R² Score**: **0.90**

#### **Libraries Used**
- `Pandas`, `NumPy`, `Matplotlib`, `Seaborn`, `Scikit-learn`, and `XGBoost`.

#### **Key Steps**
1. **Feature Scaling**: Used `StandardScaler` for numerical features like battery capacity and screen size.
2. **One-Hot Encoding**: Categorical variables (e.g., brand, network type, OS) encoded for compatibility.
3. **Data Cleaning**: Missing values addressed with appropriate imputation techniques.

#### **Models Tested**
- Linear Regression, Ridge, Lasso, Polynomial Features, SVR, KNeighborsRegressor, DecisionTreeRegressor, RandomForestRegressor, XGBRegressor.
- **Final Selection**: XGBoost Regressor.

---

### **Smartwatch Pricing Model**
- **Objective**: Predict smartwatch prices accurately, focusing on features like battery life and strap type.
- **Best Model**: **ElasticNet Regression**
- **Performance**: 
  - **R² Score**: **0.87**

#### **Libraries Used**
- `Pandas`, `NumPy`, `Matplotlib`, `Seaborn`, `Scikit-learn`.

#### **Key Steps**
1. **Feature Scaling**: Applied `StandardScaler` to key features like battery life and weight.
2. **One-Hot Encoding**: Encoded categorical variables such as brand, strap type, and connectivity options.
3. **Data Cleaning**: Missing values imputed as necessary.

#### **Models Tested**
- Linear Regression, Ridge, Lasso, Polynomial Features, SVR, KNeighborsRegressor, DecisionTreeRegressor, RandomForestRegressor, XGBRegressor.
- **Final Selection**: ElasticNet Regression.

---

## **Results Summary**

| **Device Type** | **Best Model**            | **R² Score** |
|------------------|---------------------------|--------------|
| Laptops          | CatBoost Regressor       | **0.87**     |
| Smartphones      | XGBoost Regressor        | **0.90**     |
| Smartwatches     | ElasticNet Regression    | **0.87**     |

---
