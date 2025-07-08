---
name: Large-Scale Inspection System - Spot
tools: [ROS2, IsaacSim, Python, Digital Twin]
image: /assets/images/spot/spot_stair.jpg
description: An advanced autonomous inspection system for industrial monitoring, developed for TSMC utilizing Boston Dynamics' Spot, featuring multi-map navigation and a digital twin simulation.
---

# Large-Scale Inspection System: Spot

<p class="text-center">
This work presents an advanced inspection system utilizing <strong>Boston Dynamics' Spot</strong> for autonomous industrial monitoring in collaboration with <strong>TSMC</strong>. The system integrates a <strong>Routing System</strong>, <strong>Multi-Map navigation</strong>, and a <strong>digital twin simulation through NVIDIA Isaac Sim</strong> to enhance operational efficiency in large-scale environments. By combining these technologies, we establish a scalable, memory-efficient, and highly reliable framework for autonomous industrial inspection.
</p>

<p class="text-center">
  <img src="/assets/images/spot/spot_stair.jpg" alt="Spot Robot on stairs" class="img-fluid rounded-lg shadow-lg">
</p>

---

## System Framework

The inspection process begins with user-defined task assignments, which are processed by an intelligent routing system that determines optimal navigation paths. The routing system employs:

- **Traveling Salesman Problem (TSP)** for single-robot optimization
- **Multi-Agent Path Finding (MAPF)** for coordinated multi-robot navigation

Once optimal routes are established, the navigation commands are relayed to the multi-map navigation system, which facilitates seamless movement across different factory sections.

<p class="text-center">
  <img src="/assets/images/spot/switch_map_framework.png" alt="System Framework Diagram" class="img-fluid rounded-lg shadow-lg">
</p>

---

## Map Switching System

Large factory environments pose challenges in handling comprehensive maps. To address this, we developed a map-switching system utilizing AprilTag markers as positional reference points. This system:

- **Optimizes memory usage** by eliminating the need to load an entire large-scale map.
- **Enhances scalability**, enabling efficient expansion of mapped areas.
- **Ensures precise localization**, with AprilTags setting Spot’s initial pose after each transition.

By partitioning large spaces into manageable sub-maps and leveraging AprilTag-assisted positioning, we enable reliable and efficient navigation throughout extensive factory environments.

<div class="row my-4">
  <div class="col-md-6">
    <img src="/assets/images/spot/map1.png" alt="Map Area 1" class="img-fluid rounded-lg shadow-lg mb-3">
  </div>
  <div class="col-md-6">
    <img src="/assets/images/spot/map2.png" alt="Map Area 2" class="img-fluid rounded-lg shadow-lg mb-3">
  </div>
</div>
<p class="text-center">
  <img src="/assets/images/spot/apriltag_localize.png" alt="AprilTag for Localization" class="img-fluid rounded-lg shadow-lg" style="max-width: 400px;">
</p>

---

## 3D LiDAR Localization

Spot employs an onboard 3D LiDAR sensor to continuously scan its surroundings, generating high-resolution point cloud data. This real-time data is cross-referenced with pre-established environmental maps using the **3D Normal Distributions Transform (NDT)** algorithm for robust and precise localization.

<div class="row my-4">
  <div class="col-md-6">
    <img src="/assets/images/spot/spot_lidar_localization.png" alt="LiDAR Localization View 1" class="img-fluid rounded-lg shadow-lg mb-3">
  </div>
  <div class="col-md-6">
    <img src="/assets/images/spot/spot_lidar_localization2.png" alt="LiDAR Localization View 2" class="img-fluid rounded-lg shadow-lg mb-3">
  </div>
</div>

---

## System Testing

<div class="row my-4">
  <div class="col-md-6">
    <h5 class="text-center">Outdoor Testing</h5>
    <div class="video">
      <iframe src="https://www.youtube.com/embed/LI97OdDDBUY?si=qxKzRSyGzX2XXNTA&mute=1" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    </div>
  </div>
  <div class="col-md-6">
    <h5 class="text-center">Indoor Testing</h5>
    <div class="video">
      <iframe src="https://www.youtube.com/embed/IM2RIEQZuBg?si=Bo6UEO0HiOZgwEAB" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    </div>
  </div>
</div>

---

## City Science Lab Omniverse Digital Twin

Beyond physical navigation, Spot has been integrated into a digital twin environment via **NVIDIA Isaac Sim**. This enables:

- **Virtual simulation** of navigation scenarios to optimize movement strategies before deployment.
- **Real-time visualization** of waypoints and routing paths.
- **Enhanced predictive analysis**, improving operational reliability.

<div class="row my-4">
  <div class="col-md-6">
    <img src="/assets/images/spot/CSL_digital_twin_real.png" alt="Digital Twin Real World View" class="img-fluid rounded-lg shadow-lg mb-3">
  </div>
  <div class="col-md-6">
    <img src="/assets/images/spot/CSL_digital_twin_sim2.png" alt="Digital Twin Simulation View" class="img-fluid rounded-lg shadow-lg mb-3">
  </div>
</div>
<div class="video">
  <iframe src="https://www.youtube.com/embed/frTH0QERYtQ?si=ro4zKaLa2XaklL_l" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>