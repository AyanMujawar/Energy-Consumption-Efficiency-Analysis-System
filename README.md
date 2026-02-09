# Energy Consumption & Efficiency Analysis System

A machine learning project analyzing household energy consumption patterns using regression, classification, and clustering techniques.

## 🎯 Project Overview

This project analyzes household energy consumption data through four main analytical phases:
1. **Data Preprocessing** - Cleaning, outlier removal, and feature engineering
2. **Regression** - Predicting energy consumption with multiple models
3. **Classification** - Classification energy efficiency based on consumption patterns
4. **Clustering** - Segmenting households into distinct consumption profiles

## 📊 Dataset

**File:** `Household energy unit data.csv`

**Main Features:**
- Energy consumption in kWh (target)
- Household size, rooms, area
- Appliances: AC, TV, flat type
- Urban/rural classification

**Engineered Features:**
- Energy per person & per square meter
- Energy density and efficiency ratios

## 🔧 Models & Techniques

**Regression Models:**
- Linear, Ridge, Lasso, Polynomial Regression
- Random Forest Regression
- Metrics: MSE, R², MAE, RMSE

**Classification Models:**
- Decision Tree, KNN, SVM, Logistic Regression
- Random Forest Classifier
- Metrics: Accuracy, F1-Score, ROC-AUC

**Clustering Methods:**
- K-Means, Hierarchical Clustering, DBSCAN
- Metrics: Silhouette Score, Davies-Bouldin Index

## 🚀 Quick Start

```bash
# Install dependencies
pip install pandas numpy scikit-learn matplotlib seaborn scipy

# Run the analysis
jupyter notebook "Energy Consumption & Efficiency Analysis System.ipynb"
```

## 📈 Key Results

- **Best regression model**: R² > 0.85 (Random Forest)
- **Cross-validated models**: F1-Scores compared across classifiers
- **3 household clusters** identified with distinct energy profiles

## 📁 Files

- `Energy Consumption & Efficiency Analysis System.ipynb` - Main analysis notebook
- `Household energy unit data.csv` - Dataset
- `README.md` - This file
