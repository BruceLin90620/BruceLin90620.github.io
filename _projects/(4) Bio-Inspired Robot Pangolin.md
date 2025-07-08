---
name: Bio-Inspired Robot - Pangolin
tools: [ROS2, Biomimetics, Motion Control]
image: /assets/images/pangolin/curl_state.jpg
description: An educational project to develop a pangolin-inspired quadruped robot, focusing on modular system design with ROS2 to advance hands-on learning in robotics.
---

# Bio-Inspired Robot: Pangolin

<p class="text-center">
This project integrates biomimetics, software architecture, and control systems to teach students how to use the ROS2 robot operating system for modular system design. It aims to advance hands-on learning and educational tools, providing students with insights into quadruped robot applications.
</p>

<div class="video my-4">
  <iframe src="https://www.youtube.com/embed/qN7IXwsKODI?si=t2n0xto09ZLPDRxR" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

---

## Mechanical Design

We designed a two-stage quadruped robot base with a standardized chassis housing batteries and electronic control systems. The base uses seven servo motors for leg movement, head rotation, and body actuation. Its modular design allows users to easily change drive mechanisms without altering the chassis structure.

A forward underactuated leg mechanism was created using linkage combinations. This design keeps legs vertical when standing, maximizing protection, provides a cushioning effect when the robot rights itself after rolling over, and uses a swinging motion for walking.

<div class="row my-4">
  <div class="col-md-6">
    <img src="/assets/images/pangolin/mechanical.png" alt="Mechanical Design" class="img-fluid rounded-lg shadow-lg mb-3">
  </div>
  <div class="col-md-6">
    <img src="/assets/images/pangolin/curl_state.jpg" alt="Pangolin in Curl State" class="img-fluid rounded-lg shadow-lg mb-3">
  </div>
</div>

---

## Electrical Hardware Architecture

The hardware architecture integrates signals from an IMU and a Joystick, routing this information to a Raspberry Pi. This setup enables the activation and control of corresponding motor systems to achieve various intended actions such as head rotation, leg movement, and body bending.

<p class="text-center">
  <img src="/assets/images/pangolin/hardware_framework.jpg" alt="Hardware Framework Diagram" class="img-fluid rounded-lg shadow-lg">
</p>

---

## Software Architecture

The software architecture utilizes ROS2 to modularize and separate various functional components, allowing them to operate independently. Data transmission is achieved through DDS, resulting in a highly scalable and easily maintainable architecture.

We conducted systematic research to propose gait design solutions suitable for the pangolin robot, ensuring stable and smooth movement. Inverse kinematics calculations determine the required angles for each motor, ensuring precise control for the designed gait patterns.

<p class="text-center">
  <img src="/assets/images/pangolin/software_framework.jpg" alt="Software Framework Diagram" class="img-fluid rounded-lg shadow-lg">
</p>

---

## My Work

- **Software Architecture:** Architected the ROS2-based software system with modular nodes for motor control, sensor integration, and motion planning.
- **Electrical System:** Developed the complete electrical system and communication protocols between the Raspberry Pi and peripheral components.
- **Motion Control:** Implemented robot motion algorithms for walking gaits, rolling behavior, and self-righting capabilities.