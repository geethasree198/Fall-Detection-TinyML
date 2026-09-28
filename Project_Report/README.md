# Real-Time Fall Detection and Heart Rate Monitoring Using TinyML

A real-time embedded healthcare monitoring system that combines TinyML-based fall detection with heart rate monitoring using NodeMCU ESP8266, MPU6050, MAX30102, and Edge Impulse.

## 📌 Project Overview

This project develops a lightweight, edge-based fall detection system designed to perform real-time classification directly on a resource-constrained microcontroller.

The system uses accelerometer data from the MPU6050 to distinguish between FALL and NO_FALL activities. A MAX30102 sensor is additionally used for heart rate monitoring, while an active buzzer provides an immediate physical alert.

The machine learning model is developed and verified using Edge Impulse and deployed on the NodeMCU ESP8266.

## 🎯 Objectives

- Develop a machine learning-based fall detection system.
- Collect and preprocess accelerometer data for fall and normal activities.
- Train a lightweight model suitable for embedded deployment.
- Perform real-time inference directly on the microcontroller.
- Integrate heart rate monitoring using the MAX30102 sensor.
- Provide immediate alerts using an active buzzer.
- Minimize dependence on cloud-based processing.

## 🛠️ Hardware

- NodeMCU ESP8266
- MPU6050 6-axis IMU
- MAX30102 PPG sensor
- Active buzzer
- Breadboard
- Jumper wires
- Micro USB cable
- Header pins

## 💻 Software and Tools

- Arduino IDE
- Edge Impulse Studio
- Edge Impulse CLI
- Node.js
- Embedded C
- TinyML

## 🧠 Machine Learning

The project uses time-series accelerometer data from the MPU6050.

The Edge Impulse pipeline includes:

- Data collection
- Signal preprocessing
- Spectral Analysis / FFT
- Dense Neural Network
- INT8 quantization
- Model verification
- On-device deployment

## 📊 Dataset

The system uses FALL and NO_FALL classes collected from MPU6050 sensor data.

The documented setup uses:

- Sampling rate: 100 Hz
- Window size: 2 seconds
- Window overlap: 50%
- Classes: FALL and NO_FALL
- 80/20 training-validation split

## ⚙️ System Operation

1. MPU6050 collects motion data.
2. Sensor data is streamed and processed.
3. Edge Impulse extracts relevant features.
4. The trained TinyML model classifies the activity.
5. The NodeMCU performs on-device inference.
6. A buzzer is triggered when a fall is detected.
7. MAX30102 continuously monitors heart rate.

## 📈 Results

The documented experiments achieved:

- Training Accuracy: 95.8%
- Validation Accuracy: 93.2%
- Model Size: 18.4 KB (INT8)
- Inference Time: 48 ms per window
- Peak Runtime RAM: 22 KB
- Flash Usage: 67 KB
- Overall Accuracy: 93.0%
- Precision: 93.9%
- Recall: 92.0%
- F1 Score: 92.9%
- End-to-End Latency: <150 ms

## 🔬 Edge Impulse Verification

The project also documents Edge Impulse training and verification results, including model compilation, feature generation, training output, confusion matrix evaluation, and on-device performance.

## 📄 Project Report

The complete project report is available in:

`Project_Report/Fall_Detection_TinyML_Project_Report.pdf`

## 🔮 Future Scope

- Larger and more diverse real-world datasets
- Improved detection of slow-onset falls
- Additional wearable sensors
- Real-time IoT connectivity
- Mobile/cloud notification systems
- Further model optimization for low-power embedded devices
