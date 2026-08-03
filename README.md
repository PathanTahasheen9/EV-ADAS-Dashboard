# ⚡ EV ADAS DASHBOARD

## 📌 About the Project

The **EV ADAS Dashboard** is a real-time monitoring and safety system developed for Electric Vehicles. The project combines **STM32 embedded processing, ultrasonic sensors, ADAS logic, and a Python-based dashboard** to monitor vehicle parameters and detect surrounding obstacles.

The system provides a graphical representation of the vehicle's condition and safety status through parameters such as **speed, battery SOC, motor temperature, torque, range, obstacle distance, TTC, and blind-spot alerts**.

---

## 🎯 Objectives

- Monitor important EV parameters in real time.
- Detect obstacles around the vehicle using ultrasonic sensors.
- Provide collision warning and safety alerts.
- Calculate **Time to Collision (TTC)**.
- Implement basic **Blind Spot Detection (BSD)**.
- Display vehicle and ADAS information through a Python dashboard.

---

## 🏗️ System Architecture


```text
Ultrasonic Sensors
   Front / Left / Right
          │
          ▼
   STM32F103C8T6
          │
          ▼
 Sensor Data Processing
          │
          ▼
      ADAS Logic
   ┌──────┼──────┐
   │      │      │
  TTC   Collision  BSD
        Warning
          │
          ▼
   UART / Serial
          │
          ▼
   Python Dashboard
   ```
   
🔧 Hardware Components

Component	Purpose
STM32F103C8T6	Main processing controller
HC-SR04 × 3	Front, left and right obstacle detection
LEDs	Visual safety indication
Buzzer	Audible warning
Supporting Components	Circuit interfacing

💻 Software & Tools

STM32CubeIDE – Embedded firmware development
Embedded C – STM32 programming
PICSimLab – Hardware simulation
Python – Dashboard development
Matplotlib – Real-time data visualization
UART / Serial Communication – Data transfer

🚘 EV Parameters Monitored

The dashboard displays:

🚗 Vehicle Speed
🔋 Battery State of Charge (SOC)
⚙️ Motor Torque
🌡️ Motor Temperature
📍 Estimated Range
🦶 Accelerator Status
🛑 Brake Status
🛡️ ADAS Features
🚧 Obstacle Detection

Three ultrasonic sensors monitor the surroundings:

             FRONT
               ↓
            [Object]

       LEFT    🚗    RIGHT
      Sensor         Sensor

The measured distances are processed by the STM32 to determine the vehicle's safety condition.

⚠️ Collision Warning

The system generates different warning levels based on obstacle distance:

SAFE → ADVISORY → WARNING → CRITICAL

⏱️ Time to Collision (TTC)

TTC estimates the time available before the vehicle reaches a detected obstacle.

TTC = Distance / Relative Speed

A lower TTC indicates a higher collision risk.

👁️ Blind Spot Detection

The left and right sensors monitor the vehicle's side regions and generate alerts when an object is detected within the defined blind-spot area.

📊 Python EV ADAS Dashboard

The Python dashboard provides a centralized graphical interface.

**Left Section**

Speedometer
Current speed
Speed history

**Center Section**

Battery indicator
EV metrics
Torque
Motor temperature
Range

**Right Section**

ADAS bird's-eye view
Vehicle representation
Surrounding obstacles
TTC
Collision warnings
Blind-spot alerts
🔄 Complete Working Flow
HC-SR04 Sensors
       ↓
STM32F103C8T6
       ↓
Distance & EV Data Processing
       ↓
ADAS Decision Logic
       ↓
UART / Serial Communication
       ↓
Python Dashboard
       ↓
Real-Time Visualization
🚀 Applications
Electric Vehicle monitoring
Driver assistance systems
Obstacle detection
Collision warning
Vehicle safety monitoring
Embedded automotive applications
EV simulation and prototyping
🔮 Future Enhancements
📷 Camera-based object detection
📡 Radar/LiDAR integration
🚌 CAN communication
🤖 Machine-learning-based ADAS
📍 GPS integration
🔋 Advanced battery monitoring
🚗 Real EV hardware integration
📈 Project Outcome

The project demonstrates the integration of embedded systems, ultrasonic sensing, ADAS algorithms, serial communication, and Python visualization into a single EV monitoring and safety platform.

It provides a foundation for developing more advanced Electric Vehicle and ADAS applications.
