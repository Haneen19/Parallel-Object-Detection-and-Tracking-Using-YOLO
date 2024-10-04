# Parallel Object Detection and Tracking Using YOLO

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Requirements](#requirements)
- [Code Explanation](#code-explanation)


## Overview
This project implements parallel object detection and tracking using the YOLO (You Only Look Once) algorithm. It captures video feeds from multiple cameras, detects objects in real-time, and displays the results inline. The detected objects are highlighted with bounding boxes, and their appearance is tracked across different camera feeds.

## Features
- Real-time object detection using YOLO.
- Supports multiple camera inputs.
- Displays detected frames inline within the notebook.
- Tracks the sequence of object appearances across cameras.

## Requirements
- Python 3.x
- OpenCV
- NumPy
- Pillow
- IPython



## Code Explanation

Here's a breakdown of the main components of the code:

- **Load YOLO Model**: The YOLO model is loaded using pre-trained weights and configuration files.

- **Detect Objects**: The `detect_and_draw_boxes` function processes each frame to detect objects and draw bounding boxes. It uses a confidence threshold to filter out weaker detections.

- **Camera Processing**: Each camera is processed in a separate thread to allow parallel execution. The `process_camera` function captures frames, detects objects, and saves the output video. It also displays the frames inline using IPython.

- **Object Tracking**: The `track_object` function collects detection information and logs the timestamps of detected objects across different cameras.

- **Parallel Execution**: The `parallel_object_search` function initializes multiple threads for each camera feed and a separate thread for tracking detected objects, enabling simultaneous processing.




