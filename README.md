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

### `mnist_notebook_00.ipynb`  
> **Minimalist CNN for General-Purpose Experimentation**

This notebook implements a clean, performant convolutional neural network (CNN) for the MNIST digit classification problem, achieving **~99% accuracy** with minimal complexity.

#### 🔍 Features:
- ✅ Solid MNIST benchmark (~98.9–99.0% test acc)
- 🧩 Modular design for easy layer or logic injection
- ➕ Optional integration of synthetic data via included mixing cell
- 📉 Loss curves and batch-wise metrics for quick validation cycles
- 🧪 Ideal for rapid iteration and reproducible research


---

### `mnist_synthetic_00.ipynb`  
> **Houdini-Generated Synthetic Dataset Exploration**

Explores a procedurally generated digit dataset created in Houdini and exported for ML purposes.

🧪 **Purpose**: Measure impact of synthesized training data on generalization accuracy.

📊 **Findings**: Adding ~40,960 images (~41% of training data) improved test accuracy to ~99.1%, compared to ~98.9% with MNIST-only training.

---


## 🏗 Houdini Data Synthesis Pipeline

Scene: `./houdini/digit_gen_v02.hip`

### Overview:
- Renders **64 frames** of **8×8 digit sprite sheets** to `$HIP/render`
- Cuts them into **28×28 grayscale images** using compositing + TOPs
- Outputs to `$HIP/output/{0..9}` folder structure for label consistency

This procedural pipeline enables data generation in low-data domains and can be adapted to RGB, animation, 3D points, textures, etc.

---

## 💾 Models

- `mnist_cnn.pth` — Trained on MNIST only (5 epochs)
- `mnist_cnn_01.pth` — Trained on MNIST only (15 epochs)
- `mnist_cnn_02.pth` — Trained on MNIST + synthetic digits (enhanced result)

---

## 📦 Dependencies

All experiments use **Python ≥3.12** and are tested with:

```bash
pip install torch torchvision matplotlib
```

([Get Torch Here](https://pytorch.org/get-started/locally/))

🔖 License
This repository is open-sourced under the MIT License.
