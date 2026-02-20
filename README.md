# Servo-Dog-Robot
Quadruped servo-based robot dog built with Raspberry berry Pi and Python control.

# Servo Dog 🐶

**Smart Seeing Eye-Dog Robot** – guiding visually impaired users through real-time navigation, obstacle detection, and pedestrian signal recognition.  

Developed as part of **Columbia University EECS E4764 Fall '21 Internet of Things** project (Team 26).

---

## 🎯 Project Overview

We present a wheeled robot that assists visually impaired users, emulating a smart guide dog. Key capabilities include:

- Real-time obstacle avoidance
- Platform detection
- Pedestrian signal classification
- Voice-guided navigation via smartphone interface
- Emergency location alerts

This system provides a low-cost alternative to traditional guide dogs, costing less than 1% of a service dog's price.

---

## 🏗️ System Architecture

The system consists of the following components:

1. **Wheeled Robot**: Raspberry Pi 4 controls the motors and sensors.
2. **Sensors**:
   - HC-SR04 Ultrasonic Sensor – detects obstacles.
   - VL53L0X Laser Sensor – measures ground level for navigation.
3. **Actuators**:
   - TB6612 Motor Driver + DC BO Motors – differential drive for movement.
4. **Camera** – 5MP camera for traffic signal classification.
5. **Edge-CNN Classifier** – MobileNet-based LytNet CNN running on Raspberry Pi.
6. **Smartphone Interface** – Android app for voice commands, navigation, and emergency alerts.
7. **Cloud & APIs**:
   - Google Maps API – route guidance.
   - Google Speech-to-Text API – voice commands.
8. **Power Supply** – 5V mobile power bank.

**System Architecture Diagrams**
- [Pipeline Image](images/pipeline.png)  
- [Embedded System Schematic](images/schematic.png)

---

## 💻 Technical Implementation

- **Edge CNN Classifier**: LytNet (PyTorch) optimized for Raspberry Pi, 98% precision, 96% recall on Chinese pedestrian dataset, adapted via transfer learning to NY signals.
- **App Interface**: Android Studio, large buttons, voice-guided navigation, emergency alerts.
- **Communication**: TCP/IP over Wi-Fi between Raspberry Pi and smartphone.
- **Motors & Actuators**: Differential drive using TB6612 driver and DC BO motors.

---

## 🛠️ Tech Stack

- Raspberry Pi 4
- Python, PyTorch
- Android Studio
- Google Maps & Speech-to-Text APIs
- Sensors: HC-SR04, VL53L0X
- DC Motors + TB6612 motor driver
- MobileNet CNN architecture

---

## 📈 Results

- Successfully navigated small obstacle courses.
- Correctly classified pedestrian traffic signals in real-time.
- Guided a blindfolded test user safely.
- Developed a working Android app interface.
- High precision and recall on self-collected NY pedestrian dataset.

**Project Images**

Front View: ![Front](images/bot-front.jpg)  
Top View: ![Top](images/bot-top.jpg)  
Side View: ![Side](images/bot-side.jpg)  
App Screenshot: ![App](images/app.png)  
Problems Addressed: ![Pain Points](images/pain.png)

---

## 📂 Dataset

- **Imvisible Traffic Signal Dataset** – 4 classes  
- **Custom NY Pedestrian Dataset** – collected and annotated by the team  
- Transfer learning used for adapting model to local signals.

---

## 🚀 How to Run Locally

1. Clone the repository:

 git clone https://github.com/<your-username>/Servo-Dog.git

2. Set up Raspberry Pi 4 with Python & PyTorch.

3. Connect sensors (HC-SR04, VL53L0X) and DC motors via TB6612 driver.

4. Upload CNN model and Python control scripts to Raspberry Pi.

5. Connect smartphone app for navigation and speech interface.

6. Power system via 5V mobile power bank.


