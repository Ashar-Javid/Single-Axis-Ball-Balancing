# 🎯 Single Axis Ball Balancing System

![Project Status](https://img.shields.io/badge/status-Completed-brightgreen.svg)
![Platform](https://img.shields.io/badge/platform-Arduino-blue.svg)
![License](https://img.shields.io/badge/license-MIT-lightgrey.svg)
![PID Control](https://img.shields.io/badge/control-PID-orange.svg)

> A real-time, one-axis ball balancing robot that uses a PID controller on a microcontroller to dynamically stabilize a ball on a beam. Developed as part of the Linear Control Systems (LCS) course project.

---

## 🌀 Project Preview
![Ball Balancer](https://github.com/user-attachments/assets/1eb025ea-b224-438a-bfb2-826be1fe5811)
---

## 📦 Features

- 🧠 **PID Control** for dynamic stability.
- 🤖 **Real-time sensor feedback** using IR or ultrasonic sensors.
- ⚙️ **Servo motor-driven beam** for accurate actuation.
- 💡 **Low-cost microcontroller** implementation (Arduino/STM32).
- 📊 **Serial Monitor & LCD** integration for live debugging.

---

## 🛠️ System Architecture
![FlowDiagram](https://github.com/user-attachments/assets/8171fafc-3a85-4654-961b-a84be76296f7)

## Circuit Diagram
![Circuit](https://github.com/user-attachments/assets/31c5f5d8-cd2c-44ac-b5fe-1d6ec8b357af)

## 🔧 Hardware Components

The following hardware was selected for cost-effectiveness, precision, and ease of integration:

| Component             | Description                                                                 |
|----------------------|-----------------------------------------------------------------------------|
| **Beam**             | 30–50 cm long acrylic or wooden beam mounted on a single pivot axis         |
| **Ball**             | Lightweight ping-pong ball for reduced inertia and fast dynamic response     |
| **Servo Motor**      | SG90 (for lightweight beams) or MG996R (for higher torque requirements)      |
| **Position Sensor**  | - **IR (GP2Y0A21)**: Analog output, low noise<br>- **Ultrasonic (HC-SR04)**: Digital echo timing |
| **Microcontroller**  | - **Arduino Uno**: Easy to use, good for prototyping<br>- **STM32 Blue Pill**: Higher speed, precision |
| **Power Supply**     | 5V regulated via USB or Li-ion battery pack                                  |
| **Optional LCD**     | 16x2 I2C LCD for displaying real-time PID values, ball position, and error   |
| **Supporting Tools** | Breadboard, jumper wires, screws, brackets, bearings for pivot, etc.         |

---

## ⚙️ Control Strategy
Implemented a classic PID (Proportional-Integral-Derivative) loop:

javascript
Copy
Edit
Error = Desired Position - Actual Position

PID Output = Kp * Error + Ki * ∫Error + Kd * (dError/dt)
Kp = 5, Ki = 0.01, Kd = 9

Tuned manually and iteratively for minimal overshoot and fast response.

## 🧪 Results:
✅ Stabilized within ±5mm of the center.

🔄 Settled in ~30 seconds after disturbance.

🚫 Overshoot: Controlled under 10%.

💻 Real-time graphs observed using Arduino Serial Plotter.

## 📈 Future Enhancements
⬛ 2-axis (X-Y) platform.

🎥 Vision-based tracking using OpenCV or infrared grids.

🧠 Self-tuning adaptive PID or machine learning-based control.

📶 Wireless monitoring via Bluetooth/Wi-Fi.

🔁 Simulation-first development using MATLAB or Python.

## 👨‍🔬 Authors
1. Muhammad Ashar Javid
2. Ameer Hamza
3. Awais Asghar
4. Muhammad Hammad Sarwar

## 📄 License
This project is licensed under the MIT License.

## 🌐 References
Åström & Hägglund, Advanced PID Control, ISA.

Ogata, Modern Control Engineering, Pearson.

Arduino PID Library: PID Playground

MATLAB Control Toolbox: MathWorks Control Help!

