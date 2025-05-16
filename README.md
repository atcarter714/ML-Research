# 🧪 ML-Research: Experiments in Machine Learning & AI

Welcome to **ML-Research**, a public repository of research-grade machine learning experiments, prototypes, and conceptual studies.  
This repo is designed as a **sandbox for testing new ideas**, validating theories, and producing reproducible results across various ML domains.

---

## 🔬 Project Goals

- 📚 Document machine learning experiments with clarity and rigor
- 🧠 Explore new model designs and architectural modifications
- ⚙️ Evaluate practical and theoretical performance tradeoffs
- 📈 Provide reproducible and well-structured notebooks for community use

---

## 📁 Current Experiments

### `mnist_cal_baseline.ipynb`  
> **Baseline CNN + Evaluation Framework for Curve Adjustment Layers (CALs)**

This notebook implements a clean, performant convolutional neural network (CNN) for the MNIST digit classification problem, achieving **~99% accuracy** with minimal complexity.

🎯 **Purpose**: Establish a **control model** for upcoming experiments with **Curve Adjustment Layers (CALs)** — custom neural units that deform intermediate activations via learnable curves to improve convergence and generalization.

#### 🔍 Features:
- ✅ Strong MNIST baseline (~99% acc)
- 🧱 Modular architecture (ideal for insertion of CALs or custom layers)
- 📦 Manual + automatic normalization support
- 📈 Loss curve and batch-wise evaluation visualizations
- 🧪 Ready for ablation studies and augmentation experiments

---

## **Structure**

📂 ML-Research/
> ├── mnist_notebook_00.ipynb     # Baseline CNN with eval and plotting
> ├── README.md                   # Readme file (You're here)
> └── data/                       # Downloaded datasets (ignored via .gitignore)
> └── models/                     # Folder to store models


## 📦 Dependencies

All experiments use **Python ≥3.12** and are tested with:

```bash
pip install torch torchvision matplotlib
```

🔖 License
This repository is open-sourced under the MIT License.
