# 🐶🐱 Dog vs Cat Image Classifier (Using Transfer Learning - MobileNetV2)

A deep learning model built using **Transfer Learning (MobileNetV2)** to classify images of **cats and dogs**.  
This project demonstrates preprocessing, model training, evaluation, and real-time prediction.

---

## 📂 Dataset Overview

- **Training data:** 1,600 images  
- **Testing data:** 401 images  
- Source: [Kaggle - Dogs vs Cats Dataset](https://www.kaggle.com/datasets/samuelcortinhas/dogs-vs-cats)

---

## 🧠 Model Architecture (MobileNetV2-based)

| **Layer (Type)**             | **Output Shape**     | **Parameters**    |
|------------------------------|----------------------|-------------------|
| MobileNetV2 (pre-trained)    | (None, 7, 7, 1280)   | 2,257,984         |
| GlobalAveragePooling2D       | (None, 1280)         | 0                 |
| Dense (2 neurons – output)   | (None, 2)            | 2,562             |
| **Total Parameters**         | —                    | **2,260,546 (8.62 MB)** |
| **Trainable Parameters**     | —                    | **2,562 (10.01 KB)**    |
| **Non-trainable Parameters** | —                    | **2,257,984 (8.61 MB)** |

---

## ⚙️ Model Compilation

```python
model.compile(
    optimizer='adam',
    loss='categorical_crossentropy',
    metrics=['accuracy']
)
```
Optimizer: Adam

Loss Function: Categorical Crossentropy

Metric: Accuracy

---

## 📊 Training the Model
model.fit(x_train, y_train, epochs=5)

Epoch	Accuracy	Loss
1	36.8%	4.11
2	40.7%	0.85
3	55.7%	0.70
4	79.1%	0.56
5	92.2%	0.35

✅ The model achieves ~92% training accuracy in just 5 epochs.

🧾 Evaluation on Test Data
score, acc = model.evaluate(x_test, y_test)
print("Test Loss:", score)
print("Test Accuracy:", acc)


Output:

Test Loss:  0.4923  
Test Accuracy:  0.9251


✔️ Final Test Accuracy: 92.5%

---

## 📈 Results Summary
Model	Technique	Test Accuracy
Baseline CNN	From Scratch	65.3%
MobileNetV2	Transfer Learning	92.5%

---

🧰 Tech Stack

Programming Language: Python

Libraries: TensorFlow, Keras, OpenCV, NumPy, Pandas, Matplotlib, scikit-learn

Model Used: MobileNetV2 (pre-trained on ImageNet)

Environment: Jupyter Notebook / Google Colab

---
