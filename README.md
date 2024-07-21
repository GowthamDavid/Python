#Face Detection and Demographics Recognition
This repository contains a Python script that uses OpenCV, face_recognition, and MySQL to detect faces in images or video streams, determine the age and gender of the detected faces, and store this information in a MySQL database. Additionally, the script ensures that the face detection count is updated appropriately.

Features
Face Detection: Uses OpenCV's deep learning-based face detector to locate faces in images or video frames.
Age and Gender Prediction: Utilizes pre-trained models to predict the age and gender of detected faces.
Face Encoding and Recognition: Employs the face_recognition library to generate face encodings and recognize if a face has been seen before.
Database Integration: Connects to a MySQL database to store and update face detection data.
Real-Time Processing: Capable of processing video streams in real-time to continuously detect and recognize faces.
Prerequisites
Python 3.x
OpenCV
face_recognition
mysql-connector-python
A MySQL server with a database named presenting
Installation
Clone this repository:

bash
Copy code
git clone https://github.com/yourusername/face-detection-demographics.git
cd face-detection-demographics
Install the required Python packages:

bash
Copy code
pip install opencv-python opencv-python-headless face_recognition mysql-connector-python
Set up your MySQL database and create the required table:

sql
Copy code
CREATE DATABASE presenting;
USE presenting;
CREATE TABLE collecting_data (
    id INT AUTO_INCREMENT PRIMARY KEY,
    Gender VARCHAR(10),
    Age VARCHAR(10),
    FaceCount INT DEFAULT 1
);
Usage
Run the script with an image:

bash
Copy code
python script.py --image path/to/your/image.jpg
Run the script with a video stream (default webcam):

bash
Copy code
python script.py
Code Explanation
Database Connection:
Establishes a connection to a MySQL database and ensures the required column (FaceCount) exists in the collecting_data table.

Face Detection:
The highlightFace function uses OpenCV's DNN module to detect faces in an image and draw bounding boxes around them.

Age and Gender Prediction:
Uses pre-trained models to predict the age and gender of detected faces.

Face Recognition:
Utilizes face_recognition to generate face encodings and compare them against known encodings to recognize previously seen faces.

Database Operations:
Inserts new detections into the database and updates the detection count for recognized faces.

Real-Time Processing:
Continuously captures frames from a video stream, processes them for face detection and recognition, and updates the display with demographic information.

Dependencies
OpenCV
face_recognition
mysql-connector-python
