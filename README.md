# GLADformer: A Resolution-Aware Linear Agent Transformer with Global Context for Remote Sensing Image Dehazing

[![PyTorch](https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=flat&logo=PyTorch&logoColor=white)](https://pytorch.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Data](https://img.shields.io/badge/Data-BaiduPan-brightgreen.svg)](https://pan.baidu.com/s/1-lSjalsgpFOWP_6UFxTPMA?pwd=glad)

> Welcome to the official code and dataset repository for the paper **GLADformer**. 

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
**2. Install PyTorch and dependencies：**

```bash
pip install torch==2.6.0 torchvision torchaudio
pip install -r requirements.txt
```

---
## 📂 Dataset Preparation

The RSDD dataset for this project has been released! 

**The dataset we used can be downloaded here：**
Thanks to the contributors of these datasets for their outstanding work！
[**RSHaze**](https://pan.baidu.com/s/1-lSjalsgpFOWP_6UFxTPMA?pwd=glad)

Please download the dataset and organize it following the directory structure below. Make sure the ground truth (GT) and hazy images are placed in their respective `train` and `test` folders inside the `data/RSDD/` directory.

The final file path should be the same as the following:
```text
┬─ save_models
│   ├─ RSHaze/
│   │   ├─ gladformer-b.pth
│   │   └─ ... (model name)
│   └─ ... (exp name)
└─ data/
    ├─ RSHaze/
    │   ├─ train/
    │   │   ├─ GT/
    │   │   │   └─ ... (image filename)                 # Ground Truth (clear) images for training
    │   │   └─ hazy/
    │   │       └─ ... (corresponds to the former)      # Hazy images for training
    │   └─ test/
    │   │   ├─ GT/                                      # Ground Truth (clear) images for testing
    │   │   └─ hazy/                                    # Hazy images for testing
    ├─ RSDSD/
    │   ├─ train/
    │   │   ├─ GT/
    │   │   └─ hazy/
    │   └─ test/
    │       └─ ...
    └─ ... (dataset name)
