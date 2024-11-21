# **Multiple Object Tracking for Marine Science**

### A real-time marine animal identification and tracking system, optimized for drone implementation to assist in marine science research.

---

## **Table of Contents**
- [Description](#description)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)

---

## **Description**
This project is a multiple object tracking system designed for real-time marine animal identification and tracking using drones. It leverages YOLOv5 for detection and deepSORT for tracking, offering a balance between accuracy and speed, crucial for deployment on lightweight drone hardware like the NVIDIA Jetson Nano.

The system aims to support marine science by enhancing animal tracking and population studies in ocean environments, contributing to research in fields like conservation and ecological studies.

Note: due to the large size of many of the files, this project is inccomplete as is on the repository. Files related to setting up the YOLO environement have been ommited. Please email me at nawachter50@gmail.com if you would like me to send the full fileset for replication.

---

## **Features**
- Real-time detection and tracking of marine animals.
- Utilizes YOLOv5 for object detection and deepSORT for object tracking.
- Tracks multiple entities with unique ID assignments.
- Lightweight design optimized for NVIDIA Jetson Nano deployment.
- Robust performance even in challenging oceanic environments.

---

## **Installation**
### **Prerequisites**
- **Hardware**: NVIDIA Jetson Nano
- **Software**: Python 3.8 or above, PyTorch, OpenCV
- **Dependencies**:
  ```bash
  pip install -r requirements.txt

---

## **Usage**
Run from the included virtual environment with:
source yolo_env/bin/activate

In case you need to download the required packages, download with:
pip install -r requirements.txt

Run with:
python3 track.py --source <video.mp4> --yolo_model <model.pt> --conf-thres <0.x> --save-vid

If you want to run it from a video stream instead of a pre-existing video use "--source 0" instead of a video file.

output video goes to runs/track/exp[x]

--conf-thres can be whatever confidence threshold you deem appropriate, I personally found 0.3 to 0.5 to be a good range of values for my model.

