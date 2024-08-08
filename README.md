# Real-Time Drowsiness Detection System

This project is a real-time drowsiness detection system that uses a webcam to monitor eye closure levels. The system calculates the Eye Aspect Ratio (EAR) to identify signs of drowsiness and triggers an alert if necessary.

## Features

- Real-time monitoring of eye closure using a webcam.
- Calculates EAR (Eye Aspect Ratio) to detect potential drowsiness.
- Plays a beep sound and displays an alert message if drowsiness is detected.
- Utilizes facial landmark detection and image processing techniques.

## Requirements

- Python 3.x
- `dlib`
- `opencv-python`
- `imutils`
- `scipy`
- `playsound`

You can install the required libraries using pip:

```bash
pip install dlib opencv-python imutils scipy playsound
```

## Setup

### Download the Shape Predictor Model

Download the `shape_predictor_68_face_landmarks.dat` file from dlib's model repository and place it in the same directory as the script.

### Prepare the Beep Sound

Download or create a beep sound in `.wav` format. Save the file as `beep.wav` in the same directory as the script.

## Usage

The script will open a window displaying the video feed from your webcam. If drowsiness is detected based on the EAR calculation, an alert message will be shown, and a beep sound will be played.
To stop the script, press the `q` key while the video window is active.

## Code Overview

- **`eye_aspect_ratio(eye)`**: Calculates the EAR for a given eye.
- **`thresh`**: Threshold value for EAR to trigger the alert.
- **`frame_check`**: Number of consecutive frames with low EAR to confirm drowsiness.
- **`dlib.get_frontal_face_detector()`**: Detects faces in the video feed.
- **`dlib.shape_predictor`**: Predicts facial landmarks.
- **`playsound`**: Plays the beep sound for alerting.


## Acknowledgments

- **dlib** for facial landmark detection.
- **OpenCV** for image processing.
- **imutils** for image resizing.
- **Scipy** for Euclidean distance calculation.
- **playsound** for playing sound files.

