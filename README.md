# Object Detection with YOLOv5

This project demonstrates how to perform object detection using the YOLOv5 model in a Google Colab environment.

## 🚀 Getting Started

Click the badge below to open the notebook in Google Colab:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/satyashree806/Object_Detection.ipynb/blob/main/Object_Detection.ipynb)

---

## 🛠️ Setup Instructions

1. **Clone the YOLOv5 Repository:**
```bash
!git clone https://github.com/ultralytics/yolov5
%cd yolov5
```

2. **Install Required Dependencies:**
```bash
!pip install -r requirements.txt
```

3. **Download Pre-trained Face Detection Model:**
```bash
!wget https://github.com/deepcam-cn/yolov5-face/releases/download/v0.0.1/yolov5s-face.pt -O yolov5s-face.pt
```

4. **Upload an Image:**
Use the Colab file upload tool to upload an image:
```python
from google.colab import files
uploaded = files.upload()

import os
uploaded_file = list(uploaded.keys())[0]
os.rename(uploaded_file, "test.jpg")
```

5. **Run Object Detection:**
```bash
!python detect.py --weights yolov5s.pt --img 640 --conf 0.3 --source test.jpg
```

6. **Display Results:**
```python
from IPython.display import Image
Image(filename='runs/detect/exp/test.jpg')
```

---

## 🎯 Objective
To apply YOLOv5 for object detection (especially face detection) on custom images using a pre-trained model.

---

## 📎 Notes
- The notebook is optimized for running in Google Colab.
- You can switch models (e.g., yolov5s.pt vs yolov5s-face.pt) as needed.
- Customize confidence threshold and image size via the `--conf` and `--img` flags.

---

## 📧 Contact
For questions or support, feel free to open an issue or fork the original repository.

