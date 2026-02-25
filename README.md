# 🩺 Explainable COVID-19 Chest X-Ray Classification

## 📌 Project Overview

This project implements a multi-class deep learning model to classify chest X-ray images into:

- COVID-19  
- Viral Pneumonia  
- Normal  

The system is built using **transfer learning with VGG16 (pretrained on ImageNet)** and enhanced with **Grad-CAM visualization** to verify that predictions are based on meaningful lung regions rather than image artifacts.

The focus of this project is not only predictive performance but also model interpretability and reliability.

---

## 🧠 Methodology

### 1️⃣ Data Preprocessing
- Images resized to 224×224
- Grayscale converted to 3 channels
- ImageNet normalization applied
- Light augmentation (rotation and horizontal flip)

### 2️⃣ Model Architecture
- Pretrained VGG16 backbone
- Feature extractor frozen
- Final classifier modified for 3 classes
- Weighted CrossEntropyLoss to address class imbalance

### 3️⃣ Evaluation
- Training and validation accuracy tracking
- Loss curve visualization
- Confusion matrix analysis
- Grad-CAM interpretability analysis

---

## 📊 Results

- Strong validation accuracy on the provided dataset
- High per-class performance
- Minimal confusion between categories
- Grad-CAM confirms attention focused on lung regions

---

## 🔎 Interpretability (Grad-CAM)

Grad-CAM was applied to visualize model attention maps.

The heatmaps show that the model primarily focuses on anatomically relevant lung areas rather than borders, corners, or text markers, increasing confidence in the decision process.

---

## ⚠ Limitations

- The dataset size is relatively small.
- Validation is limited to the provided data split.
- The model is not intended for real-world clinical deployment.

---

## 📌 Conclusion

This project demonstrates a complete deep learning workflow for medical image classification, combining transfer learning with interpretability analysis.

It emphasizes the importance of validating not only performance metrics but also the reasoning behind model predictions.

---

## 📜 Disclaimer

This project is intended for research and educational purposes only.  
It is not approved for medical diagnosis or clinical use.
