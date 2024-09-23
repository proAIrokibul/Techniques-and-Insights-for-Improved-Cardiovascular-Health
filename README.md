# Cardiovascular Disease Prediction Project

This project aims to predict the likelihood of cardiovascular disease using patient data. The dataset consists of various health indicators such as age, gender, height, weight, blood pressure readings, cholesterol levels, glucose levels, and lifestyle habits (e.g., smoking, alcohol consumption, physical activity).

## Project Overview

### 1. **Objective**
The goal of this project is to build and evaluate machine learning models that can predict whether a person is likely to have cardiovascular disease (`cardio` column: 0 = no, 1 = yes). Several models were trained and compared based on their accuracy and performance metrics such as precision, recall, F1-score, and ROC-AUC.

### 2. **Dataset**
- **Total Samples**: 70,000
- **Features**:
  - `age`: Age of the patient (in days)
  - `gender`: Gender of the patient (1 = female, 2 = male)
  - `height`: Height of the patient (in cm)
  - `weight`: Weight of the patient (in kg)
  - `ap_hi`: Systolic blood pressure
  - `ap_lo`: Diastolic blood pressure
  - `cholesterol`: Cholesterol levels (1 = normal, 2 = above normal, 3 = well above normal)
  - `gluc`: Glucose levels (1 = normal, 2 = above normal, 3 = well above normal)
  - `smoke`: Whether the patient smokes (1 = yes, 0 = no)
  - `alco`: Whether the patient consumes alcohol (1 = yes, 0 = no)
  - `active`: Whether the patient is physically active (1 = yes, 0 = no)
  - `cardio`: Target label indicating if the patient has cardiovascular disease (1 = yes, 0 = no)

### 3. **Preprocessing**
The following preprocessing steps were applied to the dataset:
- **Handling missing values**: Verified no missing values were present.
- **Outlier detection**: Box plots were used to detect and visualize outliers, specifically in columns such as `ap_hi`, `ap_lo`, and `weight`.
- **Feature scaling**: Applied standard scaling to the features before training the models.

### 4. **Exploratory Data Analysis (EDA)**
EDA was performed to understand the data better and uncover hidden patterns. Key insights from the analysis include:
- Distribution of patients with cardiovascular disease across different age groups.
- Correlation between blood pressure levels and cardiovascular disease.
- Impact of lifestyle habits like smoking and alcohol consumption on the target variable.

### 5. **Modeling**
Three machine learning models were applied:
1. **Logistic Regression**: A simple linear classifier used for binary classification.
2. **Random Forest**: An ensemble model that uses multiple decision trees to improve prediction performance.
3. **Support Vector Machine (SVM)**: A powerful classifier that works well with high-dimensional spaces.

Each model was evaluated using metrics such as accuracy, precision, recall, F1-score, and ROC-AUC.

### 6. **Results**
- **Logistic Regression** achieved the highest **ROC-AUC** score of 0.7810, making it the best-performing model for this task.
- **Support Vector Machine (SVM)** followed closely with an **accuracy** of 0.7233 and **ROC-AUC** of 0.7789.
- **Random Forest** had the lowest performance with an **accuracy** of 0.6929 and **ROC-AUC** of 0.7503.

### 7. **Conclusion**
The project demonstrates that Logistic Regression is an effective and interpretable model for predicting cardiovascular disease. It achieved the best balance between sensitivity and specificity (as shown by the ROC-AUC). Support Vector Machine also performed well, while Random Forest fell behind in performance.

