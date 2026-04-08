# 📊 Students Social Media Addiction & Academic Impact Analysis

## 📌 Project Overview

This project investigates the relationship between students’ social media usage and its impact on academic performance. It combines **data analysis, feature engineering, and machine learning modeling** to identify key behavioral patterns and predict whether social media negatively affects students' academic outcomes.

---

## 🎯 Problem Statement

Can we predict whether social media usage affects a student's academic performance based on behavioral and lifestyle features?

---

## 📂 Dataset Description

The dataset includes student-level behavioral and lifestyle attributes such as:

* Average daily social media usage (hours)
* Sleep duration
* Mental health score
* Conflict frequency due to social media
* Academic level
* Most used platform
* Relationship status
* Target variable:

  * `Affects_Academic_Performance` (Binary: 0 / 1)

---

## 🧹 Data Preprocessing

### ✔️ Cleaning & Transformation

* Converted target variable from categorical → binary
* Dropped irrelevant columns:

  * `Student_ID`, `Country`, `Age`, `Gender`, `Addicted_Score`
* Checked and handled missing values

### ✔️ Feature Engineering

* Ordinal encoding:

  * Academic Level → numerical ranking
* One-Hot Encoding:

  * Most Used Platform
  * Relationship Status

### ✔️ Outlier Detection

* Used **IQR method** to detect extreme values in:

  * Daily usage hours

### ✔️ Feature Scaling

* Applied **StandardScaler** on numerical features:

  * Usage hours
  * Sleep hours
  * Mental health score
  * Conflict frequency

---

## 📊 Exploratory Data Analysis (EDA)

* Boxplots comparing:

  * Usage vs academic impact
  * Sleep vs academic impact
  * Mental health vs academic impact
* Correlation heatmap for numerical features
* Platform-based impact analysis
* Behavioral grouping insights

---

## 🤖 Machine Learning Models

The following models were trained and evaluated:

* Logistic Regression (with class balancing)
* Naive Bayes
* Decision Tree (max_depth=4)
* Support Vector Machine (RBF kernel)
* K-Nearest Neighbors (k=5)

---

## ⚙️ Model Evaluation

### 📌 Metrics Used:

* Confusion Matrix
* Classification Report
* Recall (focused on Class 1 → affected students)

### 🔥 Key Insight:

The project prioritizes **Recall for Class 1** to better detect students whose academic performance is negatively affected.

---

## 🏆 Model Comparison

A comparison was performed based on **Recall score (Class 1)** across all models:

| Model               | Objective Focus         |
| ------------------- | ----------------------- |
| Logistic Regression | Balanced baseline model |
| Naive Bayes         | Probabilistic approach  |
| Decision Tree       | Interpretability        |
| SVM                 | Non-linear patterns     |
| KNN                 | Distance-based          |

---

## 🔁 Cross Validation

* Applied **5-Fold Cross Validation** on Logistic Regression
* Metric: Recall

---

## 📈 Key Insights

* Higher daily social media usage correlates with academic decline
* Poor sleep patterns strongly relate to performance issues
* Mental health score is a significant predictor
* Platform usage varies in impact severity
* Behavioral conflicts are strong indicators of addiction

---

## 🚀 Final Outcome

* Built a full ML pipeline from raw data → prediction
* Identified key drivers of academic performance decline
* Compared multiple models for best detection performance
* Focused on real-world objective: **early risk detection**

---

## ⚙️ Technologies Used

* Python
* Pandas & NumPy
* Matplotlib & Seaborn
* Scikit-learn
* Jupyter Notebook

---

## 📦 Project Structure

```
Students-Social-Media-Analysis/
│
├── data/
│   └── Students Social Media Addiction.csv
│
├── notebooks/
│   └── Students_Social_media.ipynb
│
├── requirements.txt
├── README.md
└── .gitignore
```

---

## ▶️ How to Run

```bash
pip install -r requirements.txt
jupyter notebook
```

---

## 📌 Future Improvements

* Hyperparameter tuning (GridSearch / RandomSearch)
* Feature importance analysis
* Model explainability (SHAP / LIME)
* Deployment (Streamlit / Flask)
* Real-time prediction system

---

## 👨‍💻 Author

Mohamed Ahmed
