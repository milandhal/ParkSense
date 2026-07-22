# 🚗 ParkSense AI
### Real-Time Smart Parking Detection System

> An AI-powered computer vision system that detects parking slot occupancy in real time using OpenCV and streams live parking availability through a web application.

---

## 🔴 Live Demo

**Application:** https://smart-parking-management-1.onrender.com/

---

## 📂 GitHub Repository

**Repository:** https://github.com/milandhal/Smart_Parking_Management

---

# 📌 Overview

ParkSense AI is a real-time smart parking management system that leverages **Computer Vision** to automatically detect occupied and vacant parking spaces from parking lot video footage.

The system processes each video frame, analyzes predefined parking regions, and continuously updates parking slot availability through an interactive web interface.

The project demonstrates a complete AI deployment pipeline—from image processing and parking detection to cloud deployment using Flask and Render.

---

# 🎯 Objectives

- Automate parking space monitoring.
- Reduce manual supervision.
- Improve parking space utilization.
- Provide live parking availability.
- Demonstrate practical Computer Vision deployment.

---

# ✨ Key Features

- 🚘 Real-time parking slot occupancy detection
- 🟢 Live visualization of vacant parking spaces
- 🔴 Detection of occupied parking slots
- 📊 Dynamic free-slot counter
- 🌐 Web-based live streaming interface
- ⚡ Lightweight and optimized processing pipeline
- ☁️ Cloud deployment using Render

---

# 🧠 Technology Stack

## Programming Language
- Python

## Computer Vision
- OpenCV
- CVZone
- NumPy

## Backend
- Flask
- Gunicorn

## Deployment
- Render

---

# ⚙️ System Workflow

```
Parking Video
       │
       ▼
Frame Extraction
       │
       ▼
Image Preprocessing
       │
       ▼
Parking Slot Segmentation
       │
       ▼
Pixel Density Analysis
       │
       ▼
Occupancy Detection
       │
       ▼
Live Web Streaming
```

---

# 🖼 Image Processing Pipeline

Each frame undergoes multiple preprocessing stages before parking slot analysis.

### 1️⃣ Grayscale Conversion
Converts RGB images into grayscale for efficient processing.

### 2️⃣ Gaussian Blur
Removes image noise and smooths the frame.

### 3️⃣ Adaptive Thresholding
Separates foreground from background under varying lighting conditions.

### 4️⃣ Median Filtering
Reduces salt-and-pepper noise.

### 5️⃣ Dilation
Enhances detected regions for accurate occupancy analysis.

---

# 🧠 Parking Detection Algorithm

Each parking slot is represented by predefined coordinates.

For every frame:

- Crop the parking region.
- Apply preprocessing.
- Count active pixels using:

```python
cv2.countNonZero()
```

Decision logic:

- **Pixel Count < Threshold → Free Slot**
- **Pixel Count ≥ Threshold → Occupied Slot**

The slot color changes dynamically:

🟢 Green → Available

🔴 Red → Occupied

---

# 📂 Project Structure

```
Smart_Parking_Management/
│
├── app.py
├── CarParkPos
├── carPark.mp4
├── requirements.txt
├── Procfile
├── static/
├── templates/
└── README.md
```

---

# 🚀 Installation

## Clone Repository

```bash
git clone https://github.com/milandhal/Smart_Parking_Management.git

cd Smart_Parking_Management
```

---

## Install Dependencies

```bash
pip install -r requirements.txt
```

---

## Run Application

```bash
python app.py
```

The application will start locally and can be accessed in your browser.

---

# ☁️ Deployment

The application is deployed on **Render** using **Gunicorn**.

### Build Command

```bash
pip install -r requirements.txt
```

### Start Command

```bash
gunicorn app:app
```

---

# 📊 Performance

| Metric | Value |
|---------|-------|
| Detection Accuracy | ~95% |
| Processing | Real-Time |
| Framework | Flask |
| Deployment | Render |

---

# 💼 Project Highlights

This project demonstrates practical experience in:

- Computer Vision
- Image Processing
- Real-Time Video Analytics
- Python Development
- Flask Web Development
- Cloud Deployment
- AI-Based Smart Mobility Solutions

---

# 🌍 Real-World Applications

- Smart Parking Systems
- Shopping Malls
- Airports
- Universities
- Hospitals
- Corporate Campuses
- Smart Cities

---

# 🔮 Future Enhancements

- 🚗 YOLOv8-based vehicle detection
- 📹 Live CCTV camera integration
- 🗺 Parking analytics dashboard
- 🗄 Database integration
- 📱 Mobile application
- 🔔 Real-time parking notifications
- ☁️ IoT-enabled smart parking infrastructure

---

# 📄 License

This project is intended for educational and research purposes.

---

# 👨‍💻 Author

## Milan Dhal

**Machine Learning | Computer Vision | Data Analytics | Full Stack Development**

### GitHub
https://github.com/milandhal

---

⭐ **If you found this project useful, consider giving it a star on GitHub!**
