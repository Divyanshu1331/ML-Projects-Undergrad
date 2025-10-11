# 🧠 CIFAR-10 Object Classifier using Transfer Learning (ResNet50)

This project implements an **image classification model** using the **CIFAR-10 dataset**, leveraging **Transfer Learning with ResNet50** for accurate object recognition.  
It demonstrates the complete pipeline — from dataset handling to deep learning model training, evaluation, and prediction.

---

## 📁 Dataset Overview: CIFAR-10

The **CIFAR-10** dataset is a widely used benchmark for object recognition tasks in computer vision.  
It contains **60,000 color images** of size **32×32** pixels, divided into **10 distinct classes**, with **50,000 training** and **10,000 testing** samples.

### 🔢 Classes:
- airplane ✈️  
- automobile 🚗  
- bird 🐦  
- cat 🐱  
- deer 🦌  
- dog 🐶  
- frog 🐸  
- horse 🐴  
- ship 🚢  
- truck 🚚  

Each image belongs to one of these mutually exclusive categories.

---

## 🧩 Project Workflow

### 1. **Data Preparation**
- Mounted Google Drive to access dataset in Google Colab.
- Extracted and read the dataset (`train.zip` and `trainLabels.csv`).
- Loaded images and corresponding labels into memory using OpenCV and Pandas.
- Encoded class labels numerically.
- Split dataset into **80% training** and **20% testing**.
- Scaled pixel values to the range `[0,1]`.

### 2. **Baseline Model**
- Built a simple **Neural Network (Dense layers)** for baseline accuracy.
- Achieved **~39% accuracy** on the test set.

### 3. **Transfer Learning with ResNet50**
- Implemented **ResNet50** (pre-trained on ImageNet) as a feature extractor.
- Used **UpSampling2D** to scale CIFAR-10 images from `32x32` to `256x256` (ResNet50 input size).
- Added custom Dense layers for classification:
  - Batch Normalization  
  - Dropout (0.5) for regularization  
  - ReLU activation for hidden layers  
  - Softmax for output layer (10 classes)
- Optimized using **RMSprop** with a small learning rate (`2e-5`).

### 4. **Training**
- Trained the model for **10 epochs** with `validation_split=0.1`.
- Training accuracy: **97.8%**
- Validation accuracy: **94.8%**

### 5. **Evaluation**
- Evaluated on test set achieving **Test Accuracy ≈ 94.86%**.

### 6. **Prediction**
- Built a predictive system where users can input a new image and get predicted class (e.g., *airplane*, *cat*, *truck*).

---

## 📊 Performance Visualization

The model’s training progress was visualized using Matplotlib:

- **Training vs Validation Loss**
- **Training vs Validation Accuracy**

---

## 🧠 Model Summary (ResNet50-based)

| **Layer Type**           | **Output Shape**   | **Parameters** |
|---------------------------|--------------------|----------------|
| UpSampling2D              | (256, 256, 3)      | 0              |
| ResNet50 (pre-trained)    | —                  | 23,587,712     |
| Flatten                   | —                  | 0              |
| Dense (128, ReLU)         | —                  | 16,512         |
| Dropout (0.5)             | —                  | 0              |
| Dense (64, ReLU)          | —                  | 8,256          |
| Dropout (0.5)             | —                  | 0              |
| Dense (Softmax, 10)       | —                  | 650            |
| **Total Parameters**      | —                  | **23.6M**      |

---

## 🧾 Key Learnings

- Understanding **Transfer Learning** with pre-trained CNNs.  
- Data preprocessing using **OpenCV** and **Pandas**.  
- Model optimization through **Batch Normalization** and **Dropout**.  
- Visualization of model performance using **Matplotlib**.  
- Building an **end-to-end predictive system** for real-world object classification.  

---

## 🧰 Tech Stack

- **Programming Language:** Python  
- **Libraries:** TensorFlow, Keras, OpenCV, NumPy, Pandas, Matplotlib, scikit-learn  
- **Pre-trained Model:** ResNet50 (ImageNet weights)  
- **Environment:** Google Colab  

---

## 🚀 Results

| **Model** | **Technique** | **Test Accuracy** |
|------------|----------------|------------------|
| Baseline Neural Network | Dense layers | 39.2% |
| ResNet50 Transfer Learning | CNN + ResNet50 + Dense layers | **94.86%** |

---

## 📷 Sample Prediction
Enter the path of the Image: Gave the path of an airplane image

Output:

Predicted Class: airplane ✈️
Confidence: 98.9%

---
