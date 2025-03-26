---
title: "ROS2 Autonomous Agriculture Robot Navigation with Visual Obstacle Avoidance"
excerpt: "Autonomous Agriculture Robot Navigation with NAV2 in Isaac-Sim using frontal camera for obstacle avoidance using HSV segmentation<br/><img src='/images/navigation.gif'>"
collection: portfolio
img: /images/visual_and_global_navigation.mp4
---

<img src="/images/visual_and_global_navigation.gif"/>

## Overview
This project focuses on **autonomous navigation** in an agricultural setting. The robot operates in two modes:

1. **GPS-Based Navigation (Mapped Environment)**: The robot follows a pre-mapped path using GPS localization. The assumption is that a map can be generated through drone imaging.
2. **Visual Servoing (Unmapped Terrain)**: When no prior map is available, the robot uses visual servoing with image segmentation to navigate between plants and avoid obstacles.

There is also a third mode integrating visual obstacle avoidance and global navigation but additional tuning is still required, I will come back to this.

## System Configuration
- **Simulator:** NVIDIA Isaac Sim 4.5
- **Middleware:** ROS2 Humble
- **Hardware:**
  - **GPU:** RTX 4070 (8GB VRAM)
  - **RAM:** 32GB
  - **CPU:** Intel i7

  ## Docker Setup
A **Dockerfile** is available to simplify setup. To build and run the container:
```bash
chmod u+x build.sh run.sh
./build.sh
./run.sh
```

## World Setup
<p align="center">
    <img src="/images/aerial_view.png" alt="Camera view" width="400" style="transform:rotate(90deg);"/>
</p>

As the isaacsim stage file, the one with the world environment and robot, are too large (>170MB), I will not include them in this repo. If you are interested let me known and I can share them.
Important to note that I did not developed the Nova_Carter_ROS robot file, I used from the IsaacSim tutorial.