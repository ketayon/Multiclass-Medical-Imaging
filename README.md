# 🧪 Model Evaluation Report — Quantum-Enhanced Brain Tumor Classifier

## ✅ Validation Summary

- **Validation Accuracy**: `92.37%`
- **Validation Loss**: `0.8897`
- *(on held-out 10% validation data from training)*

---

## 🔍 Test Set Performance

- **Test Accuracy**: `56.03%`

### 📋 Classification Report

| Class              | Precision | Recall | F1-Score | Support |
|-------------------|-----------|--------|----------|---------|
| **Glioma Tumor**   | 0.85      | 0.24   | 0.37     | 1000    |
| **Meningioma Tumor** | 0.86    | 0.45   | 0.59     | 1000    |
| **No Tumor**       | 0.38      | 1.00   | 0.55     | 1000    |
| **Pituitary Tumor**| 0.97      | 0.55   | 0.70     | 1000    |

- **Macro Avg**: Precision: `0.76` | Recall: `0.56` | F1: `0.55`
- **Weighted Avg**: Precision: `0.76` | Recall: `0.56` | F1: `0.55`

---

## 📊 Confusion Matrix (Insights)

- Glioma and Meningioma are **often confused** or misclassified as "No Tumor".
- "No Tumor" is overpredicted — this class gets **very high recall (1.00)**.
- "Pituitary Tumor" is the best balanced — high precision and decent recall.

---

## 📈 Observations

- Model **fits training/validation well**, but **fails to generalize** to the test set.
- Validation accuracy is misleading — possibly due to easy validation samples or minor data leakage.

---

## ⚠️ Problems Detected

1. **Low recall** for `glioma` and `meningioma` → model is biased toward safer (easier) predictions.
2. **Overconfident on 'no tumor'** — imbalance or oversensitivity to absence of tumor features.
3. **Quantum layer generalization** may be poor — it overfits but doesn't extrapolate.

---

## ✅ Recommendations

### 🔧 Improve Data & Model Generalization
- Add **more data augmentations** (zoom, contrast, cutout, color jitter).
- Use **Stratified Split** to ensure fair class representation in validation/test sets.
- Reduce model complexity or use **dropout regularization** in dense layers.

### 🧠 Improve Learning for Minority Classes
- Switch to **Focal Loss** (instead of NLLLoss or Label Smoothing) to penalize easy/no-tumor predictions.
- Use **class rebalancing** with SMOTE or further oversampling of under-represented classes.
- Try a **per-class accuracy plot** to visualize imbalance effects over epochs.

### 🔄 Try Hybrid or Ensemble Models
- Ensemble predictions from:
  - This quantum model
  - A classical CNN baseline
  - A pure ResNet model (no quantum layer)

---

## 📌 Final Notes

The model shows promising **validation accuracy**, but needs refinement in:
- Generalization to unseen test data
- Balancing predictions across classes

With further tuning of quantum layer regularization and class-aware loss functions, test accuracy > 80% is realistic.

---

🔁 **Next Step**: Would you like to apply focal loss or visualize per-class training performance?
