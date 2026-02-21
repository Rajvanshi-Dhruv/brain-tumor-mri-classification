# 🧠 Brain Tumor MRI Classification using EfficientNet & Vision Transformer

---

## 📌 Project Overview

This project presents a deep learning–based approach for multi-class brain tumor classification using MRI images. The objective is to automatically classify brain scans into four categories:

* **Glioma**
* **Meningioma**
* **Pituitary Tumor**
* **No Tumor**

By leveraging transfer learning and transformer-based architectures, this model aims to assist in automated medical image analysis and early tumor detection.

---

## 📂 Dataset

**Source:**
Kaggle – Brain Tumor MRI Dataset
[https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset/data](https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset/data)

### Dataset Structure

### 🔹 Training Set (5,600 images)

* Glioma – 1,400 images
* Meningioma – 1,400 images
* Pituitary – 1,400 images
* No Tumor – 1,400 images

### 🔹 Testing Set (1,600 images)

* Glioma – 400 images
* Meningioma – 400 images
* Pituitary – 400 images
* No Tumor – 400 images

The dataset is fully balanced across all classes, ensuring fair evaluation.

---

## 🧠 Model Architectures

Two deep learning architectures were implemented and evaluated.

---

### 1️⃣ EfficientNet (Transfer Learning)

* Pretrained on ImageNet
* Fine-tuned for 4-class classification
* Custom dense layers added
* Softmax activation for final classification

EfficientNet uses compound scaling to balance network depth, width, and resolution, making it computationally efficient and powerful.

---

### 2️⃣ Vision Transformer (ViT)

* Transformer-based architecture for image classification
* Splits images into patches instead of using convolutional filters
* Fine-tuned for medical image classification

ViT captures global contextual relationships between image regions.

---

## ⚙️ Data Preprocessing

* Image resizing to model-specific input dimensions
* Pixel normalization (scaled between 0–1)
* Conversion to appropriate input format
* Data augmentation applied:

  * Rotation
  * Horizontal flipping
  * Zoom augmentation
* Train-validation split during training

---

## 🏋️ Training Configuration

* **Loss Function:** Categorical Cross-Entropy
* **Optimizer:** Adam
* **Evaluation Metrics:** Accuracy, F1 Score
* **Callbacks Used:**

  * EarlyStopping (to prevent overfitting)
  * ModelCheckpoint (to save best model)

---

## 📊 Model Performance

### ✅ Final Test Results

* **Test Accuracy:** 94.05%
* **Test F1 Score:** 94.03%

### 📈 Training Behavior

* Training accuracy converged to ~99%
* Validation accuracy stabilized between 94–96%
* Small generalization gap (~3–4%), indicating controlled overfitting

---

## 🔍 Confusion Matrix Analysis

The confusion matrix shows strong classification performance across all classes.

### Key Observations:

* High correct classification rates for all tumor types
* Minor confusion observed between:

  * Glioma ↔ Meningioma
  * Pituitary ↔ No Tumor
* Balanced precision and recall across all categories

The model demonstrates robust and reliable multi-class performance.

---

## 📊 Evaluation Metrics Used

* Confusion Matrix
* Classification Report (Precision, Recall, F1 Score)
* Training & Validation Accuracy Curves
* Training & Validation F1 Score Curves

---

## 💾 Model Saving

* Trained models saved in `.h5` format
* Ready for further fine-tuning or deployment

---

## 🛠️ Technologies Used

* Python
* TensorFlow / Keras
* OpenCV
* NumPy
* Matplotlib
* Seaborn
---

## 📌 Conclusion

This project demonstrates the effectiveness of modern deep learning architectures for medical image classification. With a balanced dataset and strong performance metrics, the model provides a solid baseline for automated brain tumor detection using MRI scans.

---
