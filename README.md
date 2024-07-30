```markdown
# Drowsiness Detection Model

## Overview

This repository contains a project focused on detecting drowsiness in individuals using computer vision techniques and deep learning. The primary goal of this project is to develop a model that can accurately identify signs of drowsiness, which can be crucial for applications in driver safety and workplace monitoring.

## Features

- **Real-Time Drowsiness Detection**: Utilizes a YOLOv5-based model to detect drowsiness in real-time from video input.
- **Custom Dataset**: Trained on a dataset of annotated images capturing various states of drowsiness and alertness.
- **Alerts**: Provides visual or auditory alerts when drowsiness is detected.

## Technologies Used

- Python
- PyTorch
- YOLOv5
- OpenCV
- NumPy

## Getting Started

### Prerequisites

Before you begin, ensure you have Python installed on your machine. You can download it from [python.org](https://www.python.org/downloads/).

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/Nerry-AXL/Drowsiness-.git
   ```
2. Navigate to the project directory:
   ```bash
   cd Drowsiness-
   ```
3. Install the required libraries:
   ```bash
   pip install -r requirements.txt
   ```

### Dataset Preparation

1. Collect a dataset of images that includes various states of drowsiness and alertness.
2. Annotate the images using a tool like [LabelImg](https://github.com/tzutalin/labelImg).
3. Create a `dataset.yaml` configuration file that specifies the paths to your images and class names.

### Training the Model

1. To train the model, run the following command:
   ```bash
   python train.py --img 640 --batch 16 --epochs 50 --data dataset.yaml --weights yolov5s.pt
   ```
   Adjust parameters as needed based on your hardware and dataset size.

### Real-Time Detection

1. To run the drowsiness detection in real-time, execute:
   ```bash
   python drowsiness_detection.py
   ```
   Ensure your webcam is enabled, and the script will start processing the video feed.

## Evaluation

After training, evaluate the model's performance using a separate validation set. Monitor metrics such as Mean Average Precision (mAP) to assess accuracy.


```
