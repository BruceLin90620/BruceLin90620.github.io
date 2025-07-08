---
name: PBL Competition - Self-Driving Car
tools: [Arduino, C++, Computer Vision]
image: /assets/images/pbl/portfolio_PBL.png
description: A collaborative project with Osaka Institute of Technology to design and build a self-driving car for an obstacle course competition.
---

# PBL Competition: Self-Driving Car

<p class="text-center">
A collaborative project between Osaka Institute of Technology, New Taipei Municipal Zhonghe Senior High School, and National Taipei University of Technology.
</p>

<div class="video my-4">
  <iframe src="https://www.youtube.com/embed/FNIiC8IVrEo?si=8LEZFYAaZcEKnRsM" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

---

## Competition Rules

The competition field features four obstacle areas at each corner: sand, grass, white rock, and a water area. There is also a high heel area in the center of the field. Competitors must navigate these obstacles while collecting as many red balls as possible.

---

## Tools & Technology

Our system utilizes:
- **Vision System:** A Pixy camera connected to an Arduino Mega board for automatic image processing and ball detection.
- **Motors:** Two 12V DC motors for driving and a 7V servo motor for the ball catcher mechanism.
- **Sensors:** An ultrasonic sensor for wall detection and obstacle avoidance.

---

## Robot Design

We designed a specialized ball collection system inspired by table tennis ball collectors. The mechanism features a rope-based catcher that efficiently transfers collected red balls to a storage container at the rear of the robot.

<p class="text-center">
  <img src="/assets/images/pbl/portfolio_PBL.png" alt="PBL Robot Design" class="img-fluid rounded-lg shadow-lg" style="max-width: 500px;">
</p>

---

## Program Flow

Our program operates in three main steps:
- **1. Wall Detection:** The ultrasonic sensor monitors wall distance and triggers turning when necessary.
- **2. Ball Tracking:** The camera centers on detected red balls through directional adjustments.
- **3. Ball Collection:** When a ball is properly aligned (Y-axis > 180 on the camera's coordinate system), the catcher mechanism activates to collect it.