# Flower Species Image Classification using Transfer Learning

## 🌼 Overview

This project builds a deep learning classifier using Convolutional Neural Networks (CNNs) to accurately identify five types of flowers: **daisy, dandelion, rose, sunflower, and tulip**. It applies **transfer learning** to fine-tune a pre-trained CNN (such as ResNet50 or VGG16) using the [Flowers Recognition dataset](https://www.kaggle.com/datasets/alxmamaev/flowers-recognition).

---

## 📁 Dataset

- **Source**: [Kaggle - Flowers Recognition](https://www.kaggle.com/datasets/alxmamaev/flowers-recognition)
- **Total Images**: ~4,317
- **Classes**: `daisy`, `dandelion`, `rose`, `sunflower`, `tulip`
- **Split**: 75% training / 25% testing

After downloading and extracting the dataset, ensure images are sorted into class-wise directories.

---

## 🔍 Methodology

### Step 1: Data Preparation

- Images resized to 224x224
- Normalization applied
- Labels encoded as integers (e.g., Daisy → 0, Rose → 1, etc.)
- Dataset split into training and validation sets (75/25 split)

### Step 2: Model Selection

We use **transfer learning** by importing pre-trained CNNs trained on ImageNet. Supported models include:

- ResNet50
- VGG16
- MobileNetV2
- InceptionV3

### Step 3: Transfer Learning

Using **TensorFlow** or **PyTorch**:

- Load the pre-trained model (excluding the top layer)
- Freeze the base layers
- Add a new dense classifier head (5 units with softmax)
- Train for ~20 epochs using Adam or SGD optimizer

### Step 4: Evaluation

- Evaluate model on the test set
- Report:
  - Accuracy
  - Precision
  - Recall
  - F1-score
- Visualize:
  - Confusion Matrix
  - Sample Predictions

---

## ✅ Results

| Metric      | Value (Example) |
|-------------|-----------------|
| Accuracy    | 91.4%           |
| Precision   | 90.7%           |
| Recall      | 90.2%           |
| F1-Score    | 90.4%           |

> Final results may vary based on model and hyperparameter tuning.

---

## 🛠️ Setup Instructions

1. Clone the repo:
   ```bash
   git clone https://github.com/yourusername/flower-classifier-cnn.git
   cd flower-classifier-cnn
