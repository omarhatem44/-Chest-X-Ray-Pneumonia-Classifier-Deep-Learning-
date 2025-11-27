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

This repository contains a complete deep learning pipeline for detecting pneumonia from chest X-ray images using a custom-built Convolutional Neural Network (CNN).

The workflow includes EDA, preprocessing, class imbalance handling, controlled augmentation, CNN model training, evaluation (confusion matrix + classification report), and a clean ML engineering folder structure.

---

# 📌 Project Highlights

- End-to-end training pipeline  
- Modular & production-ready code  
- Selective augmentation (NORMAL only)  
- Handles dataset imbalance  
- Clear evaluation metrics  
- Confusion matrix + classification report  
- Organized ML project structure  

---

# 📊 Model Performance

| Metric | Value |
|--------|--------|
| **Test Accuracy** | **85.7%** |
| Precision (NORMAL) | 0.75 |
| Recall (NORMAL) | 0.92 |
| Precision (PNEUMONIA) | 0.94 |
| Recall (PNEUMONIA) | 0.81 |

### Confusion Matrix
[[216, 18],  
 [71, 319]]

---

# 📂 Project Structure

pneumonia-xray-classifier/
│
├── src/
│   ├── train_cnn_pneumonia.py
│   ├── evaluate_cnn_metrics.py
│   ├── augmentation_normal_only.py
│   ├── eda_pneumonia.py
│
├── results/
│   └── confusion_matrix_cnn.png
│
├── models/
│   └── (empty — model weights stored locally)
│
├── requirements.txt
└── README.md

---

# ⚙️ Installation

pip install -r requirements.txt

---

# 🏋️‍♂️ Train the Model

python src/train_cnn_pneumonia.py

Outputs:
- Trained CNN
- Best model saved locally as cnn_pneumonia_best.h5 (not uploaded to repo)

---

# 📈 Evaluate the Model

python src/evaluate_cnn_metrics.py

Outputs:
- Confusion Matrix  
- Precision / Recall / F1-score  
- Visualization saved in results/  

---

# 🚀 Future Improvements

- ResNet50 Transfer Learning
- EfficientNet / DenseNet versions
- Grad-CAM explainability
- TensorFlow Lite export
- API deployment (Flask / FastAPI)

---

# 👨‍💻 Author

Mohamed Ellabban  
Machine Learning Engineer — Deep Learning & Medical AI  

GitHub: https://github.com/omarhatem44  
Email: mohamed.ellabban@outlook.com  

---

# 📜 License  

MIT License — Free for research & educational use.
