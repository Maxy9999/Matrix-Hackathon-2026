# VisionGrid

> **One Identity. Multiple Views. Zero Confusion.**

VisionGrid is a real-time AI-powered multi-camera person detection, tracking, and PTZ automation system designed for intelligent surveillance environments. The system detects and tracks individuals across multiple RTSP camera streams, allows operators to select a target interactively, and automatically controls PTZ cameras to keep the target centered.

Built using modern computer vision and deep learning technologies, VisionGrid combines YOLO-based person detection, DeepSORT multi-object tracking, ONVIF PTZ control, and real-time visualization into a unified intelligent surveillance pipeline.

Based on the uploaded project documentation and pitch deck.  

---

# Features

* Real-time multi-camera RTSP stream processing
* AI-based human detection using YOLOv8/YOLOv11
* Multi-object tracking using DeepSORT
* Interactive target selection via mouse click
* Automatic PTZ camera tracking using ONVIF
* Smooth camera movement with jitter reduction and dead-zone logic
* Real-time OpenCV visualization
* Parallel frame processing with threaded readers
* Low-latency pipeline architecture

---

# System Architecture

```text
RTSP Streams
      ↓
Threaded Frame Readers
      ↓
YOLO Person Detection
      ↓
DeepSORT Tracking
      ↓
Target Selection (User Input)
      ↓
PTZ Control Logic
      ↓
Real-Time Display Output
```

Based on the architecture described in the project document. 

---

# Technology Stack

| Technology       | Purpose                          |
| ---------------- | -------------------------------- |
| Python           | Core development                 |
| OpenCV           | Video processing & visualization |
| YOLOv8 / YOLOv11 | Person detection                 |
| DeepSORT         | Multi-object tracking            |
| ONVIF            | PTZ camera control               |
| NumPy            | Numerical processing             |

Referenced from the uploaded documentation. 

---

# How It Works

## 1. Video Ingestion

The system reads multiple RTSP streams simultaneously using threaded frame readers to ensure low latency and parallel processing.

## 2. Person Detection

Each frame is processed using YOLO to detect human subjects with configurable confidence thresholds.

## 3. Multi-Object Tracking

DeepSORT assigns unique IDs to detected individuals and maintains identity continuity across frames.

## 4. Target Selection

The operator can click on any tracked individual in the display window to select them as the active target.

## 5. PTZ Tracking

ONVIF-compatible PTZ cameras automatically adjust pan and tilt to keep the selected target centered in frame.

## 6. Real-Time Visualization

The output feed displays:

* Bounding boxes
* Track IDs
* Highlighted target person
* Live tracking updates

---
<!--
# Project Structure (Suggested)

```text
VisionGrid/
│
├── main.py
├── detector/
│   ├── yolo_detector.py
│   └── utils.py
│
├── tracker/
│   ├── deepsort_tracker.py
│   └── reid.py
│
├── ptz/
│   ├── onvif_controller.py
│   └── tracking_logic.py
│
├── streams/
│   ├── rtsp_reader.py
│   └── threaded_capture.py
│
├── ui/
│   ├── visualization.py
│   └── mouse_callback.py
│
├── configs/
│   └── config.yaml
│
├── models/
│   └── yolov8.pt
│
├── requirements.txt
└── README.md
```

---
-->
# Installation

## Clone Repository

```bash
git clone <repository-url>
cd VisionGrid
```

---

## Create Virtual Environment

```bash
python3 -m venv venv
source venv/bin/activate
```

### Expected behavior

* Virtual environment gets activated.

---

## Install Dependencies

```bash
pip install -r requirements.txt
```

---

# Example Requirements

```txt
opencv-python
numpy
ultralytics
deep-sort-realtime
onvif-zeep
torch
torchvision
```

---

# Running the System

```bash
python3 main.py
```

### Expected behavior

* RTSP streams start
* Detection begins
* Bounding boxes appear
* User can click a target
* PTZ tracking activates

---

# Supported Capabilities

| Capability                   | Status                 |
| ---------------------------- | ---------------------- |
| Multi-camera input           | Supported              |
| Real-time detection          | Supported              |
| Multi-object tracking        | Supported              |
| PTZ automation               | Supported              |
| Interactive target selection | Supported              |
| Cross-camera ReID            | Partial / Experimental |

---

# Current Limitations

* No persistent identity across all cameras
* Limited cross-camera ReID
* No centralized database
* Single-target PTZ tracking
* No web dashboard yet

Based on the uploaded documentation. 

---

# Future Enhancements

* Advanced ReID using OSNet / FastReID
* Cross-camera identity handoff
* Web-based dashboard
* Event logging and analytics
* Multi-target PTZ support
* Distributed deployment support

Referenced from the uploaded project document. 

---

# Applications

* Smart city surveillance
* Airports & transport hubs
* Shopping malls
* Industrial monitoring
* Security operations centers
* Retail analytics

---

# Achievements

* Built a real-time AI surveillance pipeline
* Integrated PTZ automation
* Enabled operator-assisted tracking
* Processed multiple streams simultaneously
* Developed a functional intelligent surveillance prototype

As highlighted in the uploaded project materials. 

---

# Team

* Kathan Kotadia
* Vidhi Vadher
* Prince Sharma
* Manish Agarwal

Referenced from the uploaded presentation. 
