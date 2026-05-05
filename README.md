# 🚗 Arduino Smart RC Car with Bluetooth & Obstacle Detection

## 📌 Overview

This project is an Arduino-based RC car that can be controlled via Bluetooth while using an ultrasonic sensor for real-time obstacle detection.

The system combines **manual control** and **automatic safety**, where the car will stop if an object is too close—even if a forward command is given.

---

## ⚙️ Features

- 📱 Bluetooth control (HC-05)
- 🚗 Movement: forward, backward, left, right, stop
- 📏 Ultrasonic distance sensing (HC-SR04)
- 🛑 Automatic obstacle stop (safety override)
- 🔧 Expandable for smart robotics projects

---

## 🧠 System Logic

1. Receive command from Bluetooth
2. Measure distance using ultrasonic sensor
3. If obstacle detected (distance < threshold):
   → Stop immediately
4. Else:
   → Execute movement command

---

## 🔧 Components

- Arduino Uno / Nano
- L298N Motor Driver
- 2x DC Motors
- HC-SR04 Ultrasonic Sensor
- HC-05 Bluetooth Module
- Battery Pack

---

## 🔌 Wiring

### Ultrasonic Sensor (HC-SR04)

- VCC → 5V
- GND → GND
- TRIG → D9
- ECHO → D10

### Motor Driver (L298N)

- IN1 → D2
- IN2 → D3
- IN3 → D4
- IN4 → D5

### Bluetooth Module (HC-05)

- TX → RX (Arduino)
- RX → TX (Arduino)

### Power

- Battery → L298N
- L298N GND ↔ Arduino GND (COMMON GROUND)

---

## 🎮 Controls

| Command | Action   |
| ------- | -------- |
| F       | Forward  |
| B       | Backward |
| L       | Left     |
| R       | Right    |
| S       | Stop     |

---

## 💻 Code

See `main.ino` for full implementation.

## 🧑‍💻 Author

Your Name
