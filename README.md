# 🌿 Plant Hopper

> **Demo Video**

https://github.com/user-attachments/assets/7c64f9c2-c262-4401-a698-5ae2c12de1cb

---

**Smart, efficient, and adaptive watering for every plant — individually.**  
Plant Hopper intelligently targets plants using computer vision, optimized schedules, and soil moisture data, ensuring every plant gets exactly the care it needs.

<img width="854" height="697" alt="Screenshot 2025-10-07 at 12 20 19 PM" src="https://github.com/user-attachments/assets/eba1d12a-691c-497e-8d53-5543149422ea" />

---

#### Final CAD Model

![alt text](<images/Screenshot 2025-10-07 234209.png>)

### 🛠️ Hardware + Firmware
- Custom **CAD-designed turret** with **2 DOF** (pitch + base rotation)
- **AprilTag detection** to locate each plant and calculate distance + offset
- **PID alignment** with trigonometric computations for optimal water trajectory
- **Servo-controlled tunable water gun** for precision watering
- Powered by **Arduino** and controlled via **Python serial interface**

### ☁️ Cloud + Web App
- **Firebase** backend + **Next.js** frontend deployed on **Vercel**
- Robot publishes:
  - Soil moisture sensor data  
  - Computer vision snapshots for analysis  
- Web app enables remote control:
  - `Water now`
  - `Run plant scan`
  - `Get current moisture status`
- Commands execute **in real time** via a **Python threaded controller**
- Full remote monitoring — **no local setup required**

### 🧩 Python Control Layer
A **multithreaded Python system** integrates all components:
- Runs computer vision (AprilTag detection)
- Manages serial communication with the Arduino
- Handles Firebase reads/writes
- Oversees timing, alignment, and command execution
- Enables smooth, concurrent hardware + cloud operations
