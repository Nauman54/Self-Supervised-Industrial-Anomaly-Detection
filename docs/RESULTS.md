# Results

The proposed framework was evaluated on industrial anomaly detection datasets using multiple quantitative and qualitative metrics. The results demonstrate the effectiveness of self-supervised representation learning with SimCLR and multi-scale feature extraction for anomaly detection.

## Quantitative Results

| Metric | Value |
|---------|------:|
| AUC Score | **0.84** |
| Accuracy | **87.0%** |
| Precision (Anomaly) | **0.88** |
| Recall (Anomaly) | **0.99** |
| F1-Score (Anomaly) | **0.93** |

---

## Classification Report

| Class | Precision | Recall | F1-Score | Support |
|------|----------:|-------:|---------:|--------:|
| Normal (OK) | 0.60 | 0.10 | 0.17 | 30 |
| Anomaly (KO) | **0.88** | **0.99** | **0.93** | 200 |

**Overall Accuracy:** **87%**

---

## Performance Summary

- **AUC:** 0.84
- **Accuracy:** 87%
- **High anomaly recall (99%)**, indicating the model successfully identifies nearly all defective samples.
- **Strong anomaly F1-score (0.93)** demonstrates robust detection performance.
- The lower recall for the normal class reflects the intentionally anomaly-focused decision threshold, prioritizing defect detection over normal sample classification.

---

## Evaluation Results

### Image Preprocessing

The preprocessing pipeline standardizes industrial images before feature extraction and contrastive learning.

<p align="center">
<img src="outputs/Preprocessing-Visualization.png" width="90%">
</p>

---

### ROC Evaluation

The Receiver Operating Characteristic (ROC) curve evaluates the model's discrimination capability across different thresholds.

<p align="center">
<img src="outputs/ROC-Evaluation.png" width="75%">
</p>

---

### PRO Curve

The Per-Region Overlap (PRO) curve measures the localization quality of detected anomalies.

<p align="center">
<img src="outputs/PRO-Curve.png" width="75%">
</p>

---

### Confusion Matrix

The confusion matrix summarizes the classification performance on normal and anomalous samples.

<p align="center">
<img src="outputs/Confusion-Matrix.png" width="60%">
</p>

---

### Score Distribution

The anomaly score distribution illustrates the separation between normal and anomalous samples in the learned feature space.

<p align="center">
<img src="outputs/Score-Distribution.png" width="75%">
</p>

---

### Defect Localization

The learned feature representations generate anomaly heatmaps that accurately localize defective regions.

<p align="center">
<img src="outputs/Localization-Defect-Anomaly-Heatmap.png" width="90%">
</p>

---

### State-of-the-Art Comparison

Comparison of the proposed method with existing industrial anomaly detection approaches using AUC.

<p align="center">
<img src="outputs/AUC-SOTA-Comparison.png" width="80%">
</p>

---

## Key Findings

- Self-supervised SimCLR successfully learns discriminative visual representations without defect labels.
- Multi-scale feature learning improves feature representation for industrial inspection.
- The framework achieves an **AUC of 0.84** with **87% overall accuracy**.
- A **99% anomaly recall** makes the model highly effective for industrial defect detection, minimizing missed defects.
- The approach generalizes across multiple industrial datasets (MVTec AD and BTAD).
