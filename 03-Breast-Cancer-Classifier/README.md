# 🧠 Breast Cancer Detection using Neural Networks

This project implements a **binary classification model** to detect **breast cancer (Malignant vs Benign)** using the **Breast Cancer Wisconsin Diagnostic Dataset**.  
It demonstrates the complete pipeline — from dataset loading, preprocessing, feature standardization, neural network design, training, and evaluation using **TensorFlow and Keras**.

---

## 📁 Dataset Overview: Breast Cancer Wisconsin (Diagnostic)

The **Breast Cancer Wisconsin** dataset is one of the most popular datasets for binary classification tasks in healthcare analytics.  
It contains **569 samples** of cell nuclei features computed from breast mass images.

Each sample includes **30 real-valued features** such as radius, texture, perimeter, area, smoothness, etc., derived from digital images of fine needle aspirates (FNA) of breast masses.

### 🔢 Classes:
- **0 → Malignant (Cancerous)** 🛑  
- **1 → Benign (Non-Cancerous)** ✅  

---

## 🧩 Project Workflow

### 1. Data Loading
The dataset is provided as a Bunch object, similar to a Python dictionary, containing:

- data: feature matrix

- target: output labels (0 or 1)

- feature_names: list of 30 feature names

- target_names: class names (malignant, benign)

### 2. Data Preparation

- Converted dataset to a Pandas DataFrame for analysis:

- Checked for missing values and dataset balance.

- Split dataset into:

  -- 80% training set

  -- 20% testing set

### 3. Feature Standardization

Used StandardScaler to standardize feature values to zero mean and unit variance


➤ This step improves model convergence and training performance.

---

## 🧠 Model Architecture (Neural Network)

Built a simple yet effective feedforward neural network using Keras Sequential API:

Layer	Type	Activation	Output Shape: 

1	Flatten (Input Layer)	—	(30,)

2	Dense (Hidden Layer)	ReLU	20

3	Dense (Output Layer)	Sigmoid	2


#### 🔧 Compilation

- Optimizer: Adam

- Loss: Sparse Categorical Crossentropy

- Metric: Accuracy

---

## 🏋️ Model Training

Model trained for 10 epochs with 10% validation split:

Observed consistent improvement in both training and validation accuracy.

Achieved high accuracy with minimal overfitting.

### 🚀 Results
Model	Technique	Test Accuracy
Neural Network	Dense Layers + Standardization	97%

✅ The model efficiently classifies breast cancer cases with strong predictive accuracy and generalization capability.

---

🧾 Key Learnings

Understanding of Neural Network fundamentals and architecture design.

Importance of data preprocessing and standardization in machine learning.

Application of TensorFlow & Keras for real-world classification problems.

Gained hands-on experience with model evaluation, visualization, and performance tuning.

---

## 🧰 Tech Stack

Programming Language: Python

Libraries: TensorFlow, Keras, NumPy, Pandas, Scikit-learn, Matplotlib

Dataset Source: sklearn.datasets

Environment: Jupyter Notebook / Anaconda

---
