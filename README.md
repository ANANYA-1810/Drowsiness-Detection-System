# Drowsiness-Detection-System
Internship
# Project Overview:
Objective:
The primary goal of this project is to detect drowsiness in individuals based on their eye movements using a webcam or any other video source.

# Key Components:

Facial Landmark Detection:
The script employs the dlib library for face detection and facial landmark prediction. Dlib's pre-trained models identify key points on the face, including those around the eyes.

Eye Aspect Ratio (EAR) Calculation:
The eye aspect ratio is a metric derived from the distances between specific facial landmarks around the eyes. It is used to quantify the opening of the eyes.
The EAR is calculated for both the left and right eyes separately, and the average is taken.

Real-time Video Stream Processing:
The project utilizes the imutils library for efficient video stream processing. Frames from the webcam are continuously captured and resized for faster processing.

Drowsiness Detection Logic:
A predefined threshold for the eye aspect ratio (EYE_AR_THRESH) is set. If the average EAR falls below this threshold for a certain number of consecutive frames (EYE_AR_CONSEC_FRAMES), it triggers a drowsiness alert.

Alert Mechanism:
When drowsiness is detected, an alert is displayed on the video frame, and a text-to-speech engine (pyttsx3) is used to vocally announce the alert, providing an audible warning.

User Interaction:
The system runs in a continuous loop until the user interrupts by pressing the 'q' key. This allows real-time monitoring of drowsiness.

# Implementation Details:
Initialization:
The project begins with the initialization of the text-to-speech engine, setting voice properties, and introducing the system.

Facial Landmark Detection:
Dlib's face detector and shape predictor are initialized to identify facial landmarks.

Video Stream Setup:
The script initializes a video stream using VideoStream from imutils to capture real-time video frames from the webcam.

Main Loop:
The core of the system is a loop that continuously captures frames, detects faces, calculates the eye aspect ratio, and checks for drowsiness.

Alert Trigger:
When drowsiness is detected for a sustained duration, an alert is displayed on the frame, and a vocal warning is issued through the text-to-speech engine.

User Interaction and Cleanup:
The system continues to run until the user manually interrupts it by pressing the 'q' key. Upon exit, resources are cleaned up.

# Potential Enhancements:
Accuracy Improvement:
Fine-tuning the eye aspect ratio threshold and the number of consecutive frames can enhance the accuracy of drowsiness detection.
User Interface Enhancement:
Consideration for a graphical user interface (GUI) or a more visually appealing alert system.
Integration with Other Sensors:
Integration with additional sensors or data sources (e.g., head pose, heart rate) for more robust drowsiness detection.
Logging and Analytics:
Incorporation of logging mechanisms to keep track of drowsiness events and performance analytics.
