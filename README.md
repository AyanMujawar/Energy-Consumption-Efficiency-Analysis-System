# Energy Consumption & Efficiency Analysis System

Machine learning analysis of household energy consumption using regression, classification, and clustering techniques.

## 🎯 Overview

Four-part analysis pipeline:
1. **Data Preprocessing** - Feature engineering, visualization, outlier removal (IQR method)
2. **Regression** - Predict energy consumption with multiple models (Linear, Ridge, Lasso, Polynomial, Random Forest)
3. **Classification** - Binary efficiency classification (Efficient vs Inefficient)
4. **Clustering** - Segment households into 3 consumption profiles (K-Means, Hierarchical)

## 📊 Dataset

**File:** `Household energy unit data.csv`

**Features:**
- Target: `units` (energy consumption in kWh)
- Household: `num_people`, `num_rooms`, `housearea`, `num_children`
- Appliances: `is_ac`, `is_tv`, `is_flat`, `is_urban`

**Engineered Features:**
- `Energy_per_Person` - Energy normalized by household size
- `Energy_per_SqM` - Energy intensity (efficiency metric)

## 🔧 Analysis Details

### Part 1: Preprocessing
- Consolidates data loading and feature engineering
- Handles missing values (median/mode imputation)
- Removes outliers using IQR method (1.5 × threshold)
- Generates distribution histograms, correlations, and categorical plots

### Part 2: Regression
**Models:** Linear, Ridge, Lasso, Polynomial (degree 2), Random Forest

**Approach:**
- SelectKBest feature selection (top 5 features)
- StandardScaler for numerical data
- 80/20 train-test split

**Metrics:** MSE, R², MAE, RMSE, Residual Analysis

### Part 3: Classification
**Target:** Energy Efficiency (0=Efficient, 1=Inefficient) based on Energy_per_SqM median

**Models:** Decision Tree, KNN, SVM, Logistic Regression, Random Forest

**Evaluation:** Accuracy, F1-Score, ROC-AUC, Confusion Matrix

### Part 4: Clustering
**Features:** Energy_per_Person, Energy_per_SqM, Total_Energy_kWh

**Methods:** K-Means (k=3) and Hierarchical Clustering (Ward linkage)

**Metrics:** Silhouette Score, Davies-Bouldin Index, PCA visualization

## � Quick Start

```bash
# Install dependencies
pip install pandas numpy scikit-learn matplotlib seaborn scipy

# Run analysis
jupyter notebook "Energy Consumption & Efficiency Analysis System.ipynb"
```

**Execution:** Run cells sequentially (Parts 1→2→3→4)

## 💡 Key Improvements

- **Reduced redundancy:** Eliminated 4+ duplicate data loads and feature creations
- **Single preprocessing pipeline:** Reuses `df_clean` across all analyses
- **Consolidated classification:** Unified 4 scattered sections into 1
- **Optimized clustering:** Streamlined from 2+ implementations to single best version
- **Notebook reduced by ~30%** while maintaining full functionality

## 📁 Files

- `Energy Consumption & Efficiency Analysis System.ipynb` - Main analysis notebook
- `Household energy unit data.csv` - Input dataset
- `README.md` - Documentation

## ⚙️ Technical Notes

- **Random seed:** 42 (reproducibility)
- **Train-test split:** 80/20 stratified
- **Scaling:** StandardScaler fitted on training data only
- **Outlier removal:** IQR method (1.5 × multiplier)
- **Feature selection:** SelectKBest with f_regression
