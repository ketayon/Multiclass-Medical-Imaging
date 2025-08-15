# 🧪 Model Evaluation Report — Quantum-Enhanced Brain Tumor Classifier
## Overview

#### The model supports multiclass classification of brain MRI scans using a hybrid quantum-classical model.
#### Can use the pretrained 4-class model (glioma, meningioma, no tumor, pituitary) or train your own multiclass model with any #### number of classes by uploading a dataset.

#### This feature follows the hybrid ResNet18 + quantum-inspired head approach from https://arxiv.org/pdf/2505.01735.

## ✅ Validation Summary

- **Validation Accuracy**: `98.62%`
- **Validation Loss**: `0.8897`


### 📋 Classification Report

| Class              | Precision | Recall | F1-Score | Support |
|----------------------|-----------|--------|----------|-------|
| **Glioma Tumor**     | 0.99      | 0.99   | 0.99     | 202   |
| **Meningioma Tumor** | 0.99      | 0.96   | 0.98     | 192   |
| **Pituitary Tumor**  | 0.97      | 1.00   | 0.99     | 212   |
|  **No Tumor**        | 1.00      | 0.99   | 0.70     | 194   |

- **Macro Avg**: Precision: `0.99` | Recall: `0.99` | F1: `0.99`
- **Weighted Avg**: Precision: `0.99` | Recall: `0.99` | F1: `0.99`
