# Datasets

This project is evaluated on two widely used industrial anomaly detection datasets: **MVTec AD** and **BTAD (BeanTech Anomaly Detection Dataset)**. These datasets provide a diverse collection of normal and defective industrial images, making them suitable benchmarks for evaluating self-supervised anomaly detection models.

---

# Dataset Overview

| Dataset | Domain | Categories | Ground Truth | Purpose |
|----------|--------|------------|--------------|---------|
| MVTec AD | Industrial Inspection | 15 Categories | Pixel-level masks | Image-level & pixel-level anomaly detection |
| BTAD | Industrial Inspection | 3 Product Categories | Pixel-level masks | Cross-domain industrial anomaly detection |

---

# 1. MVTec AD (MVTec Anomaly Detection)

## Description

The **MVTec Anomaly Detection (MVTec AD)** dataset is one of the most widely used benchmarks for unsupervised industrial anomaly detection. It contains high-resolution images of various industrial objects and textures with multiple defect types.

The dataset provides:

- Defect-free training images
- Normal and defective testing images
- Pixel-level ground truth annotations for anomaly localization

It is designed to evaluate both image-level anomaly detection and pixel-level defect localization. The dataset contains over **5,000 high-resolution images** across **15 object and texture categories**. :contentReference[oaicite:0]{index=0}

---

## Categories

### Object Categories

- Bottle
- Cable
- Capsule
- Hazelnut
- Metal Nut
- Pill
- Screw
- Toothbrush
- Transistor
- Zipper

### Texture Categories

- Carpet
- Grid
- Leather
- Tile
- Wood

---

## Download

Kaggle Mirror:

https://www.kaggle.com/datasets/thtuan/mvtecad-mvtec-anomaly-detection

Official Dataset:

https://www.mvtec.com/research-teaching/datasets/mvtec-ad

---

# 2. BTAD (BeanTech Anomaly Detection Dataset)

## Description

The **BeanTech Anomaly Detection (BTAD)** dataset is a real-world industrial inspection benchmark developed for evaluating anomaly detection methods under practical manufacturing conditions.

The dataset contains multiple industrial products with both normal and defective samples, together with pixel-level annotations for anomaly localization.

Compared to MVTec AD, BTAD provides a complementary benchmark for evaluating the robustness and generalization capability of anomaly detection models across different industrial domains.

---

## Product Categories

The dataset contains three industrial product categories:

- Product 01
- Product 02
- Product 03

Each category includes:

- Normal training images
- Normal testing images
- Defective testing images
- Pixel-level defect masks

---

## Download

Kaggle:

https://www.kaggle.com/datasets/thtuan/btad-beantech-anomaly-detection

---

# Dataset Directory Structure

After downloading, organize the datasets as follows:

```text
datasets/
│
├── mvtec_anomaly_detection/
│   ├── bottle/
│   ├── cable/
│   ├── capsule/
│   ├── carpet/
│   ├── grid/
│   ├── hazelnut/
│   ├── leather/
│   ├── metal_nut/
│   ├── pill/
│   ├── screw/
│   ├── tile/
│   ├── toothbrush/
│   ├── transistor/
│   ├── wood/
│   └── zipper/
│
└── BTAD/
    ├── 01/
    ├── 02/
    └── 03/
```

---

# Dataset Usage

The datasets are utilized in different stages of the proposed framework:

| Stage | Purpose |
|--------|---------|
| Data Preprocessing | Image normalization and resizing |
| Self-Supervised Learning | SimCLR contrastive representation learning |
| Feature Extraction | Multi-scale feature representation |
| Model Evaluation | Image-level anomaly detection |
| Defect Localization | Pixel-level anomaly localization |

---

# Evaluation Metrics

The proposed framework is evaluated using multiple quantitative and qualitative metrics:

- Area Under the ROC Curve (AUC)
- Receiver Operating Characteristic (ROC)
- Per-Region Overlap (PRO)
- Precision
- Recall
- F1-Score
- Confusion Matrix
- Anomaly Score Distribution
- Defect Localization Heatmaps

---

# Notes

- The datasets are **not included** in this repository due to their size and licensing.
- Please download the datasets separately using the links provided above.
- Ensure that the dataset directory structure matches the format shown in this document before running the notebook.

---

# References

1. Bergmann, P., Fauser, M., Sattlegger, D., & Steger, C. **MVTec AD: A Comprehensive Real-World Dataset for Unsupervised Anomaly Detection.** International Journal of Computer Vision (IJCV), 2021. :contentReference[oaicite:1]{index=1}

2. Mishra, P., Verk, R., Fornasier, D., Piciarelli, C., & Foresti, G. L. **VT-ADL: A Vision Transformer Network for Image Anomaly Detection and Localization.** (Introduces and evaluates BTAD as an industrial benchmark.)
