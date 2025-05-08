# 🤖 intelligent-robotics-project

A modular robotics project for integrating kinematics computation, simulation, and perception for the **UR5e robot arm** using a **custom kinematics pipeline** and **UOIS-Net-based object perception**. This project enables both simulation in **Gazebo** and real-world control.

---

## 📦 Project Structure
```
intelligent-robotics-project/
│
├── ir_gazebo/
│   ├── urdf/                         # URDF model for UR5e robot
│   ├── script/
│   │   ├── demo/                     # Simulation demo scripts for Gazebo
│   │   ├── main.py                   # Main controller for real robot
│   │   └── main_clustering.py        # UOIS-Net pipeline for object clustering
```

## 🛠️ Features

### ✅ Custom Kinematics Pipeline

- Parses URDF to construct the **Kinematics Tree** and **Kinematic Chain**
- Implements both:
  - **Forward Kinematics (FK)**
  - **Inverse Kinematics (IK)**
- Allows extension to non-standard robot configurations

### 🧪 Simulation (Gazebo)

- Located at: `ir_gazebo/script/demo/`
- Demonstrates UR5e robot motion using computed FK/IK
- Integrates with Gazebo to visualize robot behavior in a simulated environment

### 🤖 Real Robot Control

- Script: `ir_gazebo/script/main.py`
- Sends calculated joint commands to the physical UR5e arm
- Interfaces with custom kinematics to perform real-time actuation

### 🧠 Object Clustering with UOIS-Net

- Script: `ir_gazebo/script/main_clustering.py`
- Uses **UOIS-Net** to segment and cluster objects in real-world RGB-D input
- Returns precise object **position coordinates** for manipulation
- Supports integration with robot grasp planning

---

## 🚀 Getting Started

1. Clone the repository
   ```bash
   git clone https://github.com/your-org/intelligent-robotics-project.git