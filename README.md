# Stroke Prediction - Machine Learning Optimization




## 📌 Overview

This project focuses on predicting the likelihood of a stroke based on clinical and demographic features (Age, BMI, Hypertension, etc.). The primary challenge of this dataset is the **High Class Imbalance** (only ~5% stroke cases), making standard accuracy a misleading metric.

## 🎯 Goal

To build a classification model that prioritizes **Recall** (identifying as many actual stroke patients as possible) over general accuracy, which is critical in medical diagnostic use cases.


## 🛠️ Tech Stack & Techniques
- **Python:** Pandas, NumPy, Scikit-Learn, Seaborn.
- **Handling Imbalance:** Applied **SMOTE** (Synthetic Minority Over-sampling Technique) to balance the training data.
- **Feature Engineering:** Log transformations for skewed data and Standard Scaling.
- **Optimization:** - **Threshold Tuning:** Shifted the decision boundary from `0.5` to `0.3` to capture more high-risk cases.
  - **Hyperparameter Tuning:** Optimized Logistic Regression and Random Forest.

## 📊 Results & Impact
By tuning the model's threshold, I achieved a significant improvement in the model's ability to catch stroke cases:

| Metric | Default (0.5 Threshold) | Tuned (0.3 Threshold) |
| :--- | :--- | :--- |
| **Recall (Class 1)** | 0.75 | **0.90** |
| **Accuracy** | 0.75 | 0.61 |

**Key Finding:** Lowering the threshold increased the **Recall to 90%**, ensuring that 9 out of 10 stroke patients are correctly alerted, which is a life-saving improvement over the base model.

## 🚀 How to Run
1. Clone the repo:
   ```bash
   git clone [https://github.com/19rehan/stroke-prediction.git](https://github.com/19rehan/stroke-prediction.git)
