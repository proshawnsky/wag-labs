---
title: "DIY Low-Cost Active 3D Motion Tracking"
date: 2026-06-03
draft: false
tags: ["motion capture", "computer vision", "3d printing", "aruco", "opencv"]
---

After using Optitrack systems in one of my graduate controls labs, I became fascinated by motion tracking cameras/algorithms and wanted to experiment with a DIY version. The basic premise is that 2 or more cameras observe the same point in 3D space and, using knowledge of their position and orientation in the room, can reconstruct the 3D coordinates of the point from their 2D views.

## Hardware

![Hardware](/wag-labs/images/motion-capture/Hardware.png)

The hardware consists of two inexpensive 120 FPS B/W IR-sensitive webcams in custom 3D-printed articulating wall mounts.

## Distortion Calibration

![Distortion Calibration](/wag-labs/images/motion-capture/Distortion%20Calibration.png)

To account for lens distortion, which causes straight edges in the real world to appear curved in photos, each camera took dozens of calibration photos of a chessboard with known dimensions from various angles and distances. The distortion observed in the chessboard squares can be undone within software. This distortion correction is then applied to all future camera outputs.

## Camera Position and Orientation

![Camera Position and Orientation](/wag-labs/images/motion-capture/Camera%20Position%20and%20Orientation.png)

To figure out exactly where each camera was located in the room and the direction they were pointing, I used an ArUco fiducial marker. A computer vision algorithm detects the unique pattern on these markers and calculates the camera's position and orientation. In this step, the camera feeds have been undistorted as seen by the edges of the frames curving inward.

## Demonstrations

The red and blue pyramids represent each camera's position, orientation, and field of view. The raw footage from each camera is shown with bright points identified using a computer vision algorithm.

## Wand Demonstration

![Wand Demonstration](/wag-labs/images/motion-capture/Wand%20Demonstration.png)

The cameras detect a single infrared LED (active marker) on the end of a stick. Each camera projects a 3D line connecting its origin to the detected bright spot in its 2D field of view. Where both 3D lines intersect is the location of the marker. In reality, the lines never perfectly intersect, so the point is taken as the midpoint of the shortest segment connecting them. This setup produces reprojection errors (shortest distance between 3D lines) of ~0.1 inches!

## 6DOF

Three active markers are arranged in a scalene right triangle, representing a vector basis. Each camera detects all 3 markers, and the triangle can be constructed in 3D using the same method above. Since the triangle has no rotational symmetry, each set of 3D points corresponds to only 1 position and orientation (6 degrees of freedom), so the object's x, y, z, roll, pitch, and yaw can be determined.

## Object Detection and Algorithm Robustness

![Object Detection and Algorithm Robustness](/wag-labs/images/motion-capture/Object%20Detection%20and%20Algorithm%20Robustness.png)

When using only 2 cameras, there is ambiguity if 2 points are collinear in a single camera's field of view. Additionally, stray light can cause false detections. To work around this, the code analyzes all possible triangles formed by near-intersections of all 3D lines. The triangle whose side lengths most closely match the known marker dimensions is taken as the actual object.
