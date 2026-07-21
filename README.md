# 🛒 Retail Sales Prediction

## 📌 Project Overview

This project aims to predict monthly retail sales using machine learning techniques. The workflow covers the complete data science pipeline, including data cleaning, exploratory data analysis (EDA), feature engineering, model training, evaluation, and model comparison.

The objective is not only to build an accurate predictive model but also to understand which features contribute most to retail sales.

---

## 🎯 Business Problem

Retail businesses need to estimate future sales to improve inventory planning and warehouse management.

This project investigates whether warehouse movement and product-related information can be used to predict retail sales accurately.

---

## 📂 Dataset

**Dataset:** Montgomery County Warehouse and Retail Sales

The dataset contains monthly warehouse and retail sales information, including:

- Retail Sales
- Retail Transfers
- Warehouse Sales
- Item Type
- Supplier Information
- Date (Year & Month)

---

## 🛠 Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Joblib
- Jupyter Notebook

---

## 📊 Project Workflow

### 1. Data Cleaning

- Removed unnecessary columns
- Checked missing values
- Checked duplicates
- Renamed columns
- Corrected data types

---

### 2. Exploratory Data Analysis (EDA)

Performed exploratory analysis to understand:

- Monthly sales trends
- Distribution of retail sales
- Supplier contribution
- Item type distribution
- Feature correlations

---

### 3. Feature Engineering

Drop column item_description & item_code because it's high-cardinality text, it will be difficult to encode,we can use item_type for identifier

Created several new features, including:

- Supplier Frequency
- Total Movement (Retail Transfers + Warehouse Sales)

Categorical variables were encoded using one-hot encoding.

---

## 🤖 Machine Learning Models

Two regression models were trained:

### Linear Regression

Three experiments:

- Model A — All features
- Model B — Without `retail_transfers`
- Model C — Without `retail_transfers` and `total_movement`

### Random Forest Regressor

Three experiments:

- Model A — All features
- Model B — Without `retail_transfers`
- Model C — Without `retail_transfers` and `total_movement`

---

## 📈 Model Evaluation

Models were evaluated using:

- R² Score
- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)

Evaluation plots include:

- Actual vs Predicted
- Residual Plot
- Error Distribution
- Random Forest Feature Importance

---

## 🔍 Key Findings

- Linear Regression achieved performance comparable to Random Forest.
- Retail movement features contributed significantly to prediction performance.
- Removing both `retail_transfers` and `total_movement` caused a substantial decrease in model performance.
- Feature engineering played an important role in improving prediction accuracy.

---

## 💾 Model Saving

The final trained model was saved using **Joblib** for future deployment and prediction.

---

## 🚀 Future Improvements

Possible future improvements include:

- Hyperparameter tuning
- Time-series feature engineering
- XGBoost or LightGBM
- Model deployment using Streamlit
- Interactive dashboard using Tableau or Power BI

---

## 📁 Project Structure

```
Retail-Sales-Prediction/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── notebooks/
│   ├── 01_data_cleaning.ipynb
│   ├── 02_eda.ipynb
│   ├── 03_feature_engineering.ipynb
│   └── 04_modeling.ipynb
│
├── models/
│   └── best_model.pkl
│
├── requirements.txt
└── README.md
```

---

## 👨‍💻 Author

Muhammad Rafly Husen Batubara, as rafsen

Civil Engineering Student | Aspiring Data Scientist
