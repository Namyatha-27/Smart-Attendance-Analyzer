# Smart-Attendance-Analyzer
This project aims to automate attendance marking using face recognition from classroom images, reducing human effort and improving accuracy.
# Problem Statement
Manual attendance marking in classrooms is time-consuming, error-prone, and inefficient, especially in large classes. Faculty members spend valuable lecture time calling roll numbers or circulating attendance sheets, which can also lead to proxy attendance.

This project aims to automate attendance marking using face recognition from classroom images, reducing human effort and improving accuracy.

# Simple Architecture Diagram
Faculty Uploads Image
        |
        v
 Flask Web App
        |
        v
 Face Detection & Encoding
        |
        v
 Match with Student Dataset
        |
        v
 Attendance Stored in CSV

 # Tech Stack

Programming Language: Python
Backend Framework: Flask
Computer Vision: OpenCV
Face Recognition: face_recognition library
Data Storage: CSV file
Frontend: HTML, CSS

# AI Tools Used

face_recognition – Used for face encoding and matching
OpenCV – Used for image processing
NumPy – Used for numerical operations

# Prompt Strategy Summary

This project does not use LLM prompts.
Instead, it uses pre-trained face recognition models to extract facial embeddings and compare them with known student embeddings.
Decision logic:
If face encoding matches known dataset → student marked present
Else → ignored

# Source Code

All source code is included in this repository:
app.py – Main application logic
templates/index.html – User interface
static/style.css – Styling
dataset/students/ – Known student images
attendance/attendance.csv – Attendance records

  # Final Output

Displays list of students marked Present
Automatically appends attendance to attendance.csv

Output format:
Date, Name
31-01-2026, Ananya
31-01-2026, Rahul

# Build Reproducibility Instructions 

To reproduce this build on any system:
Use Python 3.8+
Clone the repository
Install dependencies using:
pip install -r requirements.txt
Ensure dataset images follow format:
studentID_name.jpg
Run:
python app.py
Upload a classroom image and verify attendance output

 # Future Enhancements

Live webcam attendance
Database integration (MySQL/Firebase)
Face recognition accuracy optimization
Admin & faculty login system

