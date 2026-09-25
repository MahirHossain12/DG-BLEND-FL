# DG-BLEND: Dynamic Global-Local Foundation Model Fusion

This repository contains the official implementation of **DG-BLEND**, a novel framework for Federated Learning (FL) that enables dynamic fusion of foundation models without the need for additional parameters or complex metadata.

## 🚀 Overview
DG-BLEND addresses the challenge of integrating large-scale Vision-Language Models (VLMs) into decentralized federated environments. By utilizing an entropy-based, divergence-aware scaling mechanism, DG-BLEND achieves optimal alignment between local client updates and global foundation model knowledge.

**Key Contributions:**
*   **Zero-Parameter Fusion:** Our method improves convergence without adding any learnable parameters or storage overhead.
*   **Dynamic Scaling:** Automatically adapts client influence based on local model divergence.
*   **Privacy-Preserving:** Operates entirely within the standard FL loop without requiring extra metadata or client-side communication headers.

## 🛠️ Getting Started

### Prerequisites
*   Python 3.9+
*   PyTorch 2.0+
*   `requirements.txt` (install with `pip install -r requirements.txt`)

### Installation
```bash
git clone [https://github.com/YourUsername/DG-BLEND-FL.git](https://github.com/YourUsername/DG-BLEND-FL.git)
cd DG-BLEND-FL
pip install -r requirements.txt

```

### Running an Experiment

We provide a simple script to run the base training loop:

```bash
python train.py --config configs/cifar10_dirichlet_0.5.yaml --epochs 100

```

## 📊 Performance

| Method | Accuracy (Avg) | Overhead (Params) |
| --- | --- | --- |
| **FedAvg** | 78.4% | - |
| **FedPer** | 81.2% | +0.5M |
| **DG-BLEND** | **85.6%** | **0** |

*(Replace the table above with your actual experimental results.)*

## 📁 Repository Structure

* `configs/`: Hyperparameter settings for different heterogeneity levels.
* `models/`: Core definition of the DG-BLEND fusion logic.
* `utils/`: Entropy calculation and divergence metrics.
* `data/`: Scripts for local data partitioning.

## 📝 Citation

If you use this work in your research, please cite our paper:

```bibtex
@article{2026DGBLEND,
  title={DG-BLEND: Dynamic Global-Local Foundation Model Fusion for Federated Learning},
  author={XXXXXX},
  journal={arXiv preprint arXiv:XXXX.XXXXX},
  year={2026}
}

```

## 📄 License

This project is licensed under the **MIT License**.

```
