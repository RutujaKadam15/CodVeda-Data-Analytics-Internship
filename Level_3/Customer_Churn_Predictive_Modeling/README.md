# 👥 Customer Churn Predictive Modeling

## 📖 Project Overview

This project focuses on building and comparing multiple machine learning classification models to predict **customer churn**.

The project follows an end-to-end predictive modeling workflow, including data preprocessing, exploratory analysis, feature engineering, model training, model comparison, hyperparameter tuning, model evaluation, feature importance analysis, and model saving.

Three classification algorithms were evaluated:

- Logistic Regression
- Decision Tree Classifier
- Random Forest Classifier

Random Forest achieved the best overall performance and was further optimized using **GridSearchCV**.

---

## 🎯 Business Scenario

Customer churn can negatively impact business revenue and customer retention. Identifying customers who are likely to leave allows organizations to take proactive actions such as targeted offers, improved customer support, and personalized retention strategies.

A predictive modeling approach can help businesses identify customers at higher risk of churn before they leave.

---

## ❓ Business Problem

**How can machine learning models be used to predict customer churn, compare their performance, and identify the factors that are most important for predicting customer churn?**

---

## 🎯 Project Objectives

- Prepare customer data for predictive modeling.
- Perform data quality checks and exploratory analysis.
- Encode categorical variables.
- Split data into training and testing sets.
- Scale features where required.
- Build multiple classification models.
- Compare model performance using multiple evaluation metrics.
- Identify the best-performing model.
- Optimize the selected model using GridSearchCV.
- Analyze feature importance.
- Save the optimized model for future predictions.

---

## 📂 Dataset Information

**Dataset:** Customer Churn Dataset

The dataset contains customer account, service usage, calling, and billing-related information.

### Dataset Size

- **Rows:** 2,666
- **Columns:** 20
- **Input Features:** 19
- **Target Variable:** Churn

### Target Variable

**Churn**

- `False` → Customer did not churn
- `True` → Customer churned

### Important Features

The dataset includes variables such as:

- State
- Account Length
- Area Code
- International Plan
- Voice Mail Plan
- Number of Voicemail Messages
- Total Day Minutes
- Total Day Calls
- Total Day Charge
- Total Evening Minutes
- Total Evening Calls
- Total Evening Charge
- Total Night Minutes
- Total Night Calls
- Total Night Charge
- Total International Minutes
- Total International Calls
- Total International Charge
- Customer Service Calls

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
Data Exploration
        ↓
Data Quality Checks
        ↓
Categorical Encoding
        ↓
Feature & Target Separation
        ↓
Train-Test Split
        ↓
Feature Scaling
        ↓
Model Training
        ↓
Model Comparison
        ↓
Best Model Selection
        ↓
Hyperparameter Tuning
        ↓
Final Model Evaluation
        ↓
Feature Importance Analysis
        ↓
