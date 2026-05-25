![1](https://github.com/user-attachments/assets/2959bfb0-6dd5-4a48-a428-d074a6d91fe3)


# 🚘 License Plate Detection using YOLO11

A custom object detection project built using **Ultralytics YOLO11** for automatic **License Plate Detection** from images and videos.

This project trains a YOLO11 model on a custom license plate dataset and performs high-speed real-time detection with accurate bounding boxes.

---

# 📌 Features

- ✅ Custom License Plate Detection
- ✅ YOLO11 Object Detection
- ✅ Image Detection Support
- ✅ Video Detection Support
- ✅ Real-Time Inference
- ✅ Easy Training Pipeline
- ✅ GPU Acceleration Support
- ✅ High-Speed Detection

---

# 🧠 Model Used

This project uses:

- **YOLO11n**
- Ultralytics YOLO Framework
- PyTorch Backend

---

# 📂 Project Structure

```bash
LicensePlateDetection/
│
├── datasets/
│   ├── train/
│   ├── valid/
│   └── test/
│
├── runs/
│   └── detect/
│       └── train/
│           └── weights/
│               ├── best.pt
│               └── last.pt
│
├── test_images/
├── test_videos/
│
├── data.yaml
├── train.py
├── detect.py
├── requirements.txt
└── README.md
```

---

# ⚙️ Installation

## 1️⃣ Clone Repository

```bash
git clone https://github.com/your-username/license-plate-detection-yolo11.git
cd license-plate-detection-yolo11
```

---

## 2️⃣ Create Virtual Environment

```bash
python -m venv venv
```

### Activate Environment

#### Windows

```bash
venv\Scripts\activate
```

#### Linux/Mac

```bash
source venv/bin/activate
```

---

## 3️⃣ Install Dependencies

```bash
pip install ultralytics
pip install opencv-python
```

Or:

```bash
pip install -r requirements.txt
```

---

# 📥 Download YOLO11 Weights

The project uses pretrained YOLO11 weights:

```python
model = YOLO("yolo11n.pt")
```

Weights are automatically downloaded by Ultralytics.

---

# 🏋️ Training the Model

Train the YOLO11 model on your custom dataset:

```python
from ultralytics import YOLO

# Load model
model = YOLO("yolo11n.pt")

# Train model
train_results = model.train(
    data="E:/yolo11/demo_custom_yolo11/LicensePlateDataset/data.yaml",
    epochs=5,
    imgsz=640,
    device=0
)
```

---


# 🔍 Image Detection

Detect license plates in a single image:

```python
from ultralytics import YOLO

# Load trained model
model = YOLO("runs/detect/train/weights/best.pt")

# Perform detection
results = model("test_images/0.jpg", save=True)

# Display results
results[0].show()
```

---

# 🎥 Video Detection

Detect license plates in videos:

```python
from ultralytics import YOLO

# Load trained model
model = YOLO("runs/detect/train/weights/best.pt")

# Detect on videos
results = model("test_videos", save=True)
```

---

# 🖼️ Folder Image Detection

Run detection on all images inside a folder:

```python
from ultralytics import YOLO

# Load trained model
model = YOLO("runs/detect/train/weights/best.pt")

# Detect on image folder
results = model("test_images", save=True)
```

---

# 📊 Output Results

Detected outputs are automatically saved inside:

```bash
runs/detect/predict/
```

Outputs include:

- Bounding Boxes
- Confidence Scores
- Saved Images/Videos
- Detection Labels

---

# 🚀 Inference Workflow

```text
Dataset Preparation
        ↓
YOLO11 Training
        ↓
Model Evaluation
        ↓
Image/Video Detection
        ↓
Prediction Output
```

---

# 🛠️ Technologies Used

- Python
- YOLO11
- Ultralytics
- PyTorch
- OpenCV

---

# 📈 Future Improvements

- Real-Time CCTV Detection
- OCR Integration
- Vehicle Tracking
- Number Plate Recognition System
- Streamlit Web App
- Edge Device Deployment

---

# 🌍 Applications

- Smart Traffic Systems
- Toll Booth Automation
- Parking Management
- Vehicle Monitoring
- Security Surveillance

---

# 📜 License

This project is licensed under the MIT License.

