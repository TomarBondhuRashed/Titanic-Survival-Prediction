# 🚢 Titanic Survival Prediction: Feature Engineering & Classification

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Scikit-Learn](https://img.shields.io/badge/Library-Scikit--Learn-orange)
![Status](https://img.shields.io/badge/Status-Completed-green)

## 📌 Project Overview
This project leverages machine learning to predict the survival of passengers on the Titanic. Unlike standard clean datasets, this project focuses heavily on **Data Preprocessing** and **Feature Engineering** to handle missing values (Age, Cabin) and categorical variables (Sex, Embarked).

The goal is to answer the question: *"What sort of people were more likely to survive?"*

---

## 🧹 Data Cleaning & Strategy
Real-world data is messy. Here is how I handled the imperfections in the Titanic dataset:

* **Missing Ages:** Imputed using the **Median** age (28.0) to avoid skewing the data with outliers.
* **Cabin Column:** Dropped due to >75% missing data (Signal-to-Noise ratio was too low).
* **Categorical Encoding:** Converted `Sex` and `Embarked` into numerical dummy variables (One-Hot Encoding) for the Random Forest model.

![Missing Data Heatmap](images/missing_data.png)

---

## 📊 Key Insights (EDA)
Exploratory Data Analysis confirmed the historical "Women and Children First" protocol.

* **Gender:** Female passengers had a significantly higher survival rate (~74%) compared to males (~18%).
* **Class/Fare:** Passengers who paid higher fares (First Class) were more likely to survive.

![Survival by Gender](images/survival_gender.png)

---

## 🤖 Model Performance
I used a **Random Forest Classifier** because of its ability to handle non-linear relationships and interactions between features (e.g., Age + Class).

* **Accuracy:** ~82%
* **Top Predictors:** According to Feature Importance analysis, `Sex`, `Fare`, and `Age` were the most critical factors in predicting survival.

![Feature Importance](images/feature_imp.png)

---

## 🚀 How to Run
1. Clone the repository:
   ```bash
   git clone [https://github.com/your-username/titanic-survival-prediction.git](https://github.com/your-username/titanic-survival-prediction.git)
