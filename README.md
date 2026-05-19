# Vehicle Speed Detection System

Portfolio-ready computer vision project for estimating vehicle speed from traffic video using **YOLOv8**, **OpenCV**, **NumPy**, and **ByteTrack**.

**Author:** Muhammad Zain Fareed

---

## Project Overview

This project detects vehicles in road footage, tracks each vehicle across frames, and estimates speed in km/h using perspective-based motion analysis. It produces:

- an annotated output video: `output_speed.mp4`
- a per-vehicle speed report: `speed_log.csv`

The workflow is designed for fixed-camera traffic footage and can be run locally or in Google Colab.

---

## Key Features

- Vehicle detection with YOLOv8
- Multi-object tracking with ByteTrack IDs
- Speed estimation in km/h from tracked trajectories
- On-frame speed overlays in output video
- CSV export with speed analytics per tracked vehicle

---

## Tech Stack

- Python
- Ultralytics YOLOv8
- OpenCV
- NumPy
- ByteTrack (via Ultralytics tracker integration)

---

## How It Works

1. Load the input traffic video.
2. Detect vehicles in each frame using YOLOv8.
3. Track objects over time with ByteTrack.
4. Map motion into a calibrated perspective space.
5. Estimate speed from distance-over-time.
6. Save annotated video (`output_speed.mp4`) and speed log (`speed_log.csv`).

---

## Repository Structure

```text
.
├── README.md
├── requirements.txt
├── .gitignore
├── speed_detection.py        # Add your existing pipeline script here
├── video.mp4                 # input video (example)
├── output_speed.mp4          # generated after run
├── speed_log.csv             # generated after run
└── assets/
    └── .gitkeep
```

> This repository update focuses on project presentation/setup files. Add your existing `speed_detection.py` from your working project code to run the full pipeline locally.

---

## Installation

```bash
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\\Scripts\\activate
pip install -r requirements.txt
```

---

## Run Instructions

1. Place your existing `speed_detection.py` detection pipeline script in the project root.
2. Place your input traffic video in the project directory.
3. Update `VIDEO_IN` in `speed_detection.py` to match your input filename/path.
4. Run:

```bash
python speed_detection.py
```

After execution, verify these artifacts:

- `output_speed.mp4`
- `speed_log.csv`

---

## Results

- **Video Output (`output_speed.mp4`)**: Shows tracked vehicles and estimated speeds.
- **CSV Output (`speed_log.csv`)**: Contains vehicle-wise speed statistics (for example, avg/max speed by track ID).

---

## Notes

- Accuracy depends on camera placement, calibration, and perspective points.
- Best results come from stable, fixed-camera videos with clear road visibility.
- Different road scenes may require recalibration of perspective references.

---

## Future Improvements

- Automatic camera calibration and scale estimation
- Lane-level speed analytics and violation rules
- Real-time stream support (RTSP/webcam)
- Dashboard for live traffic monitoring
- More robust night/rain handling

---

## Author & Contact

**Muhammad Zain Fareed**

- GitHub: [zain-fareed](https://github.com/zain-fareed)

---

## Portfolio / Recruiter Notes

To present this project professionally:

1. Add 1–3 screenshots in `assets/` (for example, tracked frame and CSV preview).
2. Keep a short demo clip or generated `output_speed.mp4` in the repository (or link it if large).
3. Include `speed_log.csv` sample output when sharing project results.
