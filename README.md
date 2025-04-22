# 🚗 Gesture-Controlled Car Bot

## 🔍 Project Overview

This project showcases a gesture-controlled robotic car, where hand movements serve as commands to guide a bot wirelessly. It leverages Python for gesture recognition through OpenCV and MediaPipe and bridges the communication to hardware using serial and Bluetooth technologies. The aim is to create a seamless, intuitive interface for controlling robotics systems using natural hand gestures.

---

## ✨ Features

- **Dual-Hand Gesture Interface**:
  - Right hand directs motion (Forward, Reverse, Left, Right).
  - Left hand modulates speed (Slow, Medium, Fast).
- **Real-Time Video Processing**: Utilizes MediaPipe's hand landmark model for precise gesture tracking.
- **Wireless Communication**:
  - Serial communication between Python and Arduino.
  - Bluetooth data transmission between Arduinos.
- **Modular Code Design**:
  - Independent scripts handle gesture detection, signal dispatch, and bot actuation.

---

## 🧰 Tech Stack

- **Software**:
  - Python (OpenCV, MediaPipe, PySerial, Threading)
- **Hardware**:
  - Arduino UNO x2
  - Bluetooth HC-05
  - L298N Motor Driver
  - USB Webcam
  - 4-Wheel Drive Chassis with DC Motors
- **Protocols**:
  - USB Serial for PC-Arduino communication
  - UART Bluetooth for inter-Arduino communication

---

## 🔁 System Workflow

1. **Gesture Recognition (Python Script)**:
   - Captures webcam feed.
   - Identifies hand posture and finger orientation.
   - Encodes directions and speed into alphanumeric commands.

2. **Serial Data Transmission**:
   - Commands sent from Python to Arduino via USB serial interface.

3. **Bluetooth Relay**:
   - Arduino with `sending_signal.ino` forwards commands wirelessly to the receiver Arduino.

4. **Bot Command Execution**:
   - Arduino with `car_code.ino` interprets the signals and drives motors accordingly.

---

## ✅ Conclusion

This car bot project exemplifies an innovative blend of computer vision and embedded systems for real-time robotic control. The gesture interface not only enhances user interaction but also paves the way for developing assistive technologies and educational tools. Future improvements could include sensor-based obstacle avoidance, enhanced gesture models, and integration with mobile platforms.

---

## 📂 File Overview

```plaintext
optimized.py            # Gesture recognition and command generation
sending_signal.ino      # Arduino TX - Bluetooth sender
car_code.ino            # Arduino RX - Bot control logic
README.md               # Project documentation
