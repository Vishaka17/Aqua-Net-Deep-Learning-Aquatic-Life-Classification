# 🌊 Aqua-Net: Deep Learning for Aquatic Life Classification
### Deep Learning | Computer Vision | CNN | Transfer Learning

Aqua-Net is a deep learning project that applies **Convolutional Neural Networks (CNNs)** to classify aquatic wildlife images into three species:
- Dolphin
- Jellyfish
- Turtle/Tortoise

The project demonstrates how **data augmentation** and **transfer learning** significantly improve model accuracy and generalization in real-world image classification tasks.

---

## 🎯 Problem Statement

Classifying aquatic species from images is challenging due to:
- Variations in lighting and water clarity
- Different image resolutions and backgrounds
- Class imbalance across species

This project aims to build a **robust, scalable CNN model** capable of accurately classifying aquatic life under real-world conditions.

---

## 🧠 Business & Research Motivation

Automated image classification of marine life supports:
- Wildlife conservation
- Population monitoring
- Marine biodiversity research
- Environmental impact assessment

Aqua-Net demonstrates how deep learning can assist researchers and conservationists by reducing manual image labeling efforts.

---

## 📊 Dataset

- Source: Kaggle – Sea Animals Image Dataset
- Original classes: 23 species
- Selected classes:
  - Dolphin
  - Jellyfish
  - Turtle/Tortoise

Images were split into **training, validation, and test sets** and standardized to **224×224** resolution.

---

## 🔍 Exploratory Data Analysis & Preprocessing

Key preprocessing steps:
- Image resizing and normalization
- Pixel intensity analysis
- Noise handling and standardization
- Class distribution analysis

Feature extraction focused on:
- Shape
- Texture
- Visual patterns unique to each species

---

## 🧩 Model Architecture (CNN)

The base CNN architecture includes:
- Convolution layers with filters: 32 → 64 → 128
- Batch Normalization after each convolution
- Max Pooling for dimensionality reduction
- Dense layer with 128 units
- Softmax output layer for multi-class classification

**Optimizer:** Adam  
**Loss Function:** Categorical Cross-Entropy  
**Metric:** Accuracy  

---

## 🔁 Data Augmentation

To reduce overfitting and handle class imbalance:
- Horizontal flipping
- Rotation (±20°)
- Zoom (0.2)

Data augmentation significantly improved generalization on unseen data.

---

## 🚀 Transfer Learning

Transfer learning was applied using **EfficientNetB7 (ImageNet pre-trained)**:
- Used as a feature extractor
- Fine-tuned with EarlyStopping and ModelCheckpoint
- Reduced training time and improved performance

---

## 📈 Model Performance

| Model | Accuracy | Validation Loss |
|-----|---------|----------------|
| Base CNN | 88.70% | 0.3072 |
| CNN + Augmentation | 90.02% | 0.2122 |
| CNN + Transfer Learning | **94.92%** | **0.1835** |

### Key Observations
- Turtle/Tortoise class achieved the highest recall and F1-score
- Transfer learning delivered the best overall performance
- Augmentation reduced overfitting significantly

---

## 📊 Evaluation Metrics

- Confusion Matrix
- Precision, Recall, F1-Score
- Training vs Validation Loss Curves

The final model achieved **high precision and recall across all classes**, demonstrating strong generalization.

---

## ⚠️ Challenges

- GPU availability in cloud environments
- Overfitting in early model versions
- Hyperparameter tuning and training stability

Mitigation strategies included:
- Data augmentation
- Early stopping
- Transfer learning

---

## 🔮 Future Improvements

- Expand dataset with additional species
- Apply real-time inference pipelines
- Deploy as a web or mobile application
- Experiment with other pre-trained architectures (ResNet, MobileNet)

---

## 🛠 Tools & Technologies

- Python
- TensorFlow / Keras
- CNNs & Transfer Learning
- Google Colab (GPU)
- Computer Vision Techniques

---

## 👩‍💻 Author

**Vishaka Sharma**  
Business Analytics | Data Science | Deep Learning
