---
name: Multi-Robot Control - Super Controller
tools: [ROS2, Unity, Zenoh, Socket.IO]
image: /assets/images/supercontroller/supercontroll_2.png
description: A centralized control interface for ROS2-based devices, enabling efficient multi-robot collaboration and remote management through a web-based application.
---

# Multi-Robot Control: Super Controller

<p class="text-center">
The project aims to develop a control interface for ROS2-based devices, enhancing interaction efficiency in multi-robot collaboration scenarios. This interface will enable users to remotely control robots in the future.
</p>

<p class="text-center">
  <img src="/assets/images/supercontroller/supercontroll_2.png" alt="Super Controller Interface" class="img-fluid rounded-lg shadow-lg">
</p>

---

## Key Components

The project encompasses the following key components:

- **1. Remote Control Software:** A web-based application designed for ROS2, prioritizing convenience. This software will allow users to access data from ROS2 devices and send control commands remotely using any computer or mobile device.
- **2. Control Commands:** The remote control software will empower managers to direct robot movements. For instance, they can modify robot routes or instruct robots to navigate to specific locations.
- **3. Real-time Data:** Sensor data from ROS2 devices will be transmitted to the remote control software in real-time. This information will be visually presented, allowing managers to intuitively understand the status of various devices and robots, facilitating timely responses when necessary.

---

## System Architecture

<p class="text-center">
  <img src="/assets/images/supercontroller/supercontroll_framework.png" alt="System Architecture Diagram" class="img-fluid rounded-lg shadow-lg">
</p>

The multi-robot communication system consists of front-end and back-end components, with data transferred between them via Socket connections. The front-end is a Unity-developed application for smartphones and tablets. This app uses the device's front camera to read AprilTags attached to robots, allowing users to select and bind the control interface to the corresponding robot.

Control commands from the front-end are sent through Socket communication to a server on a central Raspberry Pi. This server organizes all control signals before forwarding them to a Zenoh Router, which connects all robots and enables inter-robot communication.

As the laboratory robots are developed using ROS2 middleware, and both ROS2 and Zenoh are DDS systems, we can easily utilize Zenoh's Bridge DDS feature. This allows us to convert ROS messages into Zenoh format and transmit them to target robots, facilitating convenient and efficient control in multi-robot environments.

---

## Final Project Video

<div class="video my-4">
  <iframe src="https://www.youtube.com/embed/iEp8NJe1Z8A?si=giUsoE4eCEe8Wd-R&mute=1" style="border:0;" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>