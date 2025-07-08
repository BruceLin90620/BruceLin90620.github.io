---
name: Bio-Inspired Robot - Triceratops (VSLAM)
tools: [ROS2, VSLAM, Nav2, AprilTag]
image: /assets/images/triceratops/portfolio_triceratops.jpg
description: This project enhanced the Triceratops robot's environmental awareness for autonomous indoor mobility by integrating a Realsense D435 depth camera with Nvidia Isaac ROS VSLAM and AprilTag SLAM technologies.
---

# Bio-Inspired Robot: Triceratops (VSLAM)

<p class="text-center">
To enable autonomous and safe indoor mobility for the robot, we enhanced its environmental awareness by implementing a Realsense D435 depth camera. Through the integration of Nvidia Isaac ROS VSLAM and AprilTag SLAM technologies, the robot gained the ability to create real-time environmental maps and accurately determine its position.
</p>

<div class="video my-4">
  <iframe src="https://www.youtube.com/embed/dL-FF7bwwxU?si=c8tTuZ_QIrHJG_Ez" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

---

## Isaac ROS VSLAM

The Triceratops robot employs an Intel RealSense D435 depth camera with Isaac ROS Visual SLAM for real-time localization. This stereo vision system, combined with the robot's IMU sensor, enables precise Visual-Inertial Odometry through GPU-accelerated feature matching. The solution provides reliable odometry and simultaneous mapping, ideal for GPS-limited indoor environments.

<p class="text-center">
  <img src="/assets/images/triceratops/isaac_ros_vslam.gif" alt="Isaac ROS VSLAM in action" class="img-fluid rounded-lg shadow-lg">
</p>

---

## AprilTag Localization System & Nav2

The AprilTag localization system determines the robot's position through coordinate transformations. When an AprilTag is detected, the system uses the **base_to_tag** transform (from camera detection) and the **map_to_tag** transform (from pre-configured map data) to calculate its precise location.

The Triceratops robot also integrates ROS 2's Nav2 navigation framework, utilizing a DWB (Dynamic Window Based) local planner for real-time obstacle avoidance and a global planner to calculate optimal routes.

<p class="text-center">
  <img src="/assets/images/triceratops/apriltag_localization_test.gif" alt="AprilTag Localization Test" class="img-fluid rounded-lg shadow-lg">
</p>

---

## Demo Videos

<div class="row my-4">
  <div class="col-md-6">
    <h5 class="text-center">Triceratops Moving Video</h5>
    <div class="video">
      <iframe src="https://www.youtube.com/embed/M36GWAr3caM?si=r3bjtizAE_vnXU75&mute=1" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    </div>
  </div>
  <div class="col-md-6">
    <h5 class="text-center">Visual Navigation Demo Video</h5>
    <div class="video">
      <iframe src="https://www.youtube.com/embed/IC6jLG2WF_c?si=9k66eLOwUuANwsE8" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    </div>
  </div>
</div>