# 🐶🐱 Dog vs Cat Classification using MobileNetV2 (Transfer Learning)

This project applies transfer learning using MobileNetV2 to classify images of cats and dogs, and achieves ~92.5% accuracy.

---

## 🔍 Key Result

- Baseline CNN: ~65% accuracy  
- MobileNetV2 (Transfer Learning): **~92.5% accuracy**

---

## 📂 Dataset

- Training: 1,600 images  
- Testing: 401 images  
- Source: Kaggle Dogs vs Cats dataset  

---

## 🧠 Approach

- Used MobileNetV2 pretrained on ImageNet as feature extractor  
- Added classification head with:
  - GlobalAveragePooling  
  - Dense layer (2 classes)  
- Optimized using Adam  
- Trained for 5 epochs  

---

## 📊 Performance

- Final Test Accuracy: **92.5%**
- Rapid convergence with minimal training

---

## ⚙️ Tech Stack

- Python  
- TensorFlow / Keras  
- OpenCV, NumPy, Pandas  
- Matplotlib  

---

## 📁 Contents

- `dog_cat_mobilenetv2.ipynb` — Training and evaluation  
- `README.md` — Project overview  

---

## 🧠 Key Takeaway

Transfer learning significantly improves performance and training efficiency compared to training CNNs from scratch on small datasets.
