# RTI Project B - Smart Warehouse Simulation (ROS2 + Gazebo)

This project simulates a smart warehouse environment using **ROS2** and **Gazebo**, where automated guided vehicles (AGVs), robotic arms, and computer vision systems work together to classify and transport materials within a warehouse layout.

## 🚀 Project Overview

- Materials arrive at the **Inbound Dock**
- A **CV Node** classifies parts by QR tag or color
- A **Scheduler Node** assigns tasks to AGVs based on priority and status
- A **Sorting Arm** loads parts onto AGVs
- **AGVs** autonomously navigate to drop zones or storage bins
- The system includes logic for **emergency handling**, **multi-AGV coordination**, and **dynamic task assignment**

## 🧩 ROS2 Packages

| Package Name         | Purpose                                      |
|----------------------|----------------------------------------------|
| `cv_inspection`      | Camera input + QR/Color-based classification |
| `logic_controller`   | Task scheduling and state management         |
| `assembly_arm_control` | Controls final-stage robotic arm            |
| `sorting_arm_control` | Controls initial sorting robotic arm        |
| `fault_handler`      | Emergency and fault management               |
| `spawn_manager`      | Spawns parts, AGVs, and handles simulation resets |

## 📁 Folder Structure

```bash
src/
├── launch/                     # Launch files
├── worlds/                    # Gazebo world
├── models/
│   ├── arm_station/
│   ├── bins/
│   └── parts/
├── urdf/                      # Robot and arm URDF files
├── moveit_configs/
│   ├── sorting_arm_config/
│   └── assembly_arm_config/
├── config/                    # YAML config files
├── rviz/                      # RViz config
├── docs/                      # Documentation files
└── src/
    ├── cv_inspection/
    ├── logic_controller/
    ├── assembly_arm_control/
    ├── sorting_arm_control/
    ├── fault_handler/
    └── spawn_manager/
