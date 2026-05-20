# ECG Arrhythmia Classification with 1D CNN

Deep learning pipeline for ECG heartbeat classification using the MIT-BIH Arrhythmia Database from PhysioNet.

---

## Overview

This project implements a 1D Convolutional Neural Network (1D CNN) for biomedical time-series classification using ECG recordings.

The model classifies heartbeat segments into:
- Normal beats
- Premature Ventricular Contractions (PVC)

The project focuses on realistic evaluation of ECG classification performance using leave-one-record-out cross-validation across unseen ECG recordings.

---

## Dataset

- Dataset: MIT-BIH Arrhythmia Database
- Source: PhysioNet
- Signal type: ECG
- Sampling frequency: 360 Hz

ECG records are automatically downloaded using the WFDB Python package.

---

## Methods

### Preprocessing
- Extracted heartbeat-centered ECG windows
- Per-beat normalization
- Selected Normal (N) and PVC (V) annotations

### Deep Learning Model
- 1D Convolutional Neural Network (1D CNN)
- TensorFlow / Keras implementation
- Binary heartbeat classification

### Evaluation
- Leave-One-Record-Out cross-validation
- Evaluation on unseen ECG recordings
- Metrics:
  - Accuracy
  - Precision
  - Recall
  - F1-score
  - Confusion matrix

---

## Why Leave-One-Record-Out?

Random beat-level splitting can introduce data leakage because beats from the same ECG recording may appear in both training and testing sets.

This project evaluates the model on completely unseen ECG records to better assess generalisation performance in biomedical signal classification.

---

## Results

Example overall performance:

- Mean accuracy: ~91%
- Strong PVC detection recall
- Performance variation across ECG records highlights inter-patient variability in biomedical data

---

## Technologies

- Python
- NumPy
- Pandas
- Matplotlib
- WFDB
- TensorFlow / Keras
- scikit-learn

---

## Repository Structure

```text
ECG-Arrhythmia-Classification-1D-CNN/
│
├── README.md
├── ECG_Deep_Learning_PhysioNet.ipynb
├── requirements.txt
├── .gitignore
│
└── results/
    ├── accuracy_plot.png
    └── confusion_matrix.png
```

---

## Key Learning Outcomes

- Biomedical time-series preprocessing
- ECG heartbeat segmentation
- Deep learning for physiological signals
- Cross-validation for grouped biomedical data
- Handling class imbalance in healthcare datasets
- Preventing data leakage in machine learning workflows

---

## Author

Elham ShabaniVaraki
Biomedical Engineer (PhD)
