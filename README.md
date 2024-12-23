# YOLOv8 Object Detection Project

## Overview
This project implements real-time object detection using the YOLOv8 model. The goal is to build a system that can detect and classify objects in images using the YOLO (You Only Look Once) architecture. YOLOv8 is a powerful and efficient model capable of performing both object localization and classification in a single forward pass, making it ideal for real-time applications.

## Dataset
The dataset used for training is structured in the YOLOv8 format, consisting of training and validation sets of images with corresponding annotation files. The dataset is prepared in a way that ensures easy training and evaluation for object detection tasks.

## Installation
To run this project, you'll need to install the necessary dependencies. You can easily set up the environment by running the following command:

```bash
pip install ultralytics

Usage

    Model Training
    The model is trained using a custom dataset for detecting a single class (e.g., vehicles). The training script loads the dataset, configures the YOLOv8 model, and trains it for 50 epochs. It uses a GPU for faster processing.

    Model Evaluation
    After training, the model is evaluated on a test dataset. Random images from the test set are selected, and predictions are displayed with bounding boxes overlaid on the detected objects.

    Prediction
    The trained model can be used to make predictions on new images or videos.

Code Example

from ultralytics import YOLO

# Load YOLOv8 model
model = YOLO('yolov8n.pt')

# Train the model with the custom dataset
model.train(data='path_to_data.yaml', epochs=50, imgsz=416, batch=8)

# Evaluate the model
metrics = model.val()

Features

    Real-time Object Detection
    The YOLOv8 model is optimized for fast object detection with high accuracy, making it suitable for real-time applications.

    Model Evaluation
    Visualize the performance of the model using confusion matrices, F1 score curves, and prediction overlays.

    Custom Dataset Support
    The dataset used for training can be easily formatted in YOLOv8’s required structure, making it flexible for various object detection tasks.

Links

    YOLOv8 Documentation
    Ultralytics GitHub

License

This project is licensed under the MIT License - see the LICENSE file for details.
