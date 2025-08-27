---
layout: page
title: Autonomous Metro Cleaning Robot
description: Developed and validated localization and navigation strategies for an autonomous metro cleaning robot, involving extensive benchmarking of SLAM and coverage planning algorithms in a challenging real-world environment.
img: assets/img/12.jpg
importance: 1
category: work
---

This project focused on developing a robust autonomous navigation system for a mobile robot designed to clean metro train cars in Barcelona. The primary challenge was the highly symmetrical and narrow environment, which posed significant difficulties for precise localization and effective full-coverage path planning.

My work involved a rigorous benchmarking process to select the optimal software components. For localization and SLAM, I evaluated five state-of-the-art methods using a real-world dataset. After analyzing the trade-offs of Lidar Localization (NDT-OMP), GLIM, ORB-SLAM3, and RTAB-Map, **Fast-LIO** was selected for its robust, real-time performance and its ability to generate accurate maps without drift or corruption.

For path planning, I benchmarked several coverage planners. Existing solutions like Fields2Cover and the Nobleo Full Coverage Planner proved unsuitable for the metro's complex and narrow spaces. Ultimately, a **custom ROS2 wrapper for a Coverage Planner** was selected and successfully adapted to the metro's constraints by carefully tuning its parameters.

The navigation stack was built on **Nav2**, with the controller changed to the Regulated Pure Pursuit algorithm for smoother path following. Final experiments conducted in a metro carriage demonstrated the system's success, as the robot completed both obstacle avoidance and full-coverage patterns without collisions. The project concluded with a robust and validated system, and identified key areas for future improvement, including enhanced sensor redundancy and filtering to handle challenges like LiDAR occlusion and reflective surfaces.
