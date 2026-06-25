# 🕷️ QuadBot

> A 12-DOF Arduino-powered quadruped robot capable of autonomous walking, obstacle avoidance, and Bluetooth control.

![Arduino](https://img.shields.io/badge/Arduino-Nano-blue)
![Robotics](https://img.shields.io/badge/Project-Robotics-green)
![License](https://img.shields.io/badge/License-MIT-yellow)

## 🚀 Overview

QuadBot is a four-legged spider-inspired robot built using an Arduino Nano, 12 SG90 servo motors, and 3D-printed components. The robot can perform various movements, avoid obstacles autonomously, and be controlled wirelessly through a Bluetooth-connected Android application.

This project combines robotics, embedded systems, inverse kinematics, and wireless communication into a single platform for learning and experimentation.

---

## ✨ Features

### 🤖 Autonomous Movement
- Stand up
- Sit down
- Walk forward
- Walk backward
- Turn left
- Turn right

### 🎭 Interactive Actions
- Hand wave
- Hand shake
- Body dance

### 🚧 Obstacle Avoidance
- Detects obstacles using an HC-SR04 ultrasonic sensor
- Automatically changes direction when blocked

### 📱 Bluetooth Control
- Wireless control using HC-05/HC-06 Bluetooth module
- Android application support
- Real-time command execution

---

## 📸 Project Images

### QuadBot
![QuadBot](images/quadbot.jpg)

### Circuit Diagram
![Circuit Diagram](https://github.com/Aditya-Kushwahaa/QuadBot/blob/514b53383b6c0a228a09a8d842468cae11b98fb4/circuit_diagram.png)

---

## 🛠️ Hardware Components

| Component | Quantity |
|------------|----------|
| Arduino Nano | 1 |
| Nano IO Expansion Shield | 1 |
| SG90 Servo Motors | 12 |
| HC-SR04 Ultrasonic Sensor | 1 |
| HC-05 Bluetooth Module | 1 |
| LM2596 Buck Converter | 1 |
| 18650 Li-ion Batteries | 2 |
| 18650 Battery Holder | 1 |
| Jumper Wires | As Required |
| 3D Printed Parts | Multiple |

---

## 🧩 Robot Architecture

QuadBot consists of:

- 4 Legs
- 3 Degrees of Freedom (DOF) per leg
- 12 Servo Motors Total

Each leg contains:
- Coxa Joint
- Femur Joint
- Tibia Joint

The robot uses inverse kinematics calculations to coordinate smooth movement across all four legs.

---

## ⚙️ Operating Modes

### 1️⃣ Basic Movement Mode

Sequence:

1. Stand Up
2. Walk Forward
3. Walk Backward
4. Turn Right
5. Turn Left
6. Wave Hand
7. Shake Hand
8. Dance
9. Sit Down

---

### 2️⃣ Obstacle Avoidance Mode

Behavior:

- Continuously moves forward
- Measures distance using ultrasonic sensor
- Detects obstacles
- Steps backward
- Randomly turns left or right
- Continues navigation

---

### 3️⃣ Bluetooth Control Mode

Control the robot using an Android smartphone.

| Command | Action |
|----------|---------|
| F | Move Forward |
| B | Move Backward |
| L | Turn Left |
| R | Turn Right |
| W | Wave |
| U | Handshake |
| V | Dance |

---

## 📂 Repository Structure

```text
QuadBot/
│
├── README.md
├── LICENSE
│
├── code/
│   ├── Basic_Movement/
│   ├── Obstacle_Avoidance/
│   └── Bluetooth_Control/
│
├── images/
│   ├── quadbot.jpg
│   ├── circuit_diagram.png
│   └── assembly.jpg
│
├── docs/
│   └── Assembly_Guide.pdf
│
└── stl-files/
    ├── body_d.stl
    ├── body_u.stl
    ├── coxa_l.stl
    ├── coxa_r.stl
    ├── tibia_l.stl
    ├── tibia_r.stl
    └── femur_1.stl
```

---

## 💻 Software Requirements

- Arduino IDE
- Servo Library
- FlexiTimer2 Library
- NewPing Library

### Install Libraries

Arduino IDE:

```text
Sketch → Include Library → Manage Libraries
```

Install:

- Servo
- FlexiTimer2
- NewPing

---

## 🔌 Wiring

### Servo Pins

```cpp
const int servo_pin[4][3] = {
  {3, 4, 2},
  {6, 7, 5},
  {9, 8, 10},
  {12, 11, 13}
};
```

### Ultrasonic Sensor

```text
Trigger → D19
Echo    → D18
```

### Bluetooth Module

```text
TX → RX
RX → TX
VCC → 5V
GND → GND
```

---

## 🔋 Power System

- 2 × 18650 Li-ion Batteries
- LM2596 Buck Converter
- Output Voltage: 6V – 7V

⚠️ Never power all 12 servos directly from the Arduino Nano.

---

## 🎯 Future Improvements

- ESP32 Upgrade
- WiFi Control
- Camera Module
- Voice Commands
- AI Object Detection
- ROS Integration
- Autonomous Navigation

---

## 📚 Skills Demonstrated

- Arduino Programming
- Embedded Systems
- Robotics
- Servo Motor Control
- Bluetooth Communication
- Sensor Integration
- Mechanical Design
- 3D Printing
- Problem Solving

---

## 👨‍💻 Author

**Aditya Kushwaha**

B.Tech CSE (AI & ML)

Passionate about Robotics, Embedded Systems, AI and Automation.

---

## ⭐ Support

If you found this project useful:

⭐ Star the repository

🍴 Fork the project

📢 Share it with fellow robotics enthusiasts

---

"Building robots today, shaping the future tomorrow." 🚀
