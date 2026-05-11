# Arduino Smart RC Car with Bluetooth and Obstacle Detection

## Overview

This project is an Arduino-based smart RC car that supports Bluetooth control and real-time obstacle detection using an ultrasonic sensor.

The system combines manual movement control with an automatic safety mechanism that prevents collisions by stopping the car when an object is detected within a specified distance threshold.

This project serves as a foundation for robotics, embedded systems, and autonomous vehicle experimentation.

---

## Features

- Bluetooth-based wireless control using HC-05
- Directional movement control
  - Forward
  - Backward
  - Left
  - Right
  - Stop
- Real-time obstacle detection using HC-SR04
- Automatic collision prevention system
- Expandable architecture for future robotics features

---

## System Workflow

1. The Arduino receives movement commands via Bluetooth.
2. The ultrasonic sensor continuously measures front-facing distance.
3. If an obstacle is detected below the configured threshold:
   - The motors stop immediately.
4. Otherwise:
   - The requested movement command is executed.

---

## Hardware Components

- Arduino Uno / Nano
- L298N Motor Driver
- HC-SR04 Ultrasonic Sensor
- HC-05 Bluetooth Module
- 2x DC Motors
- Battery Pack

---

## Wiring Configuration

### HC-SR04 Ultrasonic Sensor

| HC-SR04 | Arduino |
|----------|----------|
| VCC      | 5V       |
| GND      | GND      |
| TRIG     | D9       |
| ECHO     | D10      |

### L298N Motor Driver

| L298N | Arduino |
|--------|----------|
| IN1    | D2       |
| IN2    | D3       |
| IN3    | D4       |
| IN4    | D5       |

### HC-05 Bluetooth Module

| HC-05 | Arduino |
|--------|----------|
| TX     | RX       |
| RX     | TX       |

### Power Configuration

- Battery Pack → L298N
- L298N GND ↔ Arduino GND (Common Ground)

---

## Control Commands

| Command | Function |
|---------|----------|
| F | Move Forward |
| B | Move Backward |
| L | Turn Left |
| R | Turn Right |
| S | Stop |

---

## Project Structure

```bash
.
├── main.ino
└── README.md
```

---

## Source Code

The main implementation is located in:

```bash
main.ino
```

---

## Future Improvements

- Autonomous navigation mode
- Mobile application integration
- Line-following capability
- Camera module support
- Wi-Fi / IoT connectivity
- Battery monitoring system

---

## Author

GitHub: @ZaniTheDev
