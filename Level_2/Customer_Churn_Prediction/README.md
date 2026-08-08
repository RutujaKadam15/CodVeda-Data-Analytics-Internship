# 🏠 House Price Prediction Using Linear Regression

## 📖 Project Overview

This project implements a **Linear Regression model** to predict house prices using the Boston Housing dataset.

The project covers the complete basic regression workflow, including dataset loading, data exploration, feature-target separation, train-test splitting, model training, prediction, model evaluation, and visualization of actual versus predicted prices.

---

## 🎯 Business Scenario

Real estate businesses need reliable methods to estimate property prices based on different housing and neighborhood characteristics.

A regression model can help estimate house prices from multiple property-related factors, providing a data-driven baseline for property valuation and analysis.

---

## ❓ Business Problem

**How can a Linear Regression model be used to predict house prices based on multiple housing and neighborhood features?**

---

## 🎯 Project Objectives

- Load and explore the House Price dataset.
- Understand the structure and statistical characteristics of the data.
- Separate independent features from the target variable.
- Split the dataset into training and testing sets.
- Build a Linear Regression model.
- Predict house prices for unseen test data.
- Evaluate model performance using regression metrics.
- Compare actual and predicted house prices visually.

---

## 📂 Dataset Information

**Dataset:** Boston Housing Dataset

The dataset contains information about housing and neighborhood characteristics.

### Features

| Feature | Description |
|---|---|
| CRIM | Per capita crime rate |
| ZN | Proportion of residential land zoned for large lots |
| INDUS | Proportion of non-retail business acres |
| CHAS | Charles River dummy variable |
| NOX | Nitric oxide concentration |
| RM | Average number of rooms per dwelling |
| AGE | Proportion of owner-occupied units built before 1940 |
| DIS | Weighted distance to employment centers |
| RAD | Index of accessibility to radial highways |
| TAX | Property tax rate |
| PTRATIO | Pupil-teacher ratio |
| B | Demographic-related index |
| LSTAT | Lower-status population percentage |
| MEDV | Median value of owner-occupied homes |

### Target Variable

**MEDV** – Median value of owner-occupied homes.

---

## 🛠️ Tools & Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

---

## 🔄 Project Workflow

```text
Dataset Loading
      ↓
Data Exploration
      ↓
Dataset Information & Statistics
      ↓
Feature & Target Separation
      ↓
Train-Test Split
      ↓
Linear Regression Model
      ↓
Model Training
      ↓
Price Prediction
      ↓
Model Evaluation
      ↓
Actual vs Predicted Visualization
```

---

## 🧹 Data Exploration

The following steps were performed before modeling:

- Displayed the first five records.
- Checked dataset information using `df.info()`.
- Checked the dataset shape.
- Generated descriptive statistics using `df.describe()`.
- Assigned meaningful column names.
- Separated features and target variable.

---

## 🤖 Machine Learning Model

### Linear Regression

A **Linear Regression** model was used to establish a baseline relationship between the housing features and the target variable (`MEDV`).

The dataset was divided into:

- **80% Training Data**
- **20% Testing Data**

The model was trained on the training data and evaluated on unseen testing data.

---

## 📊 Model Evaluation

The model was evaluated using:

- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- R-squared (R²)

### Results

| Metric | Result |
|---|---:|
| MAE | 3.19 |
| MSE | 24.29 |
| RMSE | 4.93 |
| R² Score | 0.67 |

### Interpretation

The model achieved an **R² score of 0.67**, meaning that the model explains approximately **67% of the variation in the target variable** on the test data.

The RMSE of **4.93** represents the typical magnitude of prediction error in the target variable's units.

---

## 📈 Actual vs Predicted Prices

A scatter plot was created to compare:

- **Actual House Prices**
- **Predicted House Prices**

This visualization helps assess how closely the model's predictions follow the actual values.

---

## 💡 Key Findings

- The Linear Regression model provides a reasonable baseline for house price prediction.
- Multiple housing and neighborhood features can be used together to predict `MEDV`.
- The model achieved an R² score of 0.67 on the test data.
- The actual-versus-predicted visualization shows a positive relationship between actual and predicted values.

---

## 📌 Business Recommendations

Based on this analysis:

- Real estate businesses can use regression models as a baseline for data-driven property valuation.
- Property characteristics should be considered together rather than relying on a single factor.
- Model performance should be monitored when applying the approach to new market data.
- More advanced models can be evaluated to potentially improve prediction accuracy.

---

## 📁 Project Structure

```text
House_Price_Prediction/
│
├── Level_2_Task_1_Regression_Analysis.ipynb
├── House_Price_Dataset.csv
└── README.md
```

> Dataset filename should match the actual filename uploaded to this repository.

---

## 🚀 Future Improvements

- Compare Linear Regression with other regression algorithms.
- Perform feature selection and engineering.
- Analyze feature importance.
- Apply cross-validation.
- Tune model parameters.
- Evaluate additional regression models such as Random Forest or Gradient Boosting.

---

## 🎓 Learning Outcomes

Through this project, I gained practical experience in:

- Regression analysis
- Train-test splitting
- Linear Regression
- Model prediction
- Regression evaluation metrics
- Data visualization
- Interpreting model performance

---

## 👩‍💻 Author

**Rutuja Kadam**

Aspiring Data Analyst | Python | SQL | Power BI | Machine Learning
