---
name: Autonomous Vehicle - EVπ
tools: [ROS2, HHEV.OS, DDS, PCB Design]
image: /assets/images/evpi/evpi.jpg
description: A collaboration with Foxconn to integrate HHEV.OS into the EVπ autonomous vehicle, enhancing system security and compatibility with ROS2 navigation.
---

# Autonomous Vehicle: EVπ

<p class="text-center">
Collaborated with Foxconn on integrating HHEV.OS into the EVπ control system, ensuring compatibility with ROS2 navigation and localization while enhancing security. I was also responsible for circuit board design and fabrication, including schematic design, PCB layout, and physical production.
</p>

<p class="text-center">
  <img src="/assets/images/evpi/evpi.jpg" alt="EVπ Vehicle" class="img-fluid rounded-lg shadow-lg">
</p>

---

## HHEV.OS Integration

HHEV.OS is a middleware designed specifically for automobiles, balancing the performance of various components to achieve real-time communication and stability. It provides service containers and functions to support modules like BCM, IVI, ADAS, and VCU.

Based on DDS, HHEV.OS shares the same communication protocol as EVπ's original ROS2 system, ensuring high compatibility. We redefined the software architecture according to HHEV.OS's SOA design and reimplemented system modules like motor control, UWB, and Zed2 using HHEV.OS's API. The system now operates normally with both ROS2 and HHEV.OS running simultaneously.

<p class="text-center">
  <img src="/assets/images/evpi/motorcontrol_hhevos.jpg" alt="Motor Control with HHEV.OS" class="img-fluid rounded-lg shadow-lg">
</p>

---

## Hardware Circuit Board Production

I participated in redesigning the EVπ's circuit system architecture, creating a layered power supply system from a 36V battery to meet the different voltage requirements of various modules. My responsibilities included producing the required circuit boards, from initial schematic design (including voltage dividers, buck modules, fuses, and CAN bus modules) to PCB layout and final physical production.

<div class="row my-4">
  <div class="col-md-6">
    <img src="/assets/images/evpi/computer.jpg" alt="Computer Setup" class="img-fluid rounded-lg shadow-lg mb-3">
  </div>
  <div class="col-md-6">
    <img src="/assets/images/evpi/pcb.jpg" alt="Custom PCB" class="img-fluid rounded-lg shadow-lg mb-3">
  </div>
</div>