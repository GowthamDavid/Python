# Face Detection and Demographics Recognition

#### This repository contains a Python script that uses OpenCV, face_recognition, and MySQL to detect faces in images or video streams, determine the age and gender of the detected faces, and store this information in a MySQL database. Additionally, the script ensures that the face detection count is updated appropriately.

## Features

#### > Face Detection: Uses OpenCV's deep learning-based face detector to locate faces in images or video frames.
#### > Age and Gender Prediction: Utilizes pre-trained models to predict the age and gender of detected faces.
#### > Face Encoding and Recognition: Employs the face_recognition library to generate face encodings and recognize if a face has been seen before.
#### > Database Integration: Connects to a MySQL database to store and update face detection data.
#### > Real-Time Processing: Capable of processing video streams in real-time to continuously detect and recognize faces.

## Prerequisites

#### 1. Python 3.x
#### 2. OpenCV
#### 3. face_recognition
#### 4. mysql-connector-python
#### 5. A MySQL server with a database named presenting

## Code Explanation

### 1. Database Connection:
#### Establishes a connection to a MySQL database and ensures the required column (FaceCount) exists in the collecting_data table.
### 2. Face Detection:
#### The highlightFace function uses OpenCV's DNN module to detect faces in an image and draw bounding boxes around them.
### 3. Age and Gender Prediction:
#### Uses pre-trained models to predict the age and gender of detected faces.
### 4. Face Recognition:
#### Utilizes face_recognition to generate face encodings and compare them against known encodings to recognize previously seen faces.
### 5. Database Operations:
#### Inserts new detections into the database and updates the detection count for recognized faces.
### 6. Real-Time Processing:
#### Continuously captures frames from a video stream, processes them for face detection and recognition, and updates the display with demographic information.

## Dependencies
#### 1. OpenCV
#### 2. face_recognition
#### 3. mysql-connector-python


# Login and Registration page for viewing the visualizaion
## Description
#### This Python application integrates Tkinter for the GUI, MySQL for database management, and Matplotlib along with Seaborn for data visualization. It provides a simple login system, user registration, and visual representations of database-stored data.

## Features
### Login and Registration:
#### Users can log in with a username and password.
#### If the user doesn't exist, they are prompted to sign up.
## Data Visualization:
#### Upon successful login, users are presented with various data visualizations:
#### A bar chart showing age distribution by gender.
#### A seaborn bar plot displaying age groupings.
#### A line plot comparing age differences between genders.
## Dependencies
### 1. tkinter: For the graphical user interface.
### 2. mysql-connector-python: For connecting and interacting with the MySQL database.
### 3. matplotlib: For creating static, animated, and interactive visualizations in Python.
### 4. pandas: For data manipulation and analysis.
### 5. seaborn: For statistical data visualization.
### 6. scikit-learn: For preprocessing and transforming data.
## Code Explanation
### 1. Database Connection:
#### mydb = mysql.connector.connect(host="localhost", user="root", password="Gowtham$3", database="presenting")
cursor = mydb.cursor()
Connects to the MySQL database using provided credentials.

### 2. 2. Login Functionality:
#### Validates user credentials against the database.
#### Opens the landing page on successful login or prompts for sign-up if credentials are invalid.
### 3. Sign-Up Prompt:
#### Displays a sign-up form.
#### Adds new user credentials to the database.
### 4. Landing Page with Data Visualizations:
#### Queries data from the database.
#### Visualizes the data using Matplotlib and Seaborn, embedding the plots in the Tkinter window.
### 5. Main Application Loop:
#### Sets up the main application window.
#### Handles the initial login form display.
