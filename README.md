# GLADformer: A Resolution-Aware Global Linear Adaptive Beacon Transformer for Remote Sensing Image Dehazing

[![PyTorch](https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=flat&logo=PyTorch&logoColor=white)](https://pytorch.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Data](https://img.shields.io/badge/Data-BaiduPan-brightgreen.svg)](https://pan.baidu.com/s/1kkd28DAT77nwmEZwgPbPfQ?pwd=glad)

> Welcome to the official code and dataset repository for the paper **GLADformer**. 

---

## 📝 To-Do List / Roadmap

We are continuously updating this repository. Here is our current progress:

- [x] 📊 **Publish the dataset**
- [ ] 💻 **Publish the training code (Training code will be released once the paper is accepted.)**
- [x] 📦 **Publish the pre-trained models**

---
## ⚙️ Environment Preparation

To run the code, you will need **Python 3.11**, **PyTorch 2.5.1**, and **CUDA 12.4**. 

Follow these steps to set up the environment:

**1. Create a new conda environment named `gladformer`:**
```bash
conda create -n gladformer python=3.11 -y
conda activate gladformer
```
**2. Install PyTorch and dependencies:**
```bash
pip install torch==2.5.1 torchvision==0.20.1 torchaudio==2.5.1 --index-url https://download.pytorch.org/whl/cu124
pip install -r requirements.txt
```
- `opencv-python` (*Note: Please install via `pip`. Conda versions use different JPEG codecs and may yield different test results.*)

---
## 📂 Dataset Preparation

The RSDSD dataset we proposed has been released! 

**The dataset we used can be downloaded here:**

Thanks to the contributors of these datasets for their outstanding work!

> ### 📥 Download Dataset
>| **Baidu Netdisk** | [**RSHaze**](https://pan.baidu.com/s/1z79wOSwqn_VG7WGFFLAQ1Q?pwd=glad) | [**RSHaze_L**](https://pan.baidu.com/s/1QNveAuDcSKwHiHCx-CL9HA?pwd=glad) |  [**RRSHID and RSID**](https://pan.baidu.com/s/1MbNnTrwKyO1wHuzH9qGTjg?pwd=glad) | [**RSDSD**](https://pan.baidu.com/s/1kkd28DAT77nwmEZwgPbPfQ?pwd=glad)  | **Baidu Pan access code:glad** |
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
Once you have correctly named all the required files and placed them in the directory paths specified above, you can proceed to test the model.

**Run the following command in your terminal:**
```text
python test.py --model <model_name> --dataset <dataset_name> --exp <config_name> --num_workers 0
```
The configs files contain the training settings for the models. `model_name` is the name of the model you want to test, and `dataset_name` is the name of the dataset you want to test on. 

For more details on command-line arguments and their usage, please refer to `test.py`.

**For example, we test GLADformer-B on the RSHaze dataset:**
```text
python test.py --model gladformer-b --dataset RSHaze --exp RSHaze --num_workers 4
```
The test results will be automatically saved in the `results` directory.

## 🚂 Model Training

> 🚧 **Note**: The code is currently being organized and will be available soon. Thank you for your patience!(Training code will be released once the paper is accepted.)

## 📧 Contact

Send email to [congzhangyang@outlook.com](mailto:congzhangyang@outlook.com) if you have urgent issues that cannot be resolved.
