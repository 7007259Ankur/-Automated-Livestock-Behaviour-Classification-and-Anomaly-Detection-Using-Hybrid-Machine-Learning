Automated Livestock Behaviour Classification and Anomaly Detection Using Hybrid Machine Learning
📌 Overview

This project builds a hybrid machine-learning system that automatically classifies cattle behaviour and detects abnormal movement patterns using accelerometer data.
The system combines a LightGBM classifier for supervised behaviour prediction and an LSTM Autoencoder for unsupervised anomaly detection, enabling both accurate behaviour recognition and early disease indication.

📂 Dataset

17 days of tri-axial accelerometer data (X, Y, Z) recorded at 50 Hz

Includes behaviours such as grazing, rumination, resting, standing, and walking

Preprocessed using windowing, normalization, and feature extraction

✨ Features Used
Time-Domain Features

Signal Magnitude Area (SMA)

Euclidean Norm Minus One (ENMO)

Jerk Energy

Total Acceleration

Frequency-Domain Features

Power Spectral Density (PSD) across behaviour-specific frequency bands

Helps resolve confusion in static behaviours (standing vs lying)

🧠 Model Architecture
1. Supervised Behaviour Classification (LightGBM)

Input: Engineered statistical + frequency features

Output Behaviours: Grazing, Rumination, Resting, Walking

Achieved 99.98% accuracy

2. Unsupervised Anomaly Detection (LSTM Autoencoder)

Trained on normal behaviour sequences

Reconstruction error used as anomaly score

Detects gait issues like limping, trembling, or unknown abnormalities

🚀 Key Results

99.98% classification accuracy using LightGBM

Strong anomaly detection with large error difference between normal vs abnormal patterns

PSD features fixed long-standing misclassification problems

Suitable for real-time, low-power edge deployment

📌 Project Workflow

Data preprocessing (windowing + normalization)

Feature engineering (time & frequency domain)

Train LightGBM classifier

Train LSTM Autoencoder for anomaly detection

Evaluate supervised + unsupervised performance

Integrate into a hybrid decision framework

📑 Applications

Precision livestock farming

Early disease detection

Automated cattle monitoring systems

Real-time farm analytics on edge devices

📘 Future Scope

Use transformer-based time-series models

Deploy on microcontrollers (ESP32/ARM Cortex)

Add temperature, GPS, audio sensors

Adaptive anomaly thresholding

Build a farmer-friendly dashboard

👨‍💻 Author

Ankur Gupta
7th Semester Academic Project
B.Tech – Computer Science & Engineering
Indian Institute of Information Technology (IIIT) Guwahati

👩‍🏫 Supervisor

Dr. Moumita Roy
Assistant Professor, IIIT Guwahat
