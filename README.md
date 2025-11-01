# 🧠 Talent Salary Prediction Model – DAC 2025

## 📘 Overview
This project was developed for the **Data Analytics Competition (DAC) 2025**, which focused on building a machine learning model to predict the **salary range of job candidates** based on their **curriculum vitae (CV)** information.  

The dataset includes features such as **work experience, job position, education level, and certifications**.  
The goal was to predict two numerical targets — **Lower Salary Estimate** and **Upper Salary Estimate** — to provide a realistic salary range aligned with market standards.  

Although this project did not win the competition, it represents a complete end-to-end **data science workflow**, demonstrating strong skills in feature engineering, preprocessing, and model optimization for salary prediction tasks.

---

## 📊 Dataset
- **Source:** Official DAC 2025 competition dataset  
- **Samples:** ~10,000 candidates  
- **Main Features:**  
  - `experience_years` – total years of professional experience  
  - `job_title` – most recent job title  
  - `education_level` – highest academic qualification  
  - `certifications` – number or list of certifications held  
  - Other structured and text-based features extracted from CV data  
- **Targets:**  
  - `estimate_up`  
  - `estimate_bottom`

---

## ⚙️ Workflow
### 1. Exploratory Data Analysis (EDA)
- Analyzed feature distributions, outliers, and correlations.  
- Visualized patterns in experience level and salary range.  
- Identified categorical and numerical feature groups.

### 2. Feature Engineering
- Created interaction features between experience, job role, and education level.  
- Extracted and normalized text-based features from job titles.  
- Encoded categorical variables for modeling compatibility.

### 3. Data Preprocessing
- **Imputation:** Used `SimpleImputer` to fill missing numerical values.  
- **Scaling:** Standardized numerical columns with `StandardScaler`.  
- **Encoding:** One-hot encoding for categorical columns.  
- **Balancing:** Applied **SMOTE** to handle imbalanced training data.

### 4. Model Training
- Trained a **RandomForestRegressor** to predict both salary bounds.  
- Used grid search and cross-validation to tune hyperparameters.  
- Saved trained models with `joblib` for reproducibility.

### 5. Evaluation
- Metric used: **Mean Absolute Error (MAE)**  
- Cross-validation average MAE ≈ **1.23 × 10⁶**  
- Final model showed consistent performance and generalization across folds.
