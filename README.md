# Self-Supervised Industrial Anomaly Detection using SimCLR and Multi-Scale Feature Learning

<div align="center">

![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)
![PyTorch](https://img.shields.io/badge/PyTorch-Deep%20Learning-red.svg)
![Computer Vision](https://img.shields.io/badge/Computer-Vision-green.svg)
![Self-Supervised Learning](https://img.shields.io/badge/Self-Supervised-Learning-orange.svg)
![Industrial AI](https://img.shields.io/badge/Industrial-Anomaly%20Detection-purple.svg)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)

A PyTorch implementation of **self-supervised industrial anomaly detection** using **SimCLR contrastive learning** and **multi-scale feature extraction** for robust defect detection across multiple industrial datasets.

</div>

---

## Overview

Industrial anomaly detection is essential for automated quality inspection in modern manufacturing. Traditional supervised approaches require large amounts of labeled defective samples, which are expensive and often unavailable.

This project presents a **self-supervised learning framework** based on **SimCLR** that learns meaningful visual representations without requiring defect annotations. The learned features are further enhanced using **multi-scale feature learning**, enabling robust anomaly detection across different industrial domains.

The framework is evaluated on two popular industrial datasets:

- **MVTec AD**
- **BTAD**

---

## Features

- Self-supervised representation learning
- SimCLR contrastive learning framework
- ResNet50 backbone
- Multi-scale feature extraction
- Industrial defect detection
- Cross-domain feature learning
- PyTorch implementation
- Supports MVTec AD and BTAD datasets
- ROC Curve and Confusion Matrix evaluation
- Easily reproducible research pipeline

---

# Pipeline

<p align="center">
<img src="assets/Pipeline.png" width="95%">
</p>

The proposed pipeline consists of:

1. Image preprocessing
2. Data augmentation
3. SimCLR contrastive learning
4. Encoder pretraining
5. Multi-scale feature extraction
6. Feature aggregation
7. Anomaly scoring
8. Performance evaluation

---

# Architecture

<p align="center">
<img src="assets/Architecture.png" width="100%">
</p>

The architecture contains:

- Image preprocessing
- SimCLR augmentation
- ResNet50 encoder
- Projection head
- Contrastive learning (NT-Xent Loss)
- Multi-scale feature learning
- Feature aggregation
- Anomaly scoring
- Evaluation

---

# Repository Structure

```
Self-Supervised-Industrial-Anomaly-Detection/
│
├── assets/
│   ├── Architecture.png
│   ├── Pipeline.png
│
├── docs/
│   ├── DATASET.md
│   ├── INSTALLATION.md
│
├── notebooks/
│   ├── Self_Supervised_Industrial_Anomaly_Detection.ipynb
│
├── outputs/
│   ├── Confusion-Matrix.png
│   ├── ROC-Curve.png
│
├── LICENSE
├── README.md
└── requirements.txt
```

---

# Methodology

## Step 1 — Data Collection

Industrial images are collected from:

- MVTec AD
- BTAD

Both normal and anomalous samples are used for evaluation, while the self-supervised training stage only requires unlabeled images.

---

## Step 2 — Data Augmentation

Two augmented views are generated from every image using:

- Random Crop
- Color Jitter
- Gaussian Blur
- Horizontal Flip
- Random Grayscale

These image pairs are used for contrastive learning.

---

## Step 3 — SimCLR Representation Learning

A ResNet50 encoder extracts image representations.

A projection head maps features into a latent embedding space.

The model is trained using **NT-Xent Contrastive Loss** to maximize similarity between positive pairs while separating different images.

---

## Step 4 — Multi-Scale Feature Learning

After pretraining:

- Feature maps are extracted from multiple scales
- Features are aggregated
- Rich visual representations improve anomaly detection

---

## Step 5 — Anomaly Detection

The learned feature representations are used to distinguish between:

- Normal samples
- Defective samples

The resulting anomaly scores enable accurate defect localization and classification.

---

# Results

The project evaluates performance using:

- ROC Curve
- Confusion Matrix

### ROC Curve

<p align="center">
<img src="outputs/ROC-Curve.png" width="60%">
</p>

---

### Confusion Matrix

<p align="center">
<img src="outputs/Confusion-Matrix.png" width="55%">
</p>

---

# Technologies Used

- Python
- PyTorch
- Torchvision
- NumPy
- OpenCV
- Matplotlib
- Scikit-learn
- PIL
- Google Colab

---

# Datasets

| Dataset | Description |
|----------|-------------|
| MVTec AD | Industrial anomaly detection benchmark containing multiple object and texture categories |
| BTAD | BeanTech Anomaly Detection Dataset for industrial inspection |

See **docs/DATASET.md** for download instructions.

---

# Installation

Detailed installation steps are available in:

```
docs/INSTALLATION.md
```

---

# Applications

- Industrial Inspection
- Smart Manufacturing
- Surface Defect Detection
- Automated Quality Control
- Predictive Maintenance
- Computer Vision Research

---

# Future Improvements

- Vision Transformers (ViT)
- DINOv2 self-supervised learning
- Masked Autoencoders
- Faster inference
- Real-time anomaly localization
- Explainable anomaly detection
- Domain adaptation
- Lightweight deployment on edge devices

---

# Acknowledgements

This work utilizes publicly available datasets and open-source deep learning libraries including:

- PyTorch
- Torchvision
- MVTec AD
- BTAD
- SimCLR

---

# License

This project is released under the MIT License.

---

# Author

**Nauman Ahmed**

AI Engineer | Machine Learning | Deep Learning | Computer Vision | Generative AI

GitHub: https://github.com/Nauman54

LinkedIn: https://linkedin.com/in/naumanahmed254

---

## If you find this project useful, consider giving it a ⭐ on GitHub.
