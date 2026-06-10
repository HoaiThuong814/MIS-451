# 🛒 MIS451 - Classification Project

## Predicting Online Shoppers' Purchasing Intention

### 👥 Performed By

* Tran Ngoc Trung Hieu
* Nguyen Ngoc Minh Thu
* Nguyen Thi Hoai Thuong

---

## 📖 Overview

This project develops and evaluates machine learning classification models to predict whether an online shopping session will result in a purchase.

Using behavioral data from an e-commerce website, the study analyzes customer browsing patterns and compares multiple algorithms to identify the most effective model for predicting purchasing intention.

The goal is to support data-driven marketing decisions and help businesses improve conversion rates.

---

## 🎯 Research Question

**Which machine learning model best predicts whether an online session leads to a purchase?**

---

## 📊 Dataset

* **Dataset:** Online Shoppers Purchasing Intention
* **Source:** UCI Machine Learning Repository
* **Sessions:** 12,330
* **Features:** 18
* **Target:** Revenue (Purchase / Non-purchase)

🔗 Dataset Link:
https://archive.ics.uci.edu/dataset/468/online+shoppers+purchasing+intention+dataset

---

## 🔍 Exploratory Data Analysis

### Class Imbalance

* Purchase: 15.6%
* Non-purchase: 84.4%
  → F1-Macro used instead of accuracy

### Key Predictor

* **PageValues** = strongest indicator of purchase

### Customer Behavior

High purchase intention:

* More product page visits
* Longer browsing duration
* Higher PageValues

Low purchase intention:

* High BounceRates
* High ExitRates

### Seasonal Trend

* November = highest traffic & conversion (Black Friday effect)

---

## ⚙️ Data Preprocessing

### Data Cleaning

* Removed 125 duplicates
* No missing values

### Train-Test Split

* Train: 80%
* Test: 20%
* Stratified sampling

### Feature Engineering

* VisitorType → One-Hot Encoding
* Month → Ordinal Encoding

### Scaling

Applied to:

* Logistic Regression
* KNN
* MLP

(Random Forest used raw features)

### Outliers

* Retained (important behavioral signals)

---

## 🤖 Models

* **Logistic Regression** (baseline)
* **KNN** (k = 99)
* **Random Forest** (200 trees)
* **MLP Neural Network** (32,16 hidden layers)

---

## 📈 Model Performance (10-Fold CV)

| Model               | F1-Macro   |
| ------------------- | ---------- |
| Logistic Regression | 0.7765     |
| KNN                 | 0.6045     |
| MLP Neural Network  | 0.7669     |
| Random Forest       | **0.8048** |

🏆 **Best Model: Random Forest**

---

## 🏆 Final Test Results

| Metric    | Score  |
| --------- | ------ |
| Accuracy  | 90.00% |
| Precision | 68.25% |
| Recall    | 67.54% |
| F1-Score  | 67.89% |

---

## 💡 Business Insights

Purchase behavior is strongly driven by customer engagement.

**High Purchase Indicators:**

* High PageValues
* More product page visits
* Longer browsing time

**Low Purchase Indicators:**

* High BounceRates
* High ExitRates

---

## 🚀 Recommendations

### 1. Target High-Intent Users

Use prediction scores to identify likely buyers

### 2. Improve Product Pages

* Better descriptions
* Images
* Reviews
* Recommendations

### 3. Reduce Bounce & Exit

* Optimize landing pages
* Improve website speed
* Better navigation & CTA

---

## 🛠️ Technologies

* Python
* Pandas, NumPy
* Matplotlib, Seaborn
* Scikit-learn
* Jupyter Notebook

---

## 📚 Reference

Sakar, C., & Kastro, Y. (2018).
Online Shoppers Purchasing Intention Dataset.
UCI Machine Learning Repository.
