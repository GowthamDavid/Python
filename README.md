# Face Detection and Demographics Recognition

### This repository contains a Python script that uses OpenCV, face_recognition, and MySQL to detect faces in images or video streams, determine the age and gender of the detected faces, and store this information in a MySQL database. Additionally, the script ensures that the face detection count is updated appropriately.

## Features

### > Face Detection: Uses OpenCV's deep learning-based face detector to locate faces in images or video frames.
### > Age and Gender Prediction: Utilizes pre-trained models to predict the age and gender of detected faces.
### > Face Encoding and Recognition: Employs the face_recognition library to generate face encodings and recognize if a face has been seen before.
### > Database Integration: Connects to a MySQL database to store and update face detection data.
### > Real-Time Processing: Capable of processing video streams in real-time to continuously detect and recognize faces.
