# 🧠 Gesture-Based Assistive Communication Using TinyML

## 📌 Overview
Gesture-Based Assistive Communication Using TinyML is an embedded AI-based assistive system designed to help non-verbal or speech-impaired users communicate through hand gestures. The system uses an MPU6050 motion sensor to capture hand movements, an ESP32 DevKit to process the motion data, and a TinyML-ready gesture recognition pipeline to identify predefined gestures. Once a gesture is recognized, a Python-based Streamlit interface displays the output and converts it into speech.

This project demonstrates a low-cost, real-time, and scalable assistive communication solution that can be further developed into a wearable standalone device.

---

## ❗ Problem Statement
Many individuals with speech impairments or temporary communication limitations struggle to express basic needs quickly and effectively. Traditional assistive devices may be expensive, bulky, or less intuitive.

There is a need for a low-cost, real-time, portable communication system that can translate simple hand gestures into meaningful voice output.

---

## 🎯 Objective
To develop a real-time gesture-based assistive communication system that recognizes predefined hand gestures using motion sensing and TinyML concepts, and converts them into text and voice output.

---

## 💡 Key Idea
**Hand Gesture → Motion Sensing → Gesture Recognition → Voice Output**

This project gives voice to hand gestures by converting detected movements into meaningful spoken messages.

---

## ⚙️ How It Works
1. The user performs a predefined hand gesture.
2. The MPU6050 captures 6-axis motion data:
   - Accelerometer: **AX, AY, AZ**
   - Gyroscope: **GX, GY, GZ**
3. The ESP32 DevKit reads the motion data in real time.
4. The gesture is identified using:
   - **Threshold-based logic (current MVP demo)**, or
   - **TinyML model deployment on ESP32 (future/advanced version)**
5. The detected gesture is sent to the Python Streamlit UI.
6. The UI displays the recognized gesture.
7. The system generates corresponding voice output.

### Example:
- Gesture → **Wave**
- Output → **“Hi”**

---

## 🧩 Key Features
- Real-time hand gesture recognition
- Low-cost embedded hardware prototype
- 6-axis motion sensing using MPU6050
- ESP32-based data acquisition and processing
- TinyML-ready architecture for on-device inference
- Python Streamlit dashboard for visualization
- Voice output for assistive communication
- Scalable for multiple gesture-to-message mappings
- Easy to expand into a wearable assistive device

---

## 🛠️ Hardware Components
- **ESP32 DevKit**
- **MPU6050 (Accelerometer + Gyroscope)**
- **USB Cable**
- **Breadboard / Jumper Wires**
- **Laptop / PC** (for Streamlit UI demo)

---

## 💻 Software Stack
- **Arduino IDE**
- **Python 3.x**
- **Streamlit**
- **PySerial**
- **pyttsx3** / browser speech synthesis
- **NumPy**
- **Pandas**
- **Plotly** (optional for waveform visualization)
- **TensorFlow / TensorFlow Lite** *(for TinyML training & deployment – future scope)*
- **MATLAB** *(optional for waveform analysis and signal visualization)*

---

## 🧠 Why TinyML?
TinyML enables machine learning models to run on small microcontrollers such as the ESP32.

In this project, TinyML is used as the **core concept for future on-device gesture recognition**, allowing the system to:
- recognize motion patterns directly on embedded hardware
- reduce latency
- minimize dependency on a computer
- improve portability
- support low-power, real-time assistive communication

### Current MVP:
- Uses **threshold-based gesture detection** for demonstration

### Advanced Version:
- Uses **TinyML model deployed on ESP32** for real-time gesture classification

---

## 🏗️ System Architecture
```text
Hand Gesture
   ↓
MPU6050 Motion Sensor
   ↓
ESP32 DevKit (Sensor Reading + Gesture Processing / TinyML-Ready)
   ↓
Serial Communication
   ↓
Python Streamlit UI
   ↓
Text Display + Voice Output
