# Face Detection and Demographics Recognition

#### This repository contains a Python script that uses OpenCV, face_recognition, and MySQL to detect faces in images or video streams, determine the age and gender of the detected faces, and store this information in a MySQL database. Additionally, the script ensures that the face detection count is updated appropriately.

## Features

#### > Face Detection: Uses OpenCV's deep learning-based face detector to locate faces in images or video frames.
#### > Age and Gender Prediction: Utilizes pre-trained models to predict the age and gender of detected faces.
#### > Face Encoding and Recognition: Employs the face_recognition library to generate face encodings and recognize if a face has been seen before.
#### > Database Integration: Connects to a MySQL database to store and update face detection data.
#### > Real-Time Processing: Capable of processing video streams in real-time to continuously detect and recognize faces.

## Prerequisites

#### . Python 3.x
#### OpenCV
#### face_recognition
#### mysql-connector-python
#### A MySQL server with a database named presenting

## Code Explanation

### Database Connection:
#### Establishes a connection to a MySQL database and ensures the required column (FaceCount) exists in the collecting_data table.

### Face Detection:
#### The highlightFace function uses OpenCV's DNN module to detect faces in an image and draw bounding boxes around them.

### Age and Gender Prediction:
#### Uses pre-trained models to predict the age and gender of detected faces.

### Face Recognition:
#### Utilizes face_recognition to generate face encodings and compare them against known encodings to recognize previously seen faces.

### Database Operations:
#### Inserts new detections into the database and updates the detection count for recognized faces.

### Real-Time Processing:
#### Continuously captures frames from a video stream, processes them for face detection and recognition, and updates the display with demographic information.

## Dependencies
### OpenCV
### face_recognition
### mysql-connector-python
