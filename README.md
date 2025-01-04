# Webcam Monitoring Email Alert App

This Python application monitors webcam feed for any significant motion and sends an email alert with an image attachment when motion is detected.

## Prerequisites

Python 3.x

OpenCV (`pip install opencv-python`)

Email-related modules (`pip install secure-smtplib`)

## Usage

1. Clone the repository or download the files: `main.py` and `emailing.py`.

2. Ensure all dependencies are installed.

3. Run `main.py`.
   
## Description

* `main.py`: This file contains the main functionality of the application. It captures video from the webcam, detects motion, captures images when motion is detected, and triggers an email alert using a separate thread.
  
* `emailing.py`: This file contains functions to send emails with image attachments. It utilizes SMTP protocol to send emails via Gmail.

## How It Works

1. The program captures video frames from the webcam.
   
2. It compares each frame with the first frame to detect any significant changes.
   
3. When motion is detected, it captures images of the frame with motion.
  
4. It sends an email alert with the captured image attached.

## Configuration

* Update the `PASSWORD`, `SENDER`, and `RECEIVER` variables in `emailing.py` with appropriate values for your Gmail account.
  
* Make sure to enable less secure app access in your Gmail account settings or use an app password if 2-factor authentication is enabled.

## Note

* Ensure that the webcam is correctly connected and accessible.
  
* Adjust motion detection parameters (`cv2.threshold`, contour area threshold, etc.) as needed based on the environment and camera setup.
  
* This application is designed for demonstration purposes and might require modifications for use in production environments.

## Author 

Priya Patel 

Github: priyap243
