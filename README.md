# 🧬 Healthcare and Drug Persistency Classification Project
This repository presents a comprehensive machine learning project focused on analyzing and predicting **patient persistency to prescribed drugs** based on a rich set of clinical, demographic, and treatment-related features. The project was developed as part of the Data Glacier Internship Final Project.

## Project Overview
###  Objective
To analyze patient healthcare data and classify drug persistency using various machine learning models. The goal is to discover influential factors affecting persistency and develop accurate prediction models using both traditional and deep learning approaches.

### Background
One of the biggest challenges in the pharmaceutical industry is understanding **why patients do not persist with medication** as prescribed by their physicians. ABC Pharma has provided anonymized patient data (3424 rows × 68 features) including:

- Patient Demographics
- Clinical Test Results (e.g., T-scores, DEXA scans, fractures)
- Provider Attributes (e.g., physician specialty)
- Drug Treatment and Comorbidity Factors

The key target variable is the **Persistency Flag**, indicating whether the patient stayed on the prescribed treatment.
---

## 📂 Dataset Information

- **Source**: ABC Pharma (synthetic/anonymized)
- **Format**: `.csv`, `.xlsx`
- **Rows**: 3424
- **Features**: 68
- **Target**: `Persistency_Flag`

---
##  Models Trained

The following machine learning models were developed and compared:

- **Support Vector Machine (Linear)**
- **AdaBoost Classifier**
- **Gradient Boosting**
- **K-Nearest Neighbor**
- **Multi-Layer Perceptron (MLP)**
- **Custom Keras-based Artificial Neural Network**
- **Autoencoder Feature Extraction + Classifiers**
---

## Results Summary

| Model               | Accuracy | Precision | Recall | F1-score | AUC |
|--------------------|----------|-----------|--------|----------|-----|
| **AdaBoost**        | 81%      | 81%       | 79%    | 81%      | 0.87|
| **Gradient Boosting**| 81%     | 81%       | 78%    | 81%      | 0.88|
| **SVM**             | 79%      | 78%       | 76%    | 78%      | 0.86|
| **ANN (Keras)**     | 78%      | 79%       | 79%    | 79%      | 0.86|

Autoencoders were used for feature reduction, yielding high performance even with just 2 selected features — reducing data dimensionality **by 59x** while maintaining performance.

---

## Key Insights

- **Demographic factors** (age, race, region, gender) showed limited correlation to persistency.
- **Clinical factors** such as comorbidity, risk scores, and drug combinations had the strongest influence.
- Patients with **>3 risk factors** had the highest percentage of non-persistence.
- Dominance analysis showed that most important predictors were clinical, not demographic.

---

## Technologies Used

- Python, Pandas, Numpy
- Scikit-learn
- Keras / TensorFlow
- Matplotlib, Seaborn
- Jupyter Notebook
