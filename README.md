# SLE-ECA-DCGAN

## 🔍 Overview

**SLE-ECA-DCGAN** is a novel Deep Convolutional Generative Adversarial Network (DCGAN) designed to enhance data augmentation for photovoltaic (PV) panel surface defect detection. This framework addresses common challenges such as limited data availability, class imbalance, and poor image quality by incorporating two key components:

- **Skip-Layer Excitation (SLE):** Enables better feature fusion and detail preservation across network layers.
- **Efficient Channel Attention (ECA):** Improves sensitivity to fine-grained defect features in the discriminator.

Combined with **Wasserstein loss with gradient penalty (WGAN-GP)**, the model achieves more stable training and generates higher-quality, realistic defect images.

## ✨ Key Features

- Redesigned generator with SLE for enhanced multi-scale feature learning.
- Attention-augmented discriminator using lightweight ECA modules.
- Improved training stability and convergence through WGAN-GP.
- Significantly improves data diversity and downstream detection performance.

## 🗂 Dataset

> ⚠️ **Notice:**  
The PV defect image dataset used in this project is currently under confidentiality due to ongoing project restrictions. We plan to release the dataset on this GitHub repository after the confidentiality period ends.

## 📦 Project Structure

```

SLE-ECA-DCGAN/
│
├── models/                 # Generator & Discriminator architecture
├── dataset/                # Placeholder for dataset (to be released)
├── train.py                # Training script
├── utils/                  # Helper functions (e.g., metrics, visualizations)
├── results/                # Sample generated images and training logs
└── README.md               # Project introduction

````

## 🚀 Getting Started

### 1. Environment Setup

```bash
git clone https://github.com/WHU-wangke/SLE-ECA-DCGAN.git
cd SLE-ECA-DCGAN
pip install -r requirements.txt
````

### 2. Training

```bash
python train.py
```

### 3. Visualize Generated Results

Check the `results/` directory for generated image samples and FID score logs.

## 📊 Evaluation

The model is evaluated using Fréchet Inception Distance (FID) and integrated into a downstream YOLOv8s detection pipeline. Compared to standard DCGAN, our method achieves:

* **46.08% FID reduction**
* **Improved mAP in defect detection tasks**

## 📄 Citation

If you use this work in your research, please cite:

```bibtex
@article{wang2025sle,
  title={SLE-ECA-DCGAN: An Enhanced Deep Convolutional GAN for Photovoltaic Panel Surface Defect Image Augmentation},
  author={Ke Wang and Yinxi Liang and Jianqin Qu},
  journal={Sensors},
  year={2025}
}
```





