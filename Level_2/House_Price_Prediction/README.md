# 👥 Customer Churn Prediction Using Classification

## 📖 Project Overview

This project focuses on building a **Customer Churn Prediction model** using Logistic Regression.

The objective is to predict whether a customer is likely to churn based on customer-related information. The project follows a complete machine learning workflow, including data exploration, preprocessing, categorical encoding, feature scaling, model training, prediction, evaluation, and feature importance analysis.

---

## 🎯 Business Scenario

Customer churn is an important challenge for businesses because losing existing customers can negatively affect revenue and customer relationships.

A predictive classification model can help businesses identify customers who are more likely to churn, allowing them to take proactive retention actions.

---

## ❓ Business Problem

**How can machine learning be used to predict whether a customer is likely to churn and identify the factors associated with customer churn?**

---

## 🎯 Project Objectives

- Explore the customer churn dataset.
- Understand the distribution of churned and non-churned customers.
- Check data quality and missing values.
- Identify duplicate records.
- Analyze relationships between numerical features.
- Encode categorical variables.
- Standardize numerical features.
- Build a classification model using Logistic Regression.
- Evaluate model performance.
- Analyze the factors influencing churn.
- Save the trained model and scaler for future use.

---

## 📂 Dataset Information

**Dataset:** Customer Churn Dataset

The dataset contains customer information and a target variable indicating whether a customer churned.

### Target Variable

**Churn**

- `0` → Customer did not churn
- `1` → Customer churned

The dataset contains customer-related attributes such as:

- Account information
- Usage-related information
- Customer service interactions
- Calling and usage metrics

---

## 🛠️ Tools & Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Joblib
- Jupyter Notebook

---

## 🔄 Project Workflow

```text
Customer Churn Dataset
        ↓
Data Loading
        ↓
Data Exploration
        ↓
Data Quality Checks
        ↓
Churn Distribution Analysis
        ↓
EDA & Visualization
        ↓
Categorical Encoding
        ↓
Feature & Target Separation
        ↓
Train-Test Split
        ↓
Feature Scaling
        ↓
Logistic Regression
        ↓
Prediction
        ↓
Model Evaluation
        ↓
Feature Importance Analysis
        ↓
Model & Scaler Saving
```

---

## 🔍 Exploratory Data Analysis

The following analyses were performed:

### Dataset Exploration

- Displayed the first five records.
- Checked dataset information.
- Checked dataset shape.
- Generated summary statistics.
- Examined data types.

### Data Quality Checks

- Checked for missing values.
- Checked for duplicate records.

### Churn Distribution

Analyzed the number of customers who churned and did not churn.

A bar chart and count plot were created to visualize the churn distribution.

### Correlation Analysis

A correlation heatmap was created using numerical features to understand relationships between variables.

### Churn-Related Analysis

Boxplots were created to analyze the relationship between:

- Customer Churn and Total Day Minutes
- Customer Churn and Customer Service Calls

---

## 🧹 Data Preprocessing

### Categorical Encoding

Categorical columns were converted into numerical values using **Label Encoding**.

### Feature and Target Separation

The target variable was:

```text
Churn
```

All remaining variables were used as input features.

### Train-Test Split

The dataset was divided into:

- **80% Training Data**
- **20% Testing Data**

### Feature Scaling

`StandardScaler` was applied to standardize the input features before training the Logistic Regression model.

---

## 🤖 Machine Learning Model

### Logistic Regression

A **Logistic Regression** classification model was trained to predict customer churn.

The model was trained using the scaled training data and then used to predict churn for the test dataset.

---

## 📊 Model Evaluation

The model was evaluated using:

- Accuracy
- Confusion Matrix
- Classification Report
- ROC Curve

### Confusion Matrix

The confusion matrix was used to analyze:

- True Positives
- True Negatives
- False Positives
- False Negatives

### Classification Report

The classification report provides:

- Precision
- Recall
- F1-score
- Support

### ROC Curve

A ROC curve was generated to evaluate the model's ability to distinguish between churned and non-churned customers.

---

## 📈 Feature Importance

The Logistic Regression coefficients were analyzed to identify features associated with the prediction of customer churn.

A feature importance table and visualization were created using the model coefficients.

---

## 💾 Model Saving

The trained Logistic Regression model was saved using Joblib:

```text
customer_churn_model.pkl
```

The fitted StandardScaler was also saved:

```text
scaler.pkl
```

Saving both allows the preprocessing and trained model to be reused for future predictions.

---

## 💡 Key Findings

The analysis provides insights into customer churn patterns and the variables associated with churn.

In particular, customer usage behavior and customer service interactions were investigated as potential factors related to churn.

The Logistic Regression coefficients were further analyzed to understand which variables had greater influence on the model's predictions.

---

## 📌 Business Recommendations

Based on the predictive modeling approach:

- Identify customers with a higher predicted probability of churn.
- Monitor customers with frequent customer service interactions.
- Analyze usage patterns of customers at higher risk.
- Develop targeted customer retention strategies.
- Use predictive models as an early-warning system for customer churn.

---

## 📁 Project Structure

```text
Customer_Churn_Prediction/
│
├── Level_2_Task_2_Classification_Analysis.ipynb
├── churn-bigml-80.csv
├── customer_churn_model.pkl
├── scaler.pkl
└── README.md
```

> Update the dataset filename above if the actual uploaded filename is different.

---

## 🚀 Future Improvements

- Compare Logistic Regression with Decision Tree and Random Forest models.
- Perform hyperparameter tuning.
- Use cross-validation.
- Handle class imbalance if required.
- Analyze feature importance using additional model-based techniques.
- Deploy the model as an interactive prediction application.
- Monitor model performance on new customer data.

---

## 🎓 Learning Outcomes

Through this project, I gained practical experience in:

- Classification analysis
- Customer churn prediction
- Exploratory Data Analysis
- Categorical encoding
- Feature scaling
- Logistic Regression
- Model evaluation
- Confusion Matrix
- ROC Curve
- Feature importance analysis
- Model serialization using Joblib

---

## 👩‍💻 Author

**Rutuja Kadam**

Aspiring Data Analyst | Python | SQL | Power BI | Machine Learning
