# Stroke-Prediction
This project is a Machine Learning-based web application that predicts the risk of stroke based on patient health data. It uses a trained XGBoost model and is deployed via Streamlit for easy interaction.


## 📁 Dataset

- **Source:** [Kaggle - Stroke Prediction Dataset](https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset)
- **Size:** 5,110 records × 12 features
- **Target Variable:** `stroke` (0 = no stroke, 1 = stroke)

---

## 📊 Features Used

- age, hypertension, heart_disease, avg_glucose_level, bmi
- gender, ever_married, work_type, residence_type, smoking_status
- (All categorical features are one-hot encoded)

---

## Model Pipeline

1. Data Cleaning (handle nulls, encode categories)
2. Feature Scaling using `PowerTransformer`
3. SMOTE applied to handle class imbalance (only 5% positive class)
4. Model training using `XGBoostClassifier`
5. Evaluation using Recall, F1-score, and ROC-AUC

---

##  Evaluation Results (Tuned Model)

| Metric       | Value    |
|--------------|----------|
| Accuracy     | 82% ✅    |
| Recall (1)   | 48% ✅    |
| F1-score (1) | 21%      |
| ROC-AUC      | 0.78 ✅   |

---

## Streamlit App

Launch the web app locally:

```bash
streamlit run app.py
