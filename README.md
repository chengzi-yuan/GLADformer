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
