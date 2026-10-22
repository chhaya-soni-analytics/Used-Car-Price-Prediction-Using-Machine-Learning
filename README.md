# 🚗 Used Car Price Prediction Using Machine Learning

## 📌 Project Overview

The **Used Car Price Prediction** project aims to predict the selling price of a used car based on its features using Machine Learning regression algorithms.

The project includes data cleaning, feature engineering, exploratory data analysis, model training, evaluation, and model comparison to identify the best-performing regression model.

## 🎯 Business Problem

Used car prices depend on several factors, including vehicle age, kilometers driven, brand, fuel type, transmission, ownership, and rating.

The objective is to develop a regression model that predicts used car selling prices accurately.

**Target Variable:** `Price`

**Success Criteria:**
- Train R² Score ≥ 0.85
- Test R² Score ≥ 0.85

## 🛠️ Tools & Technologies

- **Python** – Data analysis and machine learning
- **Pandas & NumPy** – Data manipulation and numerical operations
- **Matplotlib & Seaborn** – Data visualization
- **Scikit-learn** – Machine learning, preprocessing, and model evaluation
- **Jupyter Notebook** – Development environment
- **Joblib** – Model saving and loading

## 📂 Project Workflow

### 1. Data Loading and Exploration
- Loaded the used car dataset using Pandas.
- Examined dataset shape, data types, missing values, duplicates, and statistical summaries.
- Analyzed numerical and categorical features.

### 2. Data Cleaning and Preprocessing
- Handled duplicate and missing records.
- Cleaned columns such as Price, Rating, Kilometers, Owner, Fuel Type, Transmission, and Insurance.
- Converted relevant columns into appropriate data types.
- Identified suspicious records and potential outliers.

### 3. Feature Engineering
Created additional features to improve model performance, including:

- `Manufacture_Year`
- `Brand`
- `Car_Model`
- `Car_Age`
- `Owner_Count`
- `RTO_State`
- `Transmission_Automatic`
- `Has_Insurance`

Applied target encoding to selected categorical features.

### 4. Exploratory Data Analysis (EDA)
- Examined skewness in numerical features.
- Visualized outliers using box plots.
- Analyzed correlations among selected numerical variables.
- Investigated relationships between vehicle features and selling price.

### 5. Data Preprocessing
- Split the dataset into training and testing sets.
- Applied feature scaling using StandardScaler.
- Prepared numerical features for regression modeling.

### 6. Machine Learning Models

The following regression algorithms were explored:

1. Linear Regression
2. Polynomial Regression
3. Lasso Regression
4. Ridge Regression
5. Elastic Net Regression
6. K-Nearest Neighbors (KNN) Regression
7. Support Vector Regression (SVR)
8. Decision Tree Regression

Hyperparameter tuning was performed for selected models using GridSearchCV.

### 7. Model Evaluation

Models were evaluated using:

- **R² Score** – Measures the proportion of variance explained by the model.
- **RMSE** – Measures the typical magnitude of prediction errors.
- **Cross-Validation** – Evaluates model performance across multiple data folds.

## 📊 Model Comparison

Based on the results shown in the notebook:

| Model | Train R² | Test R² |
|---|---:|---:|
| Decision Tree Regression | 0.92 | 0.87 |
| Support Vector Regression | 0.90 | 0.85 |
| KNN Regression | 0.88 | 0.82 |
| Polynomial Regression | 0.83 | 0.82 |
| Linear Regression | 0.76 | 0.75 |
| Ridge Regression | 0.76 | 0.75 |
| Elastic Net Regression | 0.76 | 0.75 |
| Lasso Regression | 0.76 | 0.75 |

*Note: Scores are rounded from the notebook output.*

## 🏆 Best Model

**Decision Tree Regression** achieved the best test R² score among the compared models.

- Train R² Score: approximately 0.92
- Test R² Score: approximately 0.87

The model achieved the project's target R² score of 0.85 on both training and testing data.

The selected model was saved using Joblib for later use.

## 💾 Model Saving and Loading

The best model was saved using:

```python
import joblib

joblib.dump(model_dt, 'best_model')
```

The saved model can be loaded using:

```python
abc = joblib.load('best_model')
predictions = abc.predict(x_test)
```

## 📁 Project Structure

```text
Used-Car-Price-Prediction/
│
├── Used Car Price Prediction.ipynb
├── cars24_cleaned.csv
├── best_model
└── README.md
```

*Include the dataset and saved model only if you intend to share them and have permission to do so.*

## 🚀 Key Learnings

- Data cleaning and preprocessing
- Feature engineering for regression problems
- Exploratory Data Analysis
- Categorical feature encoding
- Feature scaling
- Training and comparing regression algorithms
- Hyperparameter tuning with GridSearchCV
- Model evaluation using R², RMSE, and cross-validation
- Saving and loading machine learning models

## 🔮 Future Improvements

- Build an interactive web application for price prediction.
- Improve feature selection and hyperparameter tuning.
- Experiment with ensemble models such as Random Forest and Gradient Boosting.
- Develop a complete prediction pipeline for new car records.

## 👩‍💻 Author

**Chhaya Soni**

Aspiring Data Analyst | Machine Learning Enthusiast

- GitHub: https://github.com/chhaya-soni-analytics
- LinkedIn: https://linkedin.com/in/chhaya-soni-1733a324b/
- Medium: https://medium.com/@chayasonidurg

---

⭐ If you find this project useful, feel free to explore the repository and share your feedback.
