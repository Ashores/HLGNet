# HLGNet

**High-Light Guided Network for Low-Light Instance Segmentation with Spatial-Frequency Domain Enhancement**

<!-- Update with your paper link -->
 <!-- Add framework image -->

Official implementation of **HLGNet**. Code will be released after publication!

---

## 🏆 Benchmark Performance

### Results on Belt Dataset (4,291 images)
| Method       | AP_seg↑ | AP_50↑ | AP_75↑ | AP_box↑ | AP_50↑ | AP_75↑ |
|--------------|---------|--------|--------|---------|--------|--------|
| Mask RCNN    | 72.9    | 82.5   | 73.0   | 78.3    | 88.8   | 80.0   |
| Cascade RCNN | 73.6    | 84.4   | 73.5   | 80.0    | 90.7   | 80.3   |
| YOLA         | 79.3    | 89.8   | 80.0   | 85.4    | 95.8   | 87.1   |
| **HLGNet**   | **81.6**| **92.8**| **82.3**| **88.1**| **97.4**| **88.5**|

### Results on Lis Dataset (2,230 images)
| Method       | AP_seg↑ | AP_50↑ | AP_75↑ | AP_box↑ | AP_50↑ | AP_75↑ |
|--------------|---------|--------|--------|---------|--------|--------|
| Mask RCNN    | 34.2    | 55.6   | 34.7   | 41.3    | 63.9   | 44.6   |
| Cascade RCNN | 34.5    | 56.2   | 35.4   | 42.5    | 66.2   | 46.1   |
| YOLA         | 39.8    | 63.5   | 41.4   | 47.5    | 70.9   | 51.8   |
| **HLGNet**   | **42.2**| **65.5**| **43.6**| **50.3**| **72.4**| **53.7**|

*All values are percentages. Higher is better. Highlighted values indicate state-of-the-art performance.*

---

## 📦 Dataset Preparation

### 1. Belt Dataset
Dataset included in repo:  
`/belt/` directory contains full dataset (4,291 images with annotations)

### 2. Lis Dataset
Download from official source:  
[https://github.com/Linwei-Chen/LIS](https://github.com/Linwei-Chen/LIS)

---

## 🛠 Usage (Coming Soon)
```bash
# Installation
git clone https://github.com/yourusername/HLGNet.git
cd HLGNet
pip install -r requirements.txt

# Training
python train.py --dataset belt --config configs/base.yaml

# Evaluation
python test.py --checkpoint pretrained/hlgnet.pth --dataset lis
