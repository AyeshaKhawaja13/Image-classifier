# 🧠 Image Classifier using Transfer Learning (MobileNetV2) on CIFAR-10

This project implements an **image classification model** using **Transfer Learning** with **MobileNetV2**, trained on the **CIFAR-10 dataset**.  
It demonstrates modern deep learning workflows such as **data augmentation**, **fine-tuning**, and **performance visualization** using **TensorFlow and Keras**.

---

## 🚀 Project Overview

The goal of this project is to train a robust image classifier capable of recognizing **10 object categories**:
> airplane, automobile, bird, cat, deer, dog, frog, horse, ship, truck

Instead of training from scratch, this model uses a **pretrained MobileNetV2** (trained on ImageNet) as a **feature extractor**.  
This saves computation time and improves accuracy even with limited data.

---

## 🧩 Key Features

✅ **Transfer Learning** with `MobileNetV2` pretrained on ImageNet  
✅ **Data Augmentation** (RandomFlip, RandomRotation, RandomZoom)  
✅ **Fine-tuning** of top layers for improved accuracy  
✅ **Visualization** of training curves and predictions  
✅ **Model saving** for reuse or deployment  

---

## 📦 Dataset

**CIFAR-10 Dataset**  
- 60,000 color images (32×32 pixels)  
- 10 classes (6,000 images per class)  
- Automatically loaded via `keras.datasets.cifar10.load_data()`

---

## ⚙️ Model Architecture

1. **Input** → CIFAR-10 image (32×32×3)  
2. **Upsampling** → Resize to (96×96×3) for MobileNetV2  
3. **Data Augmentation** → Random flips, rotations, zooms  
4. **Feature Extractor** → Frozen MobileNetV2 base  
5. **Classifier Head** → Dense(256, relu) + Dropout + Dense(10, softmax)  

---

## 🧑‍💻 Training Details

- Optimizer: `Adam`  
- Loss: `Sparse Categorical Crossentropy`  
- Initial Learning Rate: `1e-3` (for frozen base)  
- Fine-tuning Learning Rate: `1e-5`  
- Epochs: 12 (initial) + 6 (fine-tuning)  
- Validation Split: 15%

---

## 📊 Results

- **Training Accuracy:** ~90%+ after fine-tuning (depends on GPU/time)
- **Test Accuracy:** Around **85–88%** on CIFAR-10 test data
- Displays sample predictions and training/validation accuracy graphs.

---

## 🖼️ Example Output

### 🧩 Training/Validation Accuracy Graph:
Shows smooth learning progress across epochs.

### 🐱 Test Predictions:
Displays a 5×5 grid of CIFAR-10 test images with predicted vs. true labels.

---

## 💾 Model Saving

The trained model is saved as:
Image Classifier

