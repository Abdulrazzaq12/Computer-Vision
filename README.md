# Face Detection with YOLOv8

This project implements a real-time face detection system using the Ultralytics YOLOv8 architecture. 

## 🚀 Performance
- **Model:** YOLOv8n (Nano)
- **Speed:** ~16ms inference on NVIDIA MX150
- **mAP50:** 0.784 (78.4%)

## 🛠️ Installation
```bash
pip install ultralytics opencv-python
🏋️ Training
To train the model on a custom dataset, use:

## Python code
from ultralytics import YOLO
model = YOLO('yolov8n.pt')
model.train(data='data.yaml', epochs=10, imgsz=640, batch=4, workers=0)
Note: batch=4 and workers=0 are optimized for laptops with lower VRAM.

🔍 Inference
To run detection on a live webcam:

Python
from ultralytics import YOLO
model = YOLO('weights/best.pt')
model.predict(source='0', show=True)

---

