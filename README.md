## Project Overview

This project implements an Automatic Number Plate Recognition (ANPR) system using Python, YOLOv8 for object detection, SORT for object tracking, and EasyOCR for optical character recognition (OCR). The system is capable of detecting, tracking, and recognizing license plates from video footage, and outputs results in a CSV file format.

## Features

- **Object Detection**: Detects license plates in each video frame using YOLOv8.
- **Object Tracking**: Tracks detected vehicles across frames using the SORT algorithm.
- **Optical Character Recognition (OCR)**: Recognizes and extracts text from detected license plates using EasyOCR.
- **Data Output**: Generates CSV files containing frame number, license plate text, and bounding box coordinates.
- **Interpolation**: Fills in missing data for smooth visualization across frames.
- **Visualization**: Visualizes detected license plates and their trajectories in the video output.

## License Plate Formats

The system is optimized for recognizing UK-style license plates.

## Project Setup

1. **Create a Python environment**:
   ```bash
   conda create --prefix ./env python==3.8 -y
   ```

2. **Activate the environment**:
   ```bash
   conda activate ./env
   ```

3. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Download the SORT module**:
   The SORT module needs to be downloaded from [this repository](https://github.com/abewley/sort).

5. **Run the main script**:
   To process the video and generate the `test.csv` file, run:
   ```bash
   python main.py
   ```

6. **Interpolate missing data**:
   To interpolate values for missing frames, generates `test_interpolated.csv` file, run:
   ```bash
   python add_missing_data.py
   ```

7. **Visualize results**:
   Finally, to create a smooth video with the interpolated data, run to generate `out.mp4` video:
   ```bash
   python visualize.py
   ```
