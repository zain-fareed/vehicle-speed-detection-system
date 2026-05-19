# Vehicle Speed Detection System

Vehicle speed detection using **YOLOv8**, **OpenCV**, and **ByteTrack**.

## Overview
This project detects vehicles in video streams, tracks them across frames, and estimates their speed.

## Features
- Vehicle detection with YOLOv8
- Multi-object tracking with ByteTrack
- Speed estimation from video frames
- OpenCV-based video processing
- Easy-to-customize pipeline for traffic analysis

## Tech Stack
- Python
- YOLOv8
- OpenCV
- ByteTrack

## Getting Started

### Prerequisites
Make sure you have:
- Python 3.9+
- pip
- A working webcam or video file
- Model weights and tracker configuration, if required by your implementation

### Installation
```bash
git clone https://github.com/zain-fareed/vehicle-speed-detection-system.git
cd vehicle-speed-detection-system
pip install -r requirements.txt
```

### Run
If your main script is named `main.py`, run:
```bash
python main.py
```

If your entry file has a different name, replace `main.py` with that file.

## Project Structure
A typical structure may include:
- `main.py` — application entry point
- `models/` — trained weights or model files
- `utils/` — helper functions
- `data/` — input videos or sample assets

## Notes
- Update paths to your model weights and input video before running.
- If you add requirements, keep `requirements.txt` up to date.

## License
Add a license file if you want to define how others can use this project.
