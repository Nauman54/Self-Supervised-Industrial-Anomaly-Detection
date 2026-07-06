# Installation Guide

This document provides step-by-step instructions for setting up and running the **Self-Supervised Industrial Anomaly Detection using SimCLR and Multi-Scale Feature Learning** project.

---

# System Requirements

Before running the project, ensure your system meets the following requirements.

## Software

- Python 3.10 or later
- Git
- Jupyter Notebook or Google Colab
- pip (Python Package Manager)

## Recommended Hardware

| Component | Recommendation |
|------------|---------------|
| CPU | Intel Core i5 / AMD Ryzen 5 or higher |
| RAM | 8 GB minimum (16 GB recommended) |
| GPU | NVIDIA GPU with CUDA support (optional but recommended) |
| Storage | 5 GB free disk space |

> **Note:** The notebook can also be executed using **Google Colab**, which provides free GPU access.

---

# Clone the Repository

Clone the repository using Git:

```bash
git clone https://github.com/Nauman54/Self-Supervised-Industrial-Anomaly-Detection.git
```

Navigate to the project directory:

```bash
cd Self-Supervised-Industrial-Anomaly-Detection
```

---

# Create a Virtual Environment (Recommended)

### Windows

```bash
python -m venv venv

venv\Scripts\activate
```

### Linux / macOS

```bash
python3 -m venv venv

source venv/bin/activate
```

---

# Install Dependencies

Install all required Python packages using:

```bash
pip install -r requirements.txt
```

---

# Download the Datasets

Download the required datasets manually.

## MVTec AD

https://www.kaggle.com/datasets/thtuan/mvtecad-mvtec-anomaly-detection

## BTAD

https://www.kaggle.com/datasets/thtuan/btad-beantech-anomaly-detection

For detailed information about the datasets, refer to:

```text
docs/DATASET.md
```

---

# Organize the Dataset

Place the downloaded datasets in the following directory structure.

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

# Running the Project

Since this project is implemented as a Jupyter Notebook, open the notebook using Jupyter Notebook, JupyterLab, VS Code, or Google Colab.

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Open:

```text
notebooks/
└── Self_Supervised_Industrial_Anomaly_Detection.ipynb
```

Run all notebook cells sequentially.

---

# Running in Google Colab

The project is fully compatible with Google Colab.

1. Open Google Colab.
2. Upload the notebook located in:

```text
notebooks/Self_Supervised_Industrial_Anomaly_Detection.ipynb
```

3. Upload or mount the datasets.
4. Enable GPU acceleration:

```
Runtime → Change runtime type → GPU
```

5. Run all notebook cells.

---

# Project Workflow

The notebook executes the following pipeline:

```text
Industrial Datasets
        │
        ▼
Image Preprocessing
        │
        ▼
Data Augmentation
        │
        ▼
SimCLR Self-Supervised Learning
        │
        ▼
ResNet50 Feature Extraction
        │
        ▼
Multi-Scale Feature Learning
        │
        ▼
Anomaly Detection
        │
        ▼
Performance Evaluation
```

---

# Output Files

After successful execution, the generated evaluation results are stored in the **outputs/** directory.

Expected outputs include:

- ROC Evaluation
- PRO Curve
- Confusion Matrix
- Score Distribution
- Defect Localization Heatmaps
- AUC Comparison
- Image Preprocessing Visualization

---

# Dependencies

Major libraries used in this project include:

- PyTorch
- Torchvision
- NumPy
- OpenCV
- Scikit-learn
- Matplotlib
- Pandas
- Pillow
- SciPy

All dependencies are listed in:

```text
requirements.txt
```

---

# Troubleshooting

## CUDA Not Available

Check CUDA availability:

```python
import torch

print(torch.cuda.is_available())
```

If CUDA is unavailable, the notebook will automatically use the CPU.

---

## Missing Python Packages

Install missing dependencies:

```bash
pip install -r requirements.txt
```

---

## Dataset Not Found

Ensure the datasets are downloaded and placed in the correct directory structure described above.

---

## Out of Memory

If GPU memory is insufficient:

- Reduce the batch size.
- Restart the runtime.
- Use Google Colab High-RAM (if available).
- Run the notebook on CPU.

---

# Reproducibility

To reproduce the reported results:

1. Clone the repository.
2. Install all dependencies.
3. Download the required datasets.
4. Organize the datasets correctly.
5. Execute every notebook cell in order.
6. Compare the generated evaluation plots with those provided in the **outputs/** directory.

---

# Additional Documentation

For more information, see:

- `README.md` — Project overview and methodology
- `docs/DATASET.md` — Dataset description and download instructions
- `docs/RESULTS.md` — Experimental evaluation and analysis

---

# Support

If you encounter any issues or have suggestions for improving the project, please open an issue on the GitHub repository.

GitHub Repository:

https://github.com/Nauman54/Self-Supervised-Industrial-Anomaly-Detection
