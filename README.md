# GLADformer: A Resolution-Aware Linear Agent Transformer with Global Context for Remote Sensing Image Dehazing 🛰️🌫️

[![PyTorch](https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=flat&logo=PyTorch&logoColor=white)](https://pytorch.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

> Welcome to the official code and dataset repository for the paper **GLADformer**. 🚀

---

## 📝 To-Do List / Roadmap

We are continuously updating this repository. Here is our current progress:

- [x] 📊 **Publish the dataset**
- [ ] 💻 **Publish the training code**
- [ ] 📦 **Publish the pre-trained weights**

---
## ⚙️ Environment Preparation

To run the code, you will need **Python 3.11**, **PyTorch 2.6.0**, and **CUDA 12.6**. 

Follow these steps to set up the environment:

**1. Create a new conda environment named `gladformer`：**
```bash
conda create -n gladformer python=3.11 -y
conda activate gladformer
```
**2.Install PyTorch and dependencies**

```bash
pip install torch==2.6.0 torchvision torchaudio
pip install -r requirements.txt
```

---
## 📂 Dataset Preparation

The RSDD dataset for this project has been released! 

Please download the dataset and organize it following the directory structure below. Make sure the ground truth (GT) and hazy images are placed in their respective `train` and `test` folders inside the `data/RSDD/` directory.

```text
data/
└── RSDD/
    ├── train/
    │   ├── GT/          # Ground Truth (clear) images for training
    │   └── hazy/        # Hazy images for training
    └── test/
        ├── GT/          # Ground Truth (clear) images for testing
        └── hazy/        # Hazy images for testing
    RSHaze/
    ├── train/
    │   ├── GT/          
    │   └── hazy/        
    └── test/
        ├── GT/          
        └── hazy/
