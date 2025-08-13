# 🍏 Apple Leaf Disease Detection & Classification (YOLOv9 + ResNet50)

This project implements a **two-stage deep learning pipeline** for detecting and classifying apple leaf diseases using a combination of **YOLOv9** (for object detection) and **ResNet50** (for classification). It enables **precise detection of diseased regions** on leaves and **accurate classification into disease categories**.

Designed for agricultural technology applications, the system is suitable for:
- 🍎 **Early disease detection** in apple orchards  
- 🌱 **Precision agriculture** and automated monitoring  
- 📊 **Yield protection** through rapid disease identification  
- 🧪 **Research in plant pathology and AI-powered farming**  

---

## 🔍 Overview

This repository includes:

- ✅ Dataset loading and preprocessing  
- ✅ YOLOv9 training for disease area detection  
- ✅ ResNet50 training for disease type classification  
- ✅ Visualization of YOLO detection results  
- ✅ Model evaluation and accuracy reporting  

---

## 🗂️ Dataset Info

**Source**: Private apple leaf dataset (loaded in notebook)  

**Tasks & Classes**:
1. **Detection** (YOLOv9) → Locate diseased leaf regions  
2. **Classification** (ResNet50) → Identify disease type (e.g., healthy, rust, scab, multiple diseases)  

**Structure** (example):
```
dataset/
 ├── train/
 │    ├── images/
 │    └── labels/
 ├── valid/
 │    ├── images/
 │    └── labels/
 └── test/
      ├── images/
      └── labels/
```

**Label Format (YOLO)**:
```
<class_id> <x_center> <y_center> <width> <height>   # normalized (0–1)
```

---

## 🛠️ Step-by-Step Usage

### 1️⃣ Upload or Clone the Project
Run the `.ipynb` notebook in **Google Colab**, **Kaggle**, or a local Jupyter environment.

### 2️⃣ Install Required Packages
```bash
pip install ultralytics torch torchvision torchaudio matplotlib opencv-python
```

### 3️⃣ YOLOv9 Training – Disease Detection
- Loads a pretrained YOLOv9 model  
- Trains for **75 epochs**  
- Detects diseased regions on apple leaves  
- Saves results to `runs/detect/apple-disease-yolov9/`

### 4️⃣ ResNet50 Training – Disease Classification
- Uses PyTorch with pretrained ResNet50 weights  
- Fine-tuned for the apple leaf disease dataset  
- Achieves final accuracy reported in the notebook

### 5️⃣ Model Evaluation
- YOLOv9 metrics: `mAP@0.5`, `mAP@0.5:0.95`, Precision, Recall  
- ResNet50 metrics: Accuracy, Loss curves, Confusion Matrix  

---

## 📸 Example Output

**YOLOv9 output showing bounding boxes around diseased areas:**
```
📷 Image: test/images/sample.jpg  
→ Detected: Scab, Rust with confidence > 0.5  
→ Bounding boxes rendered in real-time
```

**ResNet50 output for classification:**
```
Predicted class: Rust  
Confidence: 97.2%
```

---

## 📦 Requirements
- Python 3.8+  
- Ultralytics YOLOv9  
- PyTorch (for ResNet50)  
- OpenCV, Matplotlib, NumPy

---

## 🔗 Model Weights
Trained YOLOv9 and ResNet50 weights are not published in this repository.  
📩 Email **kajalbhammar@gmail.com** to request access.

---

## 🧑‍💻 Author
**Kajal Bhammar**  
AI/ML Developer  
📧 Email: kajalbhammar@gmail.com  

