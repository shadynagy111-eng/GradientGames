# GradientGames
Gradient Games: High-performance stress test for next-gen optimizers. Moving beyond AdamW, we benchmark Matrix-Aware (Muon), Variance-Reduced (MARS), and Sign-based (Lion) methods. This suite evaluates spectral health, rank collapse, and the Pareto frontier of accuracy vs. wall-clock time across Transformers and CNNs. The future of SOTA training.

This is a comprehensive, professional `README.md` designed to make the repository look like a high-level research project. It is structured to guide students through the "Stress Test" while providing clear documentation for external visitors.

---

# 🏆 The Gradient Games: Benchmarking Adaptive vs. Inertial vs. Matrix-Aware Optimizers

## 📌 Project Overview

While **AdamW** is the industry standard, it treats neural network weights as a flat list of numbers. Recent breakthroughs like **Muon** and **MARS** treat weights as structured matrices, exploiting the underlying differential geometry of the network to achieve faster, more stable convergence.

**The Gradient Games** is a benchmarking suite designed to determine if these mathematically complex "New Wave" optimizers are ready for general-purpose use or if they are specialized tools limited to large-scale training.

---

## ⚡ The Lineup

| Optimizer | Paradigm | Core Mechanism | Best For |
| --- | --- | --- | --- |
| **AdamW** | Adaptive | Second-moment gradient scaling | Universal Baseline |
| **Lion** | Sign-based | Symbolic discovery via sign momentum | Memory-efficient LLMs |
| **Muon** | **Matrix-Aware** | Newton-Schulz Orthogonalization | Fast SOTA Training |
| **MARS** | **Var-Reduced** | Recursive Momentum Correction | High-variance datasets |

---

## 🚀 Key Features

* **Spectral Health Monitoring:** Real-time tracking of singular value distributions and stable rank to detect **rank collapse**.
* **The Pareto Frontier:** Automated plotting of Final Accuracy vs. GPU Wall-Clock Time.
* **Hyperparameter Robustness Audit:** Integrated grid-search scripts for learning rate stability analysis.
* **Multi-Geometry Benchmarking:** Support for Vision (CNNs/ViT) and Language (Small GPT).

---

## 🏗️ Getting Started

### 1. Installation

```bash
git clone https://github.com/YourUsername/GradientGames.git
cd GradientGames
pip install -r requirements.txt

```

### 2. Running a Benchmark

To run the standard "Tournament" on CIFAR-100:

```bash
python run_benchmark.py --dataset cifar100 --optimizers muon adamw lion --epochs 50

```

---

## 🔬 Implementation Details

### Muon (Newton-Schulz)

Muon applies an orthonormal update to 2D parameters. The core update follows the iterative refinement:



This ensures the update matrix remains on the Stiefel manifold, maximizing the "expressive energy" of the gradient.

### MARS (Recursive Momentum)

MARS addresses the noise in stochastic gradients by using a variance-reduced recursive update, theoretically providing a smoother descent path on complex loss landscapes.

---

## 📊 Deliverables & Visualization

* **Opti-Arena Dashboard:** Interactive W&B/Streamlit dashboard for live convergence maps.
* **Spectral Footprint Report:** Detailed analysis of weight manifold geometry during training.
* **Recommendation Matrix:** A decision-making guide for hardware-to-optimizer mapping.

---

## 🤝 Contributing

This is an open-source "Stress Test." We welcome contributions in the form of new optimizers, more complex datasets, or CUDA kernel optimizations for the Newton-Schulz steps.

---

## 📜 References

* *Jordan et al. (2024)* - Muon: An optimizer for hidden layers.
* *Zheng et al. (2024)* - MARS: Unleashing the Power of Variance Reduction.
* *Chen et al. (2023)* - Lion: Symbolic Discovery of Optimization Algorithms.

---
