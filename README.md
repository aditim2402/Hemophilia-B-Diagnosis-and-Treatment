# Hemophilia-B-Diagnosis-and-Treatment

This project focuses on classifying genetic variants related to Hemophilia B using machine learning techniques. The primary objective is to develop a model that accurately predicts the severity of a variant based on its features. The dataset includes multiple attributes describing genetic variations, mechanisms, and severity levels. The model achieved high accuracy through data preprocessing, feature engineering, hyperparameter tuning, and evaluation using XGBoost, SVM, and Random Forest classifiers.

---

## Introduction
Hemophilia B is a rare X-linked genetic disorder caused by mutations in the F9 gene, leading to a deficiency in Factor IX, a crucial protein required for blood clotting. The condition varies in severity among individuals, making diagnosis and treatment highly unpredictable. Current diagnostic methods, such as clotting factor assays and genetic testing, confirm the presence of mutations but fail to predict disease severity, treatment resistance, or long-term patient outcomes. 

With over 1,400 documented genetic mutations, understanding the relationship between mutation type, severity classification, and treatment response remains a significant challenge. This study leverages machine learning models, specifically XGBoost, SVM, and Random Forest, to classify genetic variants based on their severity while addressing class imbalance using SMOTE. By integrating predictive analytics with genetic data, this model aims to provide clinicians with actionable insights, improve early diagnosis, and enhance precision medicine approaches for Hemophilia B patients.

---

## Problem Statement
Despite advances in genetic research, there is currently no comprehensive predictive framework for Hemophilia B that integrates genetic mutations, severity classification, and treatment response. Existing classification methods often lack scalability, accuracy, and the ability to personalize treatment plans. This project aims to bridge this gap by leveraging machine learning techniques to enhance the prediction of severity levels and treatment outcomes for Hemophilia B patients.

### **Key Objectives:**
- **Severity Prediction:** Accurately classifying Hemophilia B cases into Severe, Moderate, and Mild categories based on genetic mutations, enabling early diagnosis and intervention.
- **Treatment Resistance Analysis:** Identifying specific mutations associated with reduced treatment efficacy, aiding in better treatment planning.
- **Personalized Medicine:** Developing a predictive model that tailors treatment strategies based on a patient’s unique genetic profile.
- **Scalable Data Utilization:** Structuring and analyzing a dataset containing over 1,400 mutations to derive clinically meaningful insights.

To achieve these goals, this project implements machine learning models, particularly XGBoost, SVM, and Random Forest, while addressing class imbalance using SMOTE. By integrating advanced predictive analytics with genetic data, this framework seeks to enhance diagnostic precision, improve treatment outcomes, and contribute to the future of personalized medicine for Hemophilia B patients.

---

## Dataset Description
The dataset consists of **1399 entries** and **21 columns**, including:
- **Variant Types**
- **Mechanisms**
- **Exons**
- **Codons**
- **Domains**
- **Severity Levels**

### **Target Variable:**
- Severity Level (Severe, Moderate, Mild)

### **Feature Variables:**
- Variant Type
- Mechanism
- Exon
- Codon
- Domain
- Subtype
- History of Inhibitor

---

## Statistical Analysis Methods
- Data cleaning and preprocessing involved handling missing values and feature selection.
- StandardScaler was used to normalize numerical features.
- Class imbalance was addressed using SMOTE.
- Feature selection was performed using correlation analysis.

---

## Model Selection
- **XGBoost Classifier:** Selected due to its high performance in classification tasks.
- **Random Forest Classifier:** Used as an ensemble learning method to improve prediction accuracy and reduce overfitting.
- **Support Vector Machine (SVM):** Applied to explore non-linear decision boundaries and assess its performance in severity classification.
- **Class Imbalance Handling:** SMOTE (Synthetic Minority Over-sampling Technique) was used to balance the dataset and ensure fair classification across severity levels.
- **Hyperparameter Tuning:** Performed GridSearchCV to optimize parameters for all models, improving their overall effectiveness.

---

## Data Splitting
- Split dataset into **training (80%)** and **testing (20%)**.

### **Training and Evaluation:**
- Used **cross-validation** to validate model performance.
- Evaluated using **accuracy score, classification report, and confusion matrix**.

---

## Performance Metrics
### **XGBoost:**
- **Root Mean Squared Error (RMSE):** 0.1981
- **R² Score:** 0.9412
- **Accuracy:** 97.92%

### **Random Forest:**
- **Root Mean Squared Error (RMSE):** 0.1922
- **R² Score:** 0.9446
- **Accuracy:** 98.38%

### **Support Vector Machine (SVM):**
- **Root Mean Squared Error (RMSE):** 0.2761
- **R² Score:** 0.8858
- **Accuracy:** 96.54%

---

## Classification Report
- **Precision, Recall, and F1-score for each class exceed 96%**, indicating a well-performing model.
- **Random Forest performed the best** with an accuracy of **98.38%**, followed by XGBoost (97.92%), and then SVM (96.54%).
- Random Forest and XGBoost had **higher precision, recall, and F1-scores** across all severity levels.
- **SVM had the highest misclass
![image](https://github.com/user-attachments/assets/4cc011f9-d92c-424c-8b95-4dabea005173)

