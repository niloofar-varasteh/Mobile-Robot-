# Mobile-Robot-

# Mobile Robot Navigation (MATLAB + ROS2/ROS1)

This repository contains my implementation of a **mobile robot navigation stack** developed for academic purposes .  
It integrates **global path planning (RRT / PRM)** and **local trajectory optimization (Timed Elastic Band – TEB)** using MATLAB and ROS 2, tested both in simulation and on a real **TurtleBot 3** platform.

---

##  Overview

The goal of this project is to enable a differential-drive robot to autonomously reach a target position in a known environment while:
- avoiding static obstacles,
- respecting kinematic constraints, and
- producing smooth, feasible, and time-optimized trajectories.

The implementation follows a classical navigation pipeline:

| Stage | Description |
|--------|--------------|
| **Mapping / Environment** | Uses a pre-recorded occupancy grid of the RST Lab. |
| **Global Path Planning** | Uses **PRM** and **RRT** to compute a collision-free path from start → goal. |
| **Local Planning (TEB)** | Refines and optimizes the global path using the Timed Elastic Band approach. |
| **ROS2 Integration** | MATLAB acts as a ROS2 node publishing velocity commands and subscribing to odometry / goal topics. |

---

##  System Requirements

| Component | Version / Notes |
|------------|----------------|
| **MATLAB** | R2023a or newer with *Robotics System Toolbox* + *ROS Toolbox* |
| **ROS 2** | Humble Hawksbill (Ubuntu 22.04 / WSL2) |
| **Hardware** | TurtleBot 3 Burger / Waffle Pi (optional) |
| **Simulation** | Gazebo + RViz2 with `turtlebot3_rst_lab.launch.py` |

---



