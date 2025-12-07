# 🌿 Plant Hopper

> **Demo Video**

https://github.com/user-attachments/assets/5728cc32-e33f-46a7-a2b1-bc0d9ad67567

**Smart, efficient, and adaptive watering for every plant — individually.**  
Plant Hopper intelligently targets plants using computer vision, optimized schedules, and soil moisture data, ensuring every plant gets exactly the care it needs.

<img width="854" height="697" alt="Screenshot 2025-10-07 at 12 20 19 PM" src="https://github.com/user-attachments/assets/eba1d12a-691c-497e-8d53-5543149422ea" />

---

## 💡 Inspiration

Traditional watering systems like sprinklers waste up to **50%** of their water.  
They treat all plants the same — regardless of species, moisture needs, or location.

We wanted something **smarter, healthier for plants, and massively more efficient**.  
Plant Hopper solves this by individually identifying and watering each plant using **computer vision**, **PID control**, and **real-time soil moisture analysis**.

Unlike fixed-zone irrigation, our system **scales dynamically** across multiple plants using a **database-driven architecture**.

---

## ⚙️ What We Built

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

---

## 🧠 What We Learned
Building Plant Hopper required merging multiple technical disciplines:

- **Systems Integration** – combining hardware, web, and database components  
- **PID + AprilTag Control** – achieving accurate turret movement and targeting  
- **Real-Time Syncing** – maintaining consistent data flow and actuation  
- **Firebase Architecture** – structuring live robot ↔ app communication  
- **Camera Calibration** – correcting lens distortion using YAML calibration files  
- **Multithreading** – optimizing CPU utilization across multiple concurrent processes  
- **Cross-System Debugging** – bridging hardware and software reliability
