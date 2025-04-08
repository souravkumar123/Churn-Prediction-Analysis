# Churn Analysis Project - Telecom 📱💡

## Introduction to Churn Analysis 🧑‍💻
In today’s competitive business environment, retaining customers is crucial for long-term success. **Churn analysis** is a key technique used to understand and reduce customer attrition. It involves examining customer data to identify patterns and reasons behind customer departures. By using advanced data analytics and machine learning, businesses can predict which customers are at risk of leaving and understand the factors driving their decisions. This knowledge allows companies to take proactive steps to improve customer satisfaction and loyalty.

## Data & Other Resources Used 📊📂

**Colors used:**
- #4A44F2, #9B9FF2, #F2F2F2, #A0D1FF

### Target Audience 🎯
This project primarily focuses on churn analysis for a telecom firm. However, the techniques and insights can be applied across various industries like retail, finance, and healthcare. Any business valuing customer retention can benefit from churn analysis. We explore methods, tools, and best practices to reduce churn and improve customer loyalty.

## Project Target 🎯

Create an entire ETL process in a database & a Power BI dashboard to utilize the customer data and achieve the following goals:
- **Visualize & Analyze Customer Data** at various levels:
  - Demographic 👨‍👩‍👧‍👦
  - Geographic 🌍
  - Payment & Account Info 💳
  - Services 🛠️
- Study churner profiles & identify areas for implementing marketing campaigns 📈
- Identify methods to predict future churners 🔮

### Metrics Required 📏
- **Total Customers** 👥
- **Total Churn & Churn Rate** 📉
- **New Joiners** 🆕

---

## STEP 1 – ETL Process in SQL Server 💾🔄
- Load the data from the source file into Microsoft SQL Server.
- **Create Database:**
  ```sql
  CREATE DATABASE db_Churn
Import Data into Staging Table via the Import Wizard.

Data Exploration: Check distinct values and identify null values for better data cleaning.

## STEP 2 – Power BI Transform 🔄📊
1. Data Preparation & Cleaning
Add new columns like Churn Status and categorize Monthly Charge.

Map Age Groups and Tenure Groups to better analyze customer behavior.

2. Power BI Measures 🔢
Total Customers = Count of Customer_ID

New Joiners = Filtered customers who joined.

Total Churn = Sum of Churn Status

Churn Rate = Total Churn / Total Customers

## STEP 3 – Power BI Visualization 📊✨
Summary Page:
Top Card:

Total Customers 👥

New Joiners ✨

Total Churn 📉

Churn Rate % 🔽

Demographic Analysis:
Gender 💁‍♂️💁‍♀️ vs Churn Rate 📊

Age Group 👶👵 vs Churn Rate

Account Info:
Payment Method 💳 vs Churn Rate 📉

Contract 📑 vs Churn Rate

Geographic Analysis:
Top 5 States 🌍 vs Churn Rate 📉

Churn Distribution:
Churn Category 🔴 vs Total Churn

Churn Reason 🔍

## STEP 4 – Predict Customer Churn with Random Forest 🌲
What is Random Forest? 🌲
Random Forest is an ensemble machine learning method that utilizes multiple decision trees to predict outcomes, improving accuracy and reducing overfitting.

# Steps:
Data Preparation: Import the data and encode categorical features.

Model Training: Use Random Forest to predict customer churn.

Model Evaluation: Assess performance using metrics like confusion matrix and classification report.

Feature Importance: Identify key factors driving churn using feature importance.

Libraries Used 📚:
pandas

numpy

matplotlib

seaborn

scikit-learn

joblib

Example Code:
python
Copy
import pandas as pd
import numpy as np
from sklearn.model_selection import train_test_split
from sklearn.ensemble import RandomForestClassifier
from sklearn.metrics import classification_report, confusion_matrix

# Load and preprocess the data
data = pd.read_excel('Prediction_Data.xlsx', sheet_name='vw_ChurnData') 

## STEP 5 – Power BI Visualization of Predicted Data 📊🔮
Predicted Churn Analysis:
Import predicted churn data into Power BI and visualize key metrics:

Customer ID 📇

Monthly Charge 💳

Total Revenue 💰

Total Refunds 💸

Number of Referrals 📞

## Conclusion 🎯
The churn analysis provides actionable insights for understanding customer behavior and predicting future churn. By leveraging machine learning models like Random Forest and visualizing the data in Power BI, businesses can enhance retention strategies and improve customer satisfaction.
