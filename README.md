# HLGNet

**High-Light Guided Network for Low-Light Instance Segmentation with Spatial-Frequency Domain Enhancement**

<!-- Update with your paper link -->
 <!-- Add framework image -->

Official implementation of **HLGNet**. Code will be released after publication!

---

## 📊 Full Benchmark Results
### Instance Segmentation Performance on Low-Light Datasets
| Method         | AP_seg↑ | AP_50↑ | AP_75↑ | AP_box↑ | AP_50↑ | AP_75↑ | AP_seg↑ | AP_50↑ | AP_75↑ | AP_box↑ | AP_50↑ | AP_75↑ |
|----------------|---------|--------|--------|---------|--------|--------|---------|--------|--------|---------|--------|--------|
| **Belt Dataset (4,291 images)**   |         |        |        |         |        |        | **Lis Dataset (2,230 images)** |        |        |         |        |        |
| Mask RCNN      | 72.9    | 82.5   | 73.0   | 78.3    | 88.8   | 80.0   | 34.2    | 55.6   | 34.7   | 41.3    | 63.9   | 44.6   |
| Cascade RCNN   | 73.6    | 84.4   | 73.5   | 80.0    | 90.7   | 80.3   | 34.5    | 56.2   | 35.4   | 42.5    | 66.2   | 46.1   |
| DENet          | 79.0    | 89.2   | 78.8   | 84.1    | *95.8* | 85.2   | 38.6    | 61.7   | 39.8   | 46.4    | 70.1   | 51.0   |
| PENet          | 76.4    | 85.9   | 74.2   | 81.0    | 92.8   | 82.1   | 36.1    | 58.8   | 36.4   | 43.6    | 67.3   | 47.1   |
| Zero-DCE       | 79.1    | 90.0   | 78.1   | 83.3    | 95.7   | 86.7   | 38.7    | 62.0   | 39.0   | 46.4    | 70.0   | 50.9   |
| EnlightenGAN   | 77.6    | 88.9   | 78.5   | 84.0    | 93.6   | 84.5   | 38.4    | 61.5   | 39.2   | 45.8    | 69.5   | 49.7   |
| RUAS           | 75.0    | 86.0   | 75.6   | 81.7    | 91.0   | 82.2   | 36.1    | 58.6   | 36.4   | 43.8    | 66.7   | 48.0   |
| SCI            | 76.7    | 86.9   | 75.7   | 81.8    | 92.6   | 83.9   | 36.5    | 59.5   | 37.0   | 44.3    | 67.3   | 48.4   |
| NeRCo          | 76.8    | 88.3   | 77.8   | 81.9    | 92.3   | 83.6   | 36.7    | 60.3   | 38.6   | 44.6    | 68.3   | 48.6   |
| SMG            | 77.4    | 87.2   | 77.2   | 83.3    | 92.6   | 83.4   | 37.4    | 60.3   | 38.7   | 44.7    | 67.4   | 49.2   |
| YOLA           | *79.3*  | 89.8   | 80.0   | *85.4*  | *95.8* | *87.1* | *39.8*  | *63.5* | 41.4   | 47.5    | *70.9* | 51.8   |
| Mask2former    | 74.4    | 83.0   | 73.3   | 76.3    | 81.1   | 75.3   | 35.6    | 55.2   | 35.2   | 37.8    | 55.9   | 39.9   |
| YOLOv8-seg     | 73.1    | 82.6   | 73.4   | 82.4    | 88.6   | 83.9   | 34.3    | 56.0   | 34.9   | 45.1    | 64.3   | 48.3   |
| PointRend      | 71.5    | 80.8   | 78.1   | 75.7    | 82.9   | 75.0   | 32.8    | 52.9   | 39.8   | 37.1    | 57.9   | 39.8   |
| Lis            | 79.8    | *90.6* | 80.5   | 86.3    | 93.4   | 86.5   | 40.8    | 62.7   | *41.5* | 48.0    | 69.2   | 52.6   |
| **HLGNet (Ours)** | **81.6** | **92.8** | **82.3** | **88.1** | **97.4** | **88.5** | **42.2** | **65.5** | **43.6** | **50.3** | **72.4** | **53.7** |


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
