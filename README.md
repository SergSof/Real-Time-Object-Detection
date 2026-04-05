# Real-Time-Object-Detection

Production-oriented MVP for real-time PPE compliance detection using YOLOv11.

This project is designed for practical monitoring scenarios where it is necessary to detect uniform or PPE compliance violations in real time from:
- webcam input
- RTSP / IP camera streams
- local video files

The repository demonstrates a working computer vision pipeline built with Python, OpenCV, and YOLO, focused on real-world usage and fast deployment.

## Project Overview

The system processes a live or recorded video stream, runs object detection on each frame, and highlights detected compliance violations directly on the video output.

This MVP was built for a real practical use case and serves as a solid base for further production development.

## Features

- Real-time video processing
- YOLOv11-based detection
- Support for webcam input
- Support for RTSP / IP streams
- Support for local video files
- Visualization of detections on frames
- Lightweight Python-based setup

## Tech Stack

- Python
- OpenCV
- Ultralytics YOLO
- NumPy

## Repository Structure

```bash
.
├── main.py
├── main2.py
├── requirements.txt
├── best_s2.pt
├── temp_crop.jpg
└── README.md
```

## Installation

### 1. Clone the repository

```bash
git clone https://github.com/SergSof/Real-Time-Object-Detection.git
cd Real-Time-Object-Detection
```

### 2. Create and activate a virtual environment

#### Linux / macOS

```bash
python3 -m venv venv
source venv/bin/activate
```

#### Windows

```bash
python -m venv venv
venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

## Run Examples

### Webcam

```bash
python main.py
```

### RTSP / IP camera stream

```bash
python main.py --source "rtsp://your_stream_url"
```

### Local video file

```bash
python main.py --source "video.mp4"
```

## Notes

This repository represents a production-oriented MVP built for a real monitoring scenario.

The current implementation focuses on demonstrating the core detection pipeline:

* model inference
* stream and file input handling
* frame-by-frame visualization
* practical deployment simplicity

Possible next steps for further production hardening:

* unified CLI entry point
* structured configuration
* logging
* Docker packaging
* automatic reconnection and stream health checks
* event-based alerting and integrations

## License

MIT License
