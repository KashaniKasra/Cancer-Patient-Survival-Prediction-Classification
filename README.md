# Cancer Patient Survival Classification

This project develops a machine learning pipeline to predict cancer patient survival status using clinical, demographic, and treatment data. The goal is to classify each patient as either **Alive (1)** or **Deceased (0)**.

## Objective

Build a binary classification model to accurately predict `Survival_Status` using:
- Demographics (age, weight, occupation, etc.)
- Clinical history (diagnosis date, cancer type, stage)
- Treatment details (surgery, chemo, radiation, targeted therapy)
- Lifestyle factors (smoking, alcohol, urban/rural)

---

## Dataset Overview

- `train_data.csv`: Training dataset with complete features and labels.
- `test_data.csv`: Unlabeled test set for final model evaluation.

### Key Features Include:
- `Birth_Date`, `Diagnosis_Date`, `Surgery_Date`
- `Cancer_Type`, `Stage_at_Diagnosis`, `Symptoms`, `Tumor_Size`
- `Radiation_Sessions`, `Chemotherapy_Drugs`, `Immunotherapy`, `Targeted_Therapy`
- `Family_History`, `Urban_Rural`, `Occupation`, `Insurance_Type`

---

## Pipeline Steps

### 1. Data Exploration
- Correlation of features with survival status
- Distribution analysis across treatment and lifestyle factors

### 2. Preprocessing & Feature Engineering
- Encoding: One-hot/Label encoding for categorical variables
- Date transformation: Age, time since diagnosis, surgery gap
- Handling missing values
- Scaling numerical features

### 3. Model Training
- Evaluated multiple classifiers: Logistic Regression, Random Forest, SVM
- Cross-validation and hyperparameter tuning
- Metrics: Accuracy (primary), F1-score, Precision, Recall

### 4. Final Prediction
- Generated `submission.csv` with:
  - `id`: Unique test sample identifier
  - `label`: Predicted survival status (0 or 1)

---

## Tools & Libraries

- Python (Pandas, Numpy, Scikit-learn, XGBoost)
- Jupyter Notebook
- Matplotlib / Seaborn for visualization

---

## Insights

- Stage at diagnosis, recurrence status, and therapy types showed the strongest predictive power.
- Lifestyle and insurance type had secondary but meaningful impacts.