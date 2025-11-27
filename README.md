---
project:
  name: "Chest X-Ray Pneumonia Classifier — Deep Learning End-to-End Pipeline"
  author: "Mohamed Ellabban"
  role: "Machine Learning Engineer | Medical AI"
  email: "mohamed.ellabban@outlook.com"
  github: "https://github.com/omarhatem44"

dataset:
  source: "Kaggle Chest X-Ray Pneumonia Dataset"
  classes:
    - NORMAL
    - PNEUMONIA

performance:
  test_accuracy: 0.8574
  confusion_matrix:
    - [216, 18]
    - [71, 319]

license: "MIT License"
---

# 🧠 Chest X-Ray Pneumonia Classifier  
### ⚡ Deep Learning End-to-End Pipeline (CNN Baseline Model)

This repository contains a complete deep learning pipeline for detecting **pneumonia** from **chest X-ray images** using a custom-built **Convolutional Neural Network (CNN)**.

The workflow includes EDA, preprocessing, class imbalance handling, controlled augmentation, CNN model training, evaluation (confusion matrix + classification report), and a clean ML engineering folder structure.

---

# 📌 Project Highlights

### 🔹 End-to-End Machine Learning Pipeline
- Modular scripts  
- Reproducible workflow  
- Organized folder structure  

### 🔹 Medical Imaging Focus
- Kaggle pneumonia dataset  
- Targeted augmentation for NORMAL class  
- Handles heavy imbalance  

### 🔹 Model Performance
| Metric | Value |
|--------|--------|
| **Test Accuracy** | **85.7%** |
| Precision (NORMAL) | 0.75 |
| Recall (NORMAL) | 0.92 |
| Precision (PNEUMONIA) | 0.94 |
| Recall (PNEUMONIA) | 0.81 |

### 🔹 Confusion Matrix
[[216, 18],
[ 71, 319]]

---

# 📂 **Project Structure**

pneumonia-xray-classifier/
│
├── src/
│ ├── train_cnn_pneumonia.py
│ ├── evaluate_cnn_metrics.py
│ ├── augmentation_normal_only.py
│ ├── eda_pneumonia.py
│
├── results/
│ └── confusion_matrix_cnn.png
│
├── models/ # empty (weights stored locally only)
│
├── requirements.txt
└── README.md

---

# ⚙️ **Installation**

```bash
pip install -r requirements.txt


🏋️‍♂️ Train the Model
python src/train_cnn_pneumonia.py
This script:

Loads & preprocesses data

Applies augmentation to NORMAL only

Trains CNN

Saves best weights as:
This script:

Loads & preprocesses data

Applies augmentation to NORMAL only

Trains CNN

Saves best weights as:
cnn_pneumonia_best.h5  (not included in repo)
📈 Evaluate the Model

python src/evaluate_cnn_metrics.py

