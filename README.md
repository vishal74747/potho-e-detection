# 🛣️ Pothole Detection using YOLOv8m

An AI-powered pothole detection system built using **YOLOv8m** and trained on a custom pothole dataset. This project automatically converts Pascal VOC annotations into YOLO format, prepares the dataset, trains a high-performance object detection model, evaluates its performance, and performs inference on unseen road images.

---

# 📌 Project Overview

Road potholes are one of the major causes of accidents, vehicle damage, and traffic congestion. Manual road inspection is time-consuming and expensive. This project leverages **Computer Vision** and **Deep Learning** to automatically detect potholes from road images using the **YOLOv8m** object detection model.

The notebook includes the complete end-to-end pipeline:

- Dataset preprocessing
- Pascal VOC XML → YOLO conversion
- Automatic dataset splitting
- YOLO dataset configuration
- Model training
- Model evaluation
- Prediction visualization
- Exporting trained weights

---

# 🚀 Features

- ✅ Pascal VOC XML to YOLO annotation conversion
- ✅ Automatic Train / Validation / Test dataset split
- ✅ YOLOv8m object detection training
- ✅ AdamW optimizer
- ✅ Cosine Learning Rate Scheduler
- ✅ Data Augmentation
- ✅ Automatic model evaluation
- ✅ Prediction visualization
- ✅ Export trained model (`best.pt`)

---

# 🛠️ Tech Stack

- Python
- PyTorch
- Ultralytics YOLOv8
- OpenCV
- NumPy
- Matplotlib
- YAML
- XML Parser
- Kaggle Notebook

---

# 📂 Project Structure

```
pothole-detection/
│
├── pothole-detection.ipynb
├── pothole.yaml
├── runs/
│   └── pothole_yolov8m/
│       └── weights/
│           ├── best.pt
│           └── last.pt
├── predictions.png
└── README.md
```

---

# 📊 Dataset Preparation

The dataset uses **Pascal VOC XML annotations**.

The notebook automatically:

- Reads XML annotation files
- Converts bounding boxes into YOLO format
- Creates label files
- Splits the dataset into:

```
Train
Validation
Test
```

It also generates the required `pothole.yaml` configuration file.

---

# ⚙️ Training Configuration

| Parameter | Value |
|-----------|--------|
| Model | YOLOv8m |
| Epochs | 150 |
| Image Size | 640 × 640 |
| Batch Size | 32 |
| Optimizer | AdamW |
| Initial Learning Rate | 0.001 |
| Warmup Epochs | 5 |
| Scheduler | Cosine LR |
| Early Stopping | Patience = 30 |

---

# 📈 Model Performance

The trained model achieved the following results on the test dataset.

| Metric | Score |
|--------|-------:|
| **Precision** | **94.83%** |
| **Recall** | **88.89%** |
| **mAP@50** | **95.02%** |
| **mAP@50-95** | **74.05%** |

### Test Dataset

- **Images:** 234
- **Annotated Potholes:** 576

---

# 🖼️ Prediction Results

The notebook performs inference on unseen road images and generates predictions containing:

- Detected potholes
- Bounding boxes
- Confidence scores

Example output:

```
Road Image
      ↓
YOLOv8m Detection
      ↓
Bounding Boxes + Confidence Score
```

---

# 💾 Export Model

After training, the best-performing model is automatically exported as:

```
pothole_yolov8m_best.pt
```

This model can be directly used for:

- Real-time detection
- Mobile deployment
- Web applications
- Edge devices
- Smart city solutions

---

# ▶️ Running the Project

### Clone the repository

```bash
git clone https://github.com/yourusername/pothole-detection.git
```

### Install dependencies

```bash
pip install ultralytics
```

### Open the notebook

```
pothole-detection.ipynb
```

### Run all cells

The notebook automatically:

- Prepares the dataset
- Converts annotations
- Creates dataset splits
- Trains YOLOv8m
- Evaluates the model
- Performs inference
- Exports the trained weights

---

# 📌 Applications

- Smart City Infrastructure
- Road Damage Monitoring
- Highway Inspection
- Municipal Road Maintenance
- Autonomous Vehicles
- Traffic Safety Systems

---

# 🔮 Future Improvements

- Real-time webcam detection
- Drone-based pothole inspection
- Mobile application integration
- GPS location tagging
- Severity estimation of potholes
- ONNX / TensorRT deployment
- Cloud-based road monitoring platform

---

# 👨‍💻 Author

**Vishal**

AI • Computer Vision • Deep Learning Enthusiast

---

# ⭐ Support

If you found this project useful, please consider giving it a **⭐ Star** on GitHub.

It helps others discover the project and motivates further development.
