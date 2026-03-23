# Spotify Music Genre Classification

## Overview
This project builds a multi-class classification model to predict music genres using ~50,000 Spotify tracks and their audio features. The goal is to compare linear and nonlinear modeling approaches and understand how feature structure affects classification performance.

## Key Results
- **CatBoost (best model):** Macro AUC = **0.939**
- **LDA + Linear SVM:** Macro AUC ≈ **0.878**

## Methodology

### Data Processing
- Handled ~8% missing data using **MICE (Iterative Imputation)**  
- Applied **feature scaling** for linear models  
- Preserved raw features for tree-based models  

### Feature Analysis
- Compared **PCA (unsupervised)** vs **LDA (supervised)**  
- Identified **class overlap (e.g., rap vs hip-hop)** in LDA space  

### Modeling
- **Linear model:** LDA + Linear SVM (with probability calibration)  
- **Nonlinear model:** CatBoost (handles raw + categorical features natively)  

## Key Insights
- Some genres are **not linearly separable**, limiting linear models  
- **Nonlinear feature interactions** are critical for this task  
- CatBoost outperforms linear models by capturing complex patterns without heavy preprocessing  


## Tech Stack
- Python, pandas, NumPy  
- scikit-learn (MICE, PCA, LDA, SVM)  
- CatBoost  
- matplotlib 
