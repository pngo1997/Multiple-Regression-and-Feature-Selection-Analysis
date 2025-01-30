# 🏗️ Multiple Regression and Feature Selection Analysis  

## 📜 Overview  
This project explores **multiple linear regression, feature selection, Ridge & Lasso regression, and Stochastic Gradient Descent (SGD) regression**. The dataset is split into **80% training and 20% testing**, and different regression techniques are applied to predict a target variable. The analysis includes **cross-validation, feature selection, and model optimization** to improve regression performance.  

## 🎯 Problem Explanation  
The project aims to:  
1. **Perform standard multiple linear regression** and evaluate its effectiveness.  
2. **Select the most informative features** using `SelectPercentile`.  
3. **Optimize Ridge & Lasso Regression** by tuning the **alpha parameter**.  
4. **Train a Stochastic Gradient Descent (SGD) Regressor** with grid search for hyperparameter selection.  
5. **Compare models using RMSE, MAE, and cross-validation performance**.  

## 🛠️ Implementation Details  
### **1. Data Preprocessing**  
- **Missing values handled** using mean imputation.  
- **Basic statistics computed** (mean, std dev, min, max).  
- **Target variable extracted**, and dataset is split (80% train, 20% test).  

### **2. Multiple Linear Regression**  
- Standard **multiple linear regression** applied.  
- **RMSE computed** on training data.  
- **Regression coefficients plotted** to visualize feature importance.  
- **10-fold cross-validation RMSE** compared to training RMSE.  

### **3. Feature Selection with Regression**  
- `SelectPercentile` with `f_regression` used to identify top features.  
- **K-fold cross-validation (k=5)** determines the optimal percentage of features.  
- **Mean Absolute Error (MAE) plotted** vs. feature selection percentage.  

### **4. Ridge & Lasso Regression with Alpha Optimization**  
- A function is implemented to:  
  - Accept **data, target variable, parameter range (alpha), and model type**.  
  - Perform **K-fold cross-validation (k=5)**.  
  - **Plot error values** vs. alpha for Ridge & Lasso regression.  
  - Train on the best alpha and **evaluate on test data**.  
- **Bias-variance trade-off analyzed**.  

### **5. Stochastic Gradient Descent Regression**  
- **Features standardized** using `StandardScaler`.  
- **GridSearchCV applied** to compare penalty parameters (`l2`, `l1`) and different alpha values (0.0001 to 10).  
- **Elastic Net model selection** performed to find the best `l1_ratio`.  

## 🚀 Technologies Used  
- **Python** (for regression modeling and evaluation).  
- **Pandas & NumPy** (for data preprocessing and statistical computations).  
- **Scikit-learn** (for regression models, feature selection, and cross-validation).  
- **Matplotlib & Seaborn** (for data visualization).  
