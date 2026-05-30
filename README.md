# Underwater YOLO26 Detection

## Paper Information

This repository contains the implementation and experimental materials for the research paper:

**Underwater Object Detection Using YOLO26**

This project was developed as part of an academic research work focused on applying YOLO-based real-time object detection models to underwater environments. The repository includes training notebooks, dataset preparation structure, evaluation workflow, and model comparison results used for the paper.

### Author

**Madiyar Bolatov**  
Master’s Student, Applied Artificial Intelligence  
Astana IT University  
Astana, Kazakhstan 

---

## Project Overview

Underwater object detection is an important computer vision task for marine monitoring, underwater robotics, environmental protection, and biological observation. However, underwater images are difficult to process because of:

- low visibility;
- color distortion;
- light absorption and scattering;
- small and occluded objects;
- background noise;
- limited computational resources on underwater devices.

This project applies YOLO-based models to detect underwater objects and evaluates their performance using standard object detection metrics.

---

## Main Objectives

The main objectives of this project are:

1. Prepare an underwater object detection dataset in YOLO format.
2. Train YOLO-based models for underwater detection.
3. Evaluate models using precision, recall, mAP50, and mAP50-95.
4. Compare YOLO26 with previous YOLO versions.
5. Visualize training results and detection outputs.
6. Analyze the suitability of YOLO26 for real-time underwater detection.

---

# Models Used

The project may include experiments with the following models:

- YOLOv8
- YOLOv10
- YOLOv11
- YOLOv12
- YOLO26

The main model of interest is **YOLO26**, which is designed for real-time object detection and focuses on improving accuracy, speed, and deployment efficiency.

---

## Dataset Format

The link for Brackish dataset: https://www.kaggle.com/datasets/aalborguniversity/brackish-dataset

The dataset must be organized in YOLO format. Each image should have a corresponding `.txt` annotation file.

Example annotation format:

```text
class_id x_center y_center width height
```

All coordinates must be normalized between `0` and `1`.

Example:

```text
0 0.512 0.438 0.231 0.184
```

The `data.yaml` file should contain the dataset paths and class names:

```yaml
train: data/train/images
val: data/valid/images
test: data/test/images

nc: 4
names: ["fish", "jellyfish", "starfish", "crab"]
```

Change the class names according to your dataset.

---

## Requirements

Example `requirements.txt`:

```text
ultralytics
torch
torchvision
opencv-python
matplotlib
pandas
numpy
scikit-learn
seaborn
jupyter
notebook
```

If CUDA is used, install a PyTorch version compatible with your GPU and CUDA version.

---

