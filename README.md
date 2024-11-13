# Computer-Vision

# 1. Face and Eye Detection with OpenCV

This Python program uses OpenCV and Haar Cascade Classifiers to detect faces and eyes in real-time from a webcam feed. It highlights detected faces and eyes with rectangles on the video feed.

## Features

- **Real-time Face Detection**: Detects faces using a pre-trained Haar cascade classifier.
- **Real-time Eye Detection**: Detects eyes within the detected face region.
- **Live Webcam Feed**: Displays the webcam feed with highlighted faces and eyes.
- **Exit**: Press the spacebar to close the webcam feed and exit the program.

## Prerequisites

- **OpenCV**: Make sure OpenCV is installed. You can install it using:
  ```bash
  pip install opencv-python
  ```
- **Haar Cascade Files**: This program uses pre-trained XML files for face and eye detection.
  - `haarcascade_frontalface_default.xml`
  - `haarcascade_eye.xml`
  
  You can download these files from the [OpenCV GitHub repository](https://github.com/opencv/opencv/tree/master/data/haarcascades).

## How It Works

1. **Initialize Haar Cascades**: The program loads pre-trained Haar cascade classifiers for face and eye detection.
2. **Capture Video**: It accesses the webcam and captures video frames.
3. **Detect Faces**: Each frame is converted to grayscale, and faces are detected.
4. **Detect Eyes**: For each detected face, eyes are detected within the face region.
5. **Display Video Feed**: The program displays a real-time video feed with rectangles around faces and eyes.
6. **Exit**: Press the spacebar to stop the video feed and close the program.

## Code Overview

- **Load Haar Cascades**: The `CascadeClassifier` objects are initialized with the face and eye Haar cascades.
- **Video Capture**: The program initializes a webcam feed using `cv2.VideoCapture(0)`.
- **Detection and Drawing**: 
  - `detectMultiScale` is used to detect faces and eyes.
  - `cv2.rectangle` draws rectangles around detected faces and eyes.
- **Exit Condition**: The `while` loop runs until the spacebar is pressed.

## Usage

1. **Save the Code**: Save the code in a Python file, e.g., `face_eye_detection.py`.
2. **Download Haar Cascade Files**: Ensure the Haar cascade XML files are in the same directory as your code or specify their path in the code.
3. **Run the Program**:
   ```bash
   python face_eye_detection.py
   ```
4. **View the Video Feed**: The program will open a webcam window with real-time face and eye detection.
5. **Exit**: Press the spacebar to close the window and end the program.

## Example Output

The program displays a live feed with green rectangles around detected faces and blue rectangles around detected eyes.

_____________________________________________________________________________________________________________________________________________________________________________________________________________________
