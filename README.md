# GLADformer: A Resolution-Aware Linear Agent Transformer with Global Context for Remote Sensing Image Dehazing

[![PyTorch](https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=flat&logo=PyTorch&logoColor=white)](https://pytorch.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Data](https://img.shields.io/badge/Data-BaiduPan-brightgreen.svg)](https://pan.baidu.com/s/1kkd28DAT77nwmEZwgPbPfQ?pwd=glad)

> Welcome to the official code and dataset repository for the paper **GLADformer**. 

---

## 📝 To-Do List / Roadmap

We are continuously updating this repository. Here is our current progress:

- [x] 📊 **Publish the dataset**
- [ ] 💻 **Publish the training code(Training code will be released once the paper is accepted.)**
- [x] 📦 **Publish the pre-trained models**

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
- `opencv-python` (*Note: Please install via `pip`. Conda versions use different JPEG codecs and may yield different test results.*)

---
## 📂 Dataset Preparation

The RSDSD dataset we proposed has been released! 

**The dataset we used can be downloaded here：**

Thanks to the contributors of these datasets for their outstanding work！

> ### 📥 Download Dataset
>| **Baidu Netdisk** | [**RSHaze**](https://pan.baidu.com/s/1z79wOSwqn_VG7WGFFLAQ1Q?pwd=glad) | [**RSHaze_L**](https://pan.baidu.com/s/1QNveAuDcSKwHiHCx-CL9HA?pwd=glad) |  [**RRSHID and RSID**](https://pan.baidu.com/s/1MbNnTrwKyO1wHuzH9qGTjg?pwd=glad) | [**RSDSD**](https://pan.baidu.com/s/1kkd28DAT77nwmEZwgPbPfQ?pwd=glad)  | **Baidu Pan access code：glad** |
>| :--- | :--- | :--- | :--- | :--- | :--- |

Please download the dataset and organize it following the directory structure below. Make sure the ground truth (GT) and hazy images are placed in their respective `train` and `test` folders inside the `data/RSHaze/` directory.

The final file path should be the same as the following:
```text
┬─ configs
│   ├─ RSHaze/                                          # Please ensure that the configuration file matches the dataset name
│   │   ├─ gladformer-b.json
│   │   └─ ... (model name)
│   └─ ... (dataset name)
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
```

## 🚀 Quick Evaluation

### 📥 Pre-trained Models

We provide the pre-trained models for evaluation. You can download them via the following link:

- **Baidu Netdisk**: [Download Here](https://pan.baidu.com/s/108RJoSLZu9zj6xdCuyruNg?pwd=glad)
- **Extraction Code**: `glad`

### 📂 Directory Configuration

After downloading, please ensure the `.pth` file is placed in the correct path so the scripts can locate it automatically. The expected project hierarchy is as follows:

```text
GLADformer/
├── ...
├── saved_models/
│   └── RSHaze/
│   │   └── gladformer-t.pth  <-- Place the downloaded file here
│   │   └─ ... (model name)
│   ├─ Haze1k_thin/
│       └── gladformer-t.pth
├── ...
```

## 🚂 Model Training

> 🚧 **Note**: The code is currently being organized and will be available soon. Thank you for your patience!(Training code will be released once the paper is accepted.)

## 📧 Contact

Send email to [congzhangyang@outlook.com](mailto:congzhangyang@outlook.com) if you have urgent issues that cannot be resolved.
