
## 🚗 Autonomous Vehicle System – Final Engineering Project

An intelligent autonomous vehicle designed using **Arduino Mega 2560** and **Raspberry Pi 5**, capable of **GPS-guided navigation**, **real-time human detection (YOLO)**, **multi-sensor obstacle avoidance**, and seamless switching between **manual and autonomous control** modes.


### 🚀 Key Features

**Dual Operation Modes**

* **Manual Control**: Bluetooth-enabled control via custom mobile app
* **Autonomous Mode**: GPS-based pathfinding with intelligent maneuvering

**Safety & Detection**

* **Human Detection**: Real-time person recognition using YOLO; triggers emergency stop
* **Obstacle Avoidance**:

  * **LiDAR Lite V3** for long-range detection (up to 40m)
  * **Dual HC-SR04** ultrasonic sensors for side detection
  * **Three-mode avoidance algorithm** for smart navigation
* **Visual & Audio Alerts**: LED indicators and buzzer for direction and event alerts

**Navigation System**

* **GPS Navigation**: Location tracking with ±15m accuracy
* **Compass Support**: **MPU-9250/6500** for real-time heading correction
* **Hybrid Navigation**: Inertial backup during GPS signal loss
* **Interrupt-Driven Architecture**: Ensures responsive sensor handling


### 🛠 Hardware Overview

**Controllers**

* **Arduino Mega 2560** – Core unit for motion, sensor input, and decision-making
* **Raspberry Pi 5** – Responsible for computer vision and person detection

**Sensors & Modules**

* **LiDAR Lite V3** – Precise distance measurement up to 40m
* **HC-SR04** – Ultrasonic sensors for obstacle proximity
* **Pi Camera V2** – Real-time video for YOLO detection
* **Neo-6M GPS Module** – Accurate positioning data
* **MPU-9250/6500** – 9-axis IMU for orientation and heading
* **HC-06 Bluetooth** – Wireless app communication

**Actuators & Power**

* **4x DC Motors** – Controlled independently via L293D motor shield
* **LED System** – Directional and status indication
* **Buzzer** – Destination and warning alerts
* **Portable Power** – 5V/2.1A charger for Raspberry Pi + 7.4V for motors


### 💻 Software Architecture

**Modular Arduino Firmware**

* `Autonomous_Car.ino` – Main control loop
* `CarMovement.cpp/h` – Motion logic
* `CarState.cpp/h` – Mode/state control
* `DistanceSensors.cpp/h` – Sensor readings with interrupts
* `Config.h` – Hardware and threshold configuration

**Raspberry Pi Software**

* `YOLO.py` – Human detection and safety logic

**Core Algorithms**

* **Haversine Formula** – GPS distance calculations
* **YOLOv3 Detection** – Real-time person detection at 30fps
* **State Machine** – Clean handling of control modes
* **Interrupts** – Efficient, non-blocking sensor data management


### 📱 Mobile Application

Custom-designed Bluetooth app with:

* Directional controls (forward, backward, left, right)
* Horn activation
* Manual/autonomous mode switching
* Predefined destination selection
* Real-time status and connectivity feedback

### 🎯 Project Capabilities

* Fully autonomous point-to-point navigation
* Real-time human detection with emergency braking
* Smart, responsive obstacle avoidance
* Smooth switching between control modes
* Live feedback from sensors and subsystems


### 🔧 Technical Summary

| Feature            | Specification                               |
| ------------------ | ------------------------------------------- |
| GPS Accuracy       | ±15 meters                                  |
| Obstacle Detection | 2 cm – 4 m (Ultrasonic), up to 40 m (LiDAR) |
| Camera Processing  | YOLOv3 at 30 fps                            |
| Bluetooth Range    | Up to 10 meters                             |
| Power              | 7.4V (motors), 5V/2.1A (electronics)        |

---

**Built with passion for autonomous robotics and real-time embedded systems** ❤️