Model Saving
```

---

## 🔍 Data Exploration & Quality Checks

The dataset was explored using:

- `head()`
- `info()`
- `describe()`
- `shape`

### Data Quality Results

- Total records: **2,666**
- Total features: **20**
- Missing values: **0**
- Duplicate records: **0**

This indicates that the dataset did not contain missing or duplicate records requiring removal.

---

## 🧹 Data Preprocessing

### Categorical Encoding

Categorical variables were converted into numerical values using **LabelEncoder**.

### Feature & Target Separation

The target variable was separated from the input features:

```text
X → Input Features
y → Churn
```

The project used **19 input features** to predict customer churn.

### Train-Test Split

The dataset was divided into:

- **80% Training Data**
- **20% Testing Data**

This resulted in:

- Training records: **2,132**
- Testing records: **534**

### Feature Scaling

`StandardScaler` was applied to the training and testing features for the Logistic Regression model.

---

# 🤖 Machine Learning Models

Three classification algorithms were trained and compared.

## 1. Logistic Regression

Logistic Regression was used as a baseline classification model.

## 2. Decision Tree Classifier

A Decision Tree model was trained to capture non-linear relationships between customer characteristics and churn.

## 3. Random Forest Classifier

Random Forest was trained as an ensemble classification model combining multiple decision trees.

---

# 📊 Model Comparison

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-score

### Results

| Model | Accuracy | Precision | Recall | F1 Score |
|---|---:|---:|---:|---:|
| Logistic Regression | 85.96% | 56.25% | 22.78% | 32.43% |
| Decision Tree | 90.26% | 68.49% | 63.29% | 65.79% |
| Random Forest | **95.13%** | **100.00%** | **67.09%** | **80.30%** |

### Best Performing Model

**Random Forest** achieved the highest overall performance among the three models.

Its results were:

- Accuracy: **95.13%**
- Precision: **100.00%**
- Recall: **67.09%**
- F1 Score: **80.30%**

---

# ⚙️ Hyperparameter Tuning

Because Random Forest performed best, it was selected for further optimization.

**GridSearchCV** with 5-fold cross-validation was used to search for the best combination of hyperparameters.

### Parameters Tested

- `n_estimators`
- `max_depth`
- `min_samples_split`

### Best Parameters

```text
n_estimators = 100
max_depth = None
min_samples_split = 2
```

### Best Cross-Validation Accuracy

**95.22%**

---

# 🏆 Final Model Evaluation

The optimized Random Forest model was evaluated on the test dataset.

### Classification Results

| Class | Precision | Recall | F1 Score |
|---|---:|---:|---:|
| Non-Churn | 0.95 | 1.00 | 0.97 |
| Churn | 1.00 | 0.67 | 0.80 |

### Overall Accuracy

**95%**

The model achieved strong overall classification performance, while the recall for the churn class indicates that there is still room to improve the identification of all customers who are likely to churn.

---

# 📌 Confusion Matrix

A confusion matrix was generated for the optimized Random Forest model to analyze:

- True Positives
- True Negatives
- False Positives
- False Negatives

This helps understand how effectively the model identifies both churned and non-churned customers.

---

# 📈 Feature Importance

Random Forest feature importance was used to identify the variables contributing most strongly to the model's predictions.

### Top Important Features

| Rank | Feature |
|---:|---|
| 1 | Total Day Minutes |
| 2 | Total Day Charge |
| 3 | Customer Service Calls |
| 4 | International Plan |
| 5 | Total Evening Charge |
| 6 | Total Evening Minutes |
| 7 | Total International Calls |
| 8 | Total International Minutes |

### Key Observation

**Total Day Minutes**, **Total Day Charge**, and **Customer Service Calls** were among the most important features in the final Random Forest model.

> Feature importance indicates how useful a variable was to the model's predictions; it does not by itself establish that the feature causes churn.

---

# 💡 Key Insights

- Random Forest significantly outperformed Logistic Regression and Decision Tree in this project.
- The optimized Random Forest achieved approximately **95% test accuracy**.
- The model achieved a **0.80 F1-score for the churn class**.
- Customer usage patterns were important in predicting churn.
- Customer service interactions were also an important predictive feature.
- International plan usage showed notable importance in the model.
- Hyperparameter tuning produced a slightly higher cross-validation accuracy than the initial Random Forest model.

---

# 📌 Business Recommendations

Based on the predictive modeling results, businesses can:

1. **Identify high-risk customers** using the churn prediction model.
2. Monitor customers with high usage levels and frequent customer service interactions.
3. Develop targeted retention campaigns for customers predicted to churn.
4. Investigate customer service experiences and resolve recurring issues.
5. Use customer usage patterns to create personalized retention strategies.
6. Continuously monitor model performance as new customer data becomes available.

---

# 💾 Model Saving

The final optimized Random Forest model was saved using Joblib:

```text
best_random_forest_model.pkl
```

This allows the trained model to be reused for future predictions without retraining it from scratch.

---

# 📁 Project Structure

```text
Customer_Churn_Predictive_Modeling/
│
├── Level_3_Task_1_Predictive_Modeling.ipynb
├── churn-bigml-80.csv
├── best_random_forest_model.pkl
└── README.md
```

> Update the dataset filename if the actual filename uploaded to GitHub is different.

---

# 🚀 Future Improvements

- Optimize the model based on recall for the churn class.
- Address potential class imbalance.
- Compare additional ensemble models.
- Perform cross-validation with multiple evaluation metrics.
- Tune the classification threshold to improve churn detection.
- Deploy the model as an API or interactive web application.
- Monitor model performance on new customer data.

---

# 🎓 Learning Outcomes

Through this project, I gained practical experience in:

- Predictive modeling
- Classification algorithms
- Data preprocessing
- Feature encoding
- Feature scaling
- Model comparison
- Random Forest
- Hyperparameter tuning
- GridSearchCV
- Cross-validation
- Classification metrics
- Confusion matrix
- Feature importance
- Model serialization

---

# 👩‍💻 Author

**Rutuja Kadam**

Aspiring Data Analyst | Python | SQL | Power BI | Machine Learning
