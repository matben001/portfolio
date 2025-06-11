# Mathieu Benoit – Project Portfolio

**Electrical & Software Engineer**  
*High Voltage Battery Design | Autonomous Systems | Embedded Control*

📍 Montreal, Canada  
📧 matben@bell.net  
🌐 [github.com/matben001](https://github.com/matben001)

---

## 🔋 High Voltage Battery System

**Objective:**  
Design a safe, efficient, and reliable 96S8P (~400 V) Li-ion battery pack with thermal management and accurate SOC estimation.

**Highlights:**
- Full pack design: cell selection, layout, thermal strategy, and HV interlocks.
- Custom **BMS firmware** on STM32F4 with **ADBMS6830** via isoSPI and FreeRTOS.
- SOC estimation using **Kalman filter** (OCV + coulomb counting).
- Thermal loss modeling using cell resistance and power output.
- Created interactive **3D heatmaps** mapped onto the STL battery casing for diagnostics.

**Tools:** STM32CubeMX, FreeRTOS, Python (Plotly, Pandas), MATLAB, SolidWorks, Altium

---

## 🚗 Autonomous Driving Software Stack

**Objective:**  
Develop a full ROS2-based autonomous pipeline for a Formula Student Driverless race car.

**System Overview:**
- **Perception:** LiDAR cone detection, GPS + IMU fusion, SLAM map generation.
- **Localization:** Real-time EKF (100 Hz) fusing LiDAR odometry, GNSS RTK, IMU.
- **Planning:**
  - Track centerline + velocity profiling.  
  - Frenet-frame **MPC** for trajectory tracking with curvature awareness.
- **Control:**
  - MPC using **CasADi + IPOPT** to minimize lateral deviation, heading error, and input effort.
  - Real-time constraints respected with failover logic.

**Testing & Validation:**
- HIL simulation using **IPG CarMaker**.
- Telemetry replay via **Foxglove** + **RViz** for debugging.

**Tools:** ROS2, CasADi, IPOPT, YAML, C++, Python

---

## 🛞 Traction Control System

**Objective:**  
Implement a dynamic traction control system using slip-ratio regulation on a rear-wheel-drive electric race car.

**Key Features:**
- Slip ratio computed from fused wheel speed and IMU-based velocity.
- PID controller to reduce torque when slip exceeds dynamically-set threshold.
- Torque limits integrated with regen and battery constraints.
- Deployed on **TI Hercules Cortex-R4** MCU, tested in dry/wet surface conditions.

**Outcome:**  
Improved acceleration, reduced wheelspin, and better tire energy efficiency.

**Tools:** HalCoGen, MATLAB, C, Python, CANalyzer

---

## 🛠️ Supplementary Tools

- **3D Telemetry Viewer:** Dash + STL rendering for thermal visualization.
- **Log Processing Tool:** Extracts, flattens, and interpolates CAN/sensor data.
- **Test Automation Suite:** Simulates sensor faults, timing jitter, and control behavior replay.

---

Feel free to explore the code and documentation for each of these systems on my [GitHub profile](https://github.com/matben001).