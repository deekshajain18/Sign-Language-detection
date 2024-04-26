# Sign Language Detection

This repository contains a sign language detection project that utilizes computer vision and machine learning to recognize and classify hand gestures in real-time. The project includes scripts for collecting hand gesture data and testing the model with a camera feed.

## Table of Contents
- [Overview](#overview)
- [Technologies Used](#technologies-used)
- [Data Collection](#data-collection)
- [Testing](#testing)
- [How to Use](#how-to-use)
- [Contributing](#contributing)

## Overview
This project uses the OpenCV library to capture video input and detect hand gestures. A machine learning classifier is used to recognize sign language gestures, allowing users to perform actions like "Hello," "I Love You," "Okay," "Please," "Thank You," and "Yes."

## Technologies Used
- OpenCV for computer vision tasks
- cvzone for hand tracking and classification
- NumPy for array manipulation
- Math for mathematical operations
- Keras for machine learning model handling
- TensorFlow for deep learning

## Data Collection
The `datacollection.py` script captures images from a webcam feed to create a dataset for training the classifier. It uses the `cvzone.HandTrackingModule` to detect hands and crop the image to fit the hand's bounding box with a specified offset.

### Features
- Captures images of hand gestures with a specified offset and aspect ratio.
- Allows saving images by pressing the "s" key.
- Displays the cropped and resized hand image for validation.

### Usage
- Open the `datacollection.py` script and set the `folder` variable to the desired data collection folder.
- Run the script to start capturing images from the webcam.
- Press "s" to save an image of the current hand gesture.

## Testing
The `test.py` script uses the pre-trained model and classifier to recognize sign language gestures in real-time from a webcam feed. It detects hands, crops the image, and makes predictions using a pre-trained Keras model.

### Features
- Detects hands using `cvzone.HandTrackingModule`.
- Classifies hand gestures with `cvzone.ClassificationModule`.
- Displays the predicted gesture in the video output.

### Usage
- Ensure the Keras model and labels are in the specified directory.
- Run the `test.py` script to start detecting and classifying gestures from the webcam.
- The predicted gesture and a bounding box are displayed in the video feed.

## How to Use
To use this project, follow these steps:
1. Clone this repository.
2. Install the required dependencies listed in `requirements.txt`.
3. Run `datacollection.py` to collect images of hand gestures for your dataset.
4. Train a model using the collected dataset.
5. Use `test.py` to classify hand gestures in real-time.
