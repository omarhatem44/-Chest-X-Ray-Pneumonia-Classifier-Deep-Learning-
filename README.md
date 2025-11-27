project:
  name: "Chest X-Ray Pneumonia Classifier — Deep Learning End-to-End Pipeline"
  description: >
    A complete deep learning pipeline for classifying chest X-ray images into NORMAL and 
    PNEUMONIA using a custom Convolutional Neural Network (CNN). 
    Includes full workflow: EDA, preprocessing, class imbalance handling, controlled augmentation, 
    model training, evaluation (confusion matrix + classification report), and modular scripts.

dataset:
  name: "Chest X-Ray Pneumonia Dataset"
  source: "Kaggle (public medical dataset)"
  classes:
    - NORMAL
    - PNEUMONIA
  splits:
    train: "Original dataset split"
    validation: "Original dataset split"
    test: "Original dataset split"

features:
  - "End-to-End ML pipeline"
  - "Custom CNN model"
  - "Balanced training using selective augmentation (NORMAL only)"
  - "Full evaluation with precision/recall/F1-score"
  - "Confusion matrix visualization"
  - "Production-ready modular code structure"
  - "Project organized following ML engineering best practices"

performance:
  final_test_accuracy: 0.8574
  confusion_matrix:
    - [216, 18]
    - [71, 319]
  classification_report:
    NORMAL:
      precision: 0.7526
      recall: 0.9231
      f1_score: 0.8292
    PNEUMONIA:
      precision: 0.9466
      recall: 0.8179
      f1_score: 0.8776

project_structure:
  root:
    - README.md
    - requirements.txt
    - .gitignore
    - src/
    - results/
    - models/
  src:
    - train_cnn_pneumonia.py
    - evaluate_cnn_metrics.py
    - augmentation_normal_only.py
    - eda_pneumonia.py
  results:
    - confusion_matrix_cnn.png
  models: "Empty (no .h5 uploaded due to GitHub size limits)"

setup:
  clone:
    command: |
      git clone https://github.com/<your-username>/pneumonia-xray-classifier.git
      cd pneumonia-xray-classifier
  install_dependencies:
    command: "pip install -r requirements.txt"

training:
  command: "python src/train_cnn_pneumonia.py"
  output:
    - "Trains CNN model"
    - "Saves best model weights locally (cnn_pneumonia_best.h5)"
    - "Applies augmentation to NORMAL only"
    - "Runs validation on val/ split"

evaluation:
  command: "python src/evaluate_cnn_metrics.py"
  outputs:
    - "Confusion matrix"
    - "Classification report"
    - "Overall accuracy"
    - "Saved plot under results/"

future_work:
  - "Add Transfer Learning models (ResNet50, EfficientNet, DenseNet)"
  - "Add Grad-CAM visualization for explainability"
  - "Deploy model using Flask or FastAPI"
  - "Convert model to TFLite for mobile deployment"

author:
  name: "Mohamed Ellabban"
  role: "Machine Learning Engineer | Deep Learning | Medical AI"
  github: "https://github.com/omarhatem44"
  email: "mohamed.ellabban@outlook.com"

license:
  type: "MIT License"
  note: "Free to use for research and educational purposes"
