# Diabetes Health Indicators – Machine Learning Analysis 🩺📊

## 📌 Overview
This project applies **machine learning techniques** to predict diabetes status using the **CDC Diabetes Health Indicators dataset**.  
The goal is to classify individuals into:
- **Non-diabetic**
- **Pre-diabetic**
- **Diabetic**

The project focuses on handling **class imbalance**, **feature engineering**, and **model comparison**, and includes a complete **research paper** documenting the methodology and results.

---

## 🎯 Objectives
- Predict diabetes risk using health and lifestyle indicators
- Handle highly **imbalanced medical data**
- Compare multiple ML models and evaluate their tradeoffs
- Identify significant predictors of diabetes
- Explore the impact of dimensionality reduction (PCA)

---

## 📊 Dataset
- **Source:** CDC Diabetes Health Indicators (BRFSS)
- **Size:** ~250,000+ records
- **Features:** 21 health and lifestyle indicators (BMI, age, smoking, alcohol use, etc.)
- **Target Variable:** Diabetes status  
  - 0 → Non-diabetic  
  - 1 → Pre-diabetic  
  - 2 → Diabetic  

📌 *Raw data is not included in this repository. See `data/README.md` for download instructions.*

---

## 🧠 Methodology

### 🔹 Data Preprocessing
- Missing value handling using mean substitution
- Categorical feature encoding (One-Hot Encoding)
- Feature scaling using Z-score normalization
- **Class imbalance correction using SMOTENC**
- Dimensionality reduction using **PCA (95% variance retained)**

### 🔹 Models Implemented
- Logistic Regression
- Multilayer Perceptron (MLP)
- Kernel SVM (RBF)
- Random Forest

### 🔹 Evaluation Metrics
- Accuracy
- Precision
- Recall (Sensitivity)
- F1-score
- Specificity
- Confusion Matrix

Metrics were selected specifically for **imbalanced classification problems**.

---

## 🏆 Key Findings
- **Non-linear models** outperform linear models on diabetes prediction
- Random Forest achieved high accuracy and specificity
- Sensitivity remains challenging for distinguishing **pre-diabetic vs diabetic**
- SMOTENC improved class balance but synthetic data quality impacted minority classes
- PCA improved computational efficiency with minimal performance loss

---

## 📄 Research Paper
A full academic paper describing the dataset, methodology, experiments, and findings is included:

📄 **`paper/Diabetes_health_indicator.pdf`**

**Title:**  
*Smarter Predictions, Healthier Lives: Machine Learning in Diabetes*

---

## 📂 Repository Structure
Diabetes-Health-Indicators-ML/
│
├── README.md
├── requirements.txt
│
├── paper/
│ └── Diabetes_health_indicator.pdf
│
├── notebooks/
│ ├── preprocessing.ipynb
│ ├── modeling.ipynb
│ └── evaluation.ipynb
│
├── results/
│ └── metrics_summary.csv
│
├── assets/
│ └── plots/
│
└── data/
└── README.md
