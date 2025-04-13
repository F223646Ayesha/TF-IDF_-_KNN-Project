# 🧠 Disease Classification using TF-IDF, One-Hot Encoding, and KNN

This project applies classical data science techniques to predict disease categories using text-based features like **Risk Factors**, **Symptoms**, and **Signs**. We explore and compare two feature encoding methods — **TF-IDF** and **One-Hot Encoding** — and evaluate classification performance using **K-Nearest Neighbors (KNN)** and **Logistic Regression**.

## ✅ Objectives

- Preprocess text-based disease features for modeling.
- Implement and compare **TF-IDF** and **One-Hot Encoding** strategies.
- Train and evaluate **KNN** models across distance metrics and k-values.
- Compare against **Logistic Regression** baseline.
- Visualize feature space using **PCA** and **SVD**.
- Build an **interactive Streamlit app** for category prediction.

---

## 🧪 Tasks Overview

### **Task 1 – TF-IDF Feature Extraction**
- Parsed list-like strings in Risk Factors, Symptoms, Signs
- Transformed into flat text
- Applied TF-IDF to each column separately and combined

### **Task 2 – Dimensionality Reduction**
- Used PCA and SVD to project both encodings to 2D
- Visualized clustering by disease category
- Compared explained variance ratios

### **Task 3 – Model Training & Evaluation**
- Trained KNN models for `k = 3, 5, 7` with `Euclidean`, `Manhattan`, and `Cosine` distances
- 5-fold cross-validation on both TF-IDF and One-Hot
- Trained Logistic Regression as a baseline
- Collected **Accuracy, Precision, Recall, F1** for each setup

### **Task 4 – Critical Analysis**
- Compared encodings and model types
- Analyzed clinical relevance of feature clusters
- Highlighted limitations and improvement areas

---

## 🌐 Streamlit Web App

The project includes a **Streamlit application** for live disease category prediction.

### Features:
- Select any disease from the dataset
- Choose between **TF-IDF** and **One-Hot**
- Tune `k` and distance metric
- Get the **Top 3 most likely categories**, along with vote counts

### ▶️ To Run Locally:
streamlit run streamlit_knn_app.py

📊 Results Summary
Model	Encoding	Best Distance	Best k	F1 Score
KNN	One-Hot	Cosine	5	0.74
Logistic Regression	TF-IDF	-	-	0.78
(Note: Table values are illustrative. See task3_model_comparison_results.csv for actual results.)

🚀 Future Improvements
Replace hand-crafted encodings with word embeddings

Add contextual preprocessing (synonyms, negations, etc.)

Try more complex models like Random Forest, XGBoost, or SVM

Add explainability (e.g., SHAP or LIME)

Deploy the app using Streamlit Cloud or Hugging Face Spaces

👨‍💻 Built With
Python

Pandas, NumPy, Scikit-learn

Matplotlib, Seaborn

Streamlit

📌 Credits
This project was completed as part of a Data Science assignment focused on applying encoding, classification, evaluation, and app development techniques to real-world healthcare data.

Developed by: Ayesha
