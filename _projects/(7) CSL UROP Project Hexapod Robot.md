---
name: CSL UROP Project - Hexapod Robot
tools: [ROS2, SLAM, Cartographer, AprilTag]
image: /assets/images/hexapod/final_1.png
description: A comprehensive ROS2-based hexapod robot featuring LiDAR-based mapping, AprilTag tracking, and autonomous navigation, developed during the UROP program at City Science Lab.
---

# CSL UROP Project: Hexapod Robot

<p class="text-center">
A comprehensive ROS2-based hexapod robot implementation featuring LiDAR-based mapping, AprilTag tracking capabilities, and manual control interface. The system integrates autonomous navigation with visual marker following and remote operation functionality.
</p>

<div class="video my-4">
  <iframe src="https://www.youtube.com/embed/5kGbZkwkKU0?si=W-_teUgqTQTAJ9DH" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

---

## Project Background

This project was conducted as part of the Undergraduate Research Opportunity Program (UROP) at City Science Lab @ Taipei Tech, in collaboration with MIT Media Lab. While I had prior robotics experience, this marked my first venture into legged robotics and ROS2 integration. The project provided an excellent opportunity to develop a deeper understanding of Simultaneous Localization and Mapping (SLAM) and autonomous navigation systems.

---

## ROS2 Implementation & Control Interface

The initial phase involved developing Python-based control systems for the hexapod's movement, including linear and angular motion control along with stance management. I subsequently implemented a ROS2 node architecture to handle `cmd_vel` and `joy` topic subscriptions, enabling robot control through ROS2's Data Distribution Service (DDS).

<p class="text-center">
  <img src="/assets/images/hexapod/move.png" alt="Control Interface" class="img-fluid rounded-lg shadow-lg" style="max-height: 250px;">
</p>

---

## SLAM Integration

The SLAM implementation presented unique challenges, as many conventional algorithms rely on sensor fusion for optimal odometry estimation. Through extensive testing of various solutions including Lio-SAM, Gmapping, and Cartographer, I selected **Cartographer** as the most suitable option due to its robust performance without requiring external odometry sources.

<div class="row my-4">
  <div class="col-md-6">
    <img src="/assets/images/hexapod/jostick_move.png" alt="Joystick Movement for Mapping" class="img-fluid rounded-lg shadow-lg mb-3">
  </div>
  <div class="col-md-6">
    <img src="/assets/images/hexapod/rviz2_map.png" alt="RVIZ2 Map" class="img-fluid rounded-lg shadow-lg mb-3">
  </div>
</div>

---

## Navigation System

The navigation implementation required establishing a comprehensive TF tree for ROS2's Navigation2 framework. Key components include:

- **AMCL:** Adaptive Monte Carlo Localization for map-to-odometry transformations.
- **Laser Scan Matcher:** LiDAR-based odometry calculation.
- **Static Transform Publisher:** Defining spatial relationships between frames.

<div class="row my-4 justify-content-center">
  <div class="col-md-8 text-center">
    <img src="/assets/images/hexapod/nav2_rviz.png" alt="Nav2 in RVIZ" class="img-fluid rounded-lg shadow-lg mb-4">
  </div>
  <div class="col-md-4 text-center">
    <img src="/assets/images/hexapod/tf_tree.png" alt="TF Tree" class="img-fluid rounded-lg shadow-lg">
  </div>
</div>

---

## AprilTag Integration

To enhance the robot's capabilities, I implemented AprilTag-based localization and tracking. The system maintains a specified relative position to detected AprilTags, enabling dynamic target following behavior.

<div class="row my-4">
  <div class="col-md-6">
    <img src="/assets/images/hexapod/apriltag_following.png" alt="AprilTag Following 1" class="img-fluid rounded-lg shadow-lg mb-3">
  </div>
  <div class="col-md-6">
    <img src="/assets/images/hexapod/apriltag_following2.png" alt="AprilTag Following 2" class="img-fluid rounded-lg shadow-lg mb-3">
  </div>
</div>

---

## System Integration

The final implementation incorporated all developed functionalities through a priority-based control system using the `twist_mux` node to manage multiple `cmd_vel` sources:

- **Priority 1:** Joystick control (highest priority)
- **Priority 2:** AprilTag following behavior
- **Priority 3:** Autonomous navigation

The robot's operational state is indicated through LED feedback: Green for standard operation, Blue for active navigation, and back to Green upon completion.

<p class="text-center">
  <img src="/assets/images/hexapod/final_flow.png" alt="Final System Flow" class="img-fluid rounded-lg shadow-lg my-4">
</p>

<div class="row mt-4">
  <div class="col-md-4">
    <img src="/assets/images/hexapod/final_1.png" alt="Final Hexapod 1" class="img-fluid rounded-lg shadow-lg mb-3">
  </div>
  <div class="col-md-4">
    <img src="/assets/images/hexapod/final_2.png" alt="Final Hexapod 2" class="img-fluid rounded-lg shadow-lg mb-3">
  </div>
  <div class="col-md-4">
    <img src="/assets/images/hexapod/final_3.png" alt="Final Hexapod 3" class="img-fluid rounded-lg shadow-lg mb-3">
  </div>
</div>