# 🛢️ Groundnut Oil Adulteration Detection

Detect adulteration levels in groundnut oil using spectral data and machine learning.  
Implemented **Logistic Regression, SVM, Decision Tree, and Random Forest classifiers**.

---

## 📂 Dataset Overview

- **Source:** [Groundnut Oil Adulteration Dataset](https://github.com/ishwarjagdale/ground-nut-oil-adulteration/blob/main/data/Groundnut%20Oil%20Adulteration.csv)  
- **Samples:** 160 entries, 130 columns (Wavelength measurements + target)  
- **Target Classes:** `pure` → 0, `25% adulteration` → 1, `50% adulteration` → 2, `6.25% adulteration` → 3  

---

## 🧹 Data Preprocessing

- Checked for null values: None  
- Encoded categorical labels (0–3)  
- Split dataset into training (70%) and testing (30%) sets  

---

## 🧠 Models Implemented

This project implements the following classification models to detect adulteration in groundnut oil:

- Logistic Regression  
- Support Vector Machine (SVM)  
- Decision Tree  
- Random Forest  

### 📊 Model Evaluation

| Model                 | Accuracy |
|-----------------------|----------|
| Logistic Regression   | 0.71     |
| SVM                   | 0.71     |
| Decision Tree         | 0.69     |
| Random Forest         | 0.98     |

**Best performing model:** Random Forest (98% accuracy)
---

## 🧰 Tech Stack

- Language: Python

- Libraries: Pandas, NumPy, Scikit-learn, Matplotlib

- Environment: Jupyter Notebook / Anaconda

---
