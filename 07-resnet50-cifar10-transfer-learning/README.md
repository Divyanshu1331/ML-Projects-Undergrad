# 🧠 CIFAR-10 Classification using ResNet50 (Transfer Learning)

This project explores transfer learning using ResNet50 to improves CIFAR-10 classification from ~39% baseline to ~94.86% using ResNet50 transfer learning.

---

## 🔍 Key Result

- Baseline Neural Network: ~39% accuracy  
- ResNet50 (Transfer Learning): **~94.86% accuracy**

---

## 📂 Dataset

- CIFAR-10: 60,000 images (32×32)  
- 10 classes: airplane, automobile, bird, cat, deer, dog, frog, horse, ship, truck  

---

## 🧠 Approach

- Upsampled images to match ResNet50 input size  
- Used ResNet50 pretrained on ImageNet as feature extractor  
- Added fully connected layers with:
  - Batch Normalization  
  - Dropout (0.5)  
- Optimized using RMSprop with low learning rate  

---

## 📊 Performance

- Training Accuracy: ~97.8%  
- Validation Accuracy: ~94.8%  
- Test Accuracy: **~94.86%**

---

## ⚙️ Tech Stack

- Python  
- TensorFlow / Keras  
- OpenCV, NumPy, Pandas  
- Matplotlib  

---

## 📁 Contents

- `cifar10_resnet50.ipynb` — Training and evaluation  
- `README.md` — Project overview  

---

## 🧠 Key Takeaway

Transfer learning dramatically improves performance on small datasets, highlighting the importance of pretrained representations over training from scratch.
