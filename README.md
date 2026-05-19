# Vehicle Speed Detection System

**Author:** Muhammad Zain Fareed

A computer vision project that detects vehicles in traffic video, tracks them across frames, and estimates their speed using perspective transformation and object tracking.

---

## Demo

- **Input Video:** `video.mp4` or your uploaded source video  
- **Output Video:** `output_speed.mp4`  
- **Speed Report:** `speed_log.csv`

> If you have a short demo clip, place it in the repository and link it here.

---

## Project Overview

This project uses **YOLOv8** for vehicle detection and **ByteTrack** for multi-object tracking.  
Each vehicle is tracked across frames using a unique track ID. The vehicle’s position is projected into a bird’s-eye view using perspective transformation, and real-world speed is estimated in km/h.

The system also exports a CSV report containing the average and maximum speed for each tracked vehicle.

---

## Features

- Detects vehicles in video frames
- Tracks vehicles with unique IDs
- Estimates vehicle speed in km/h
- Displays live speed labels on the video
- Exports speed statistics to CSV
- Supports cars, motorcycles, buses, and trucks
- Works on fixed camera traffic footage

---

## Tech Stack

- **Python**
- **OpenCV**
- **NumPy**
- **Ultralytics YOLOv8**
- **ByteTrack**

---

## How It Works

1. Load the input video
2. Detect vehicles using YOLOv8
3. Track vehicles across frames using ByteTrack
4. Convert image coordinates to bird’s-eye-view coordinates
5. Calculate distance traveled over time
6. Estimate speed in km/h
7. Save the annotated output video and CSV report

---

## Project Structure

```text
.
├── assets/
│   ├── output_frame.png
│   └── csv_preview.png
├── speed_detection.py
├── README.md
├── requirements.txt
├── output_speed.mp4
├── speed_log.csv
└── video.mp4
```

---

## Installation

Install the required Python packages:

```bash
pip install ultralytics opencv-python numpy
```

Or, if you use a requirements file:

```bash
pip install -r requirements.txt
```

---

## How to Run

1. Make sure your input video is available in the project folder.
2. Update the `VIDEO_IN` variable inside `speed_detection.py` if needed.
3. Run the script:

```bash
python speed_detection.py
```

After execution, the following files will be generated:

- `output_speed.mp4`
- `speed_log.csv`

---

## Results

### Output Video
The output video shows:
- detected vehicles
- track IDs
- speed labels in km/h
- color-coded speed display

### CSV Report
The CSV file contains:
- `track_id`
- `class`
- `frames_tracked`
- `avg_kph`
- `max_kph`

---

## Notes

- Speed accuracy depends on camera position, road geometry, and calibration quality.
- The system performs best with a fixed camera and clear lane visibility.
- Perspective points may need to be adjusted for different road scenes.

---

## Future Improvements

- Improve road calibration accuracy
- Support live webcam input
- Add lane-wise analysis
- Build a dashboard for real-time monitoring
- Add better speed smoothing for noisy detections

---

## Learning Outcomes

This project helped me strengthen my skills in:

- Computer Vision
- Object Detection
- Multi-Object Tracking
- Speed Estimation
- Video Analytics
- Python development

---

## Author

**Muhammad Zain Fareed**

---

## Contact

If you'd like to connect or discuss this project, feel free to reach out.
