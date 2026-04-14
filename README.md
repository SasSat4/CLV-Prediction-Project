# Customer Lifetime Value (CLV) Prediction & Customer Segmentation

## 📌 Project Overview

This project presents an end-to-end machine learning pipeline to predict Customer Lifetime Value (CLV) and perform customer segmentation using transactional data. The solution combines regression and clustering techniques to generate actionable business insights for customer targeting and retention.

## Problem Statement

Businesses need to identify high-value customers and predict future revenue to optimize marketing strategies and improve customer retention. This project addresses:

Predicting future customer spend (CLV)
Segmenting customers into High, Medium, and Low-value groups

## 📊 Dataset

Dataset used: Online Retail Dataset
Source: https://archive.ics.uci.edu/ml/datasets/online+retail

## Project Workflow

## 🧹 Data Preprocessing
Removed missing values, duplicates, and canceled transactions
Handled outliers in Quantity and Price

## ⚙️ Feature Engineering
Created Revenue = Quantity × Price
Aggregated data to customer level
Engineered features:
      Recency
      Frequency
      Monetary (RFM)
      Tenure

## 🎯 Target Variable (CLV)
     Defined CLV as future customer spend
     Used time-based train-test split (70–30) for realistic prediction

## 🤖 Model Building
       Model	                       Performance
    Lasso Regression	                R² ≈ 0.17
    LightGBM (Baseline)	              RMSE ≈ 234, R² ≈ 0.90
    Stacking Ensemble	                R² ≈ 0.84

## 📈 Model Validation
Applied K-Fold Cross Validation for initial evaluation
Adopted time-based validation to preserve temporal structure

## 🔧 Hyperparameter Tuning
Used RandomizedSearchCV with TimeSeriesSplit
Final LightGBM performance:
    RMSE ≈ 212
    R² ≈ 0.92

## 📊 Feature Importance

    Key drivers of CLV:
       Monetary (highest impact)
       Tenure
       Frequency

## 🔍 Customer Segmentation (Advanced)
      Applied Gaussian Mixture Model (GMM)
      Identified 9 clusters, consolidated into:
         💎 High Value Customers
         🙂 Medium Value Customers
         ⚠️ Low Value Customers

## 🔹 Key Insights
     A small group of customers contributes to the majority of revenue
     Monetary value and purchase frequency are strong indicators of CLV
     LightGBM effectively captures non-linear customer behavior
     Clustering enables actionable segmentation for targeted marketing

## ⚙️ Tools & Libraries

* Python
* Pandas
* NumPy
* Matplotlib / Seaborn
* Scikit-learn

## 🔹 Results
  Built a robust CLV prediction model with R² ≈ 0.92
  Successfully segmented customers into meaningful business groups
  Enabled data-driven decision-making for marketing strategies

## 📈 What I Did

* Data cleaning & preprocessing
* RFM (Recency, Frequency, Monetary) analysis
* Customer segmentation
* CLV prediction model

## 🔹 Conclusion

This project demonstrates how combining predictive modeling (LightGBM) with unsupervised learning (GMM) can deliver both accurate predictions and actionable customer segmentation.

## 🔹 Future Improvements
   Deploy model using Streamlit or Flask
   Build interactive dashboard (Power BI / Tableau)
   Incorporate additional customer features

## ▶️ How to Run

1. Download dataset from the link above
2. Place it in the same folder as notebook
3. Open and run the `.ipynb` file

## 📌 Author

Sashank Sathvik Bhaskarani
