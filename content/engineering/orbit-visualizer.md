---
title: "Orbit Visualizer"
date: 2026-09-01
draft: false
cover:
  image: "/wag-labs/images/orbit_visualizer/orbit_visualizer_1.png"
  alt: "Orbit visualizer"
  relative: false
---

## Overview
As a senior project, I designed and built a 3D orbit visualizer for use as a teaching aid on orbital elements. The orbit plane (right ascension and inclination) is depicted as an articulating 3D plane, and the orbit is then drawn on the plane by one of 4 laser turrets.

The plane is controlled by two stationary motors using concentric shafts. This let me avoid using slip rings and was also a more interesting mechanism. The two motors were brushed DC motors with worm gear reductions, and each had a quadrature encoder to close the loop on position. Using tensioned high-torque belts gave the system virtually no backlash. The lasers were articulated on a pair of metal-geared digital hobby servos arranged in a pan/tilt turret. The motors, servos, and lasers were controlled by an Arduino Mega connected to a PC where the orbit parameters were input.

To locate the origin of each laser turret, I wrote an algorithm in which the user hand-jogs the laser to designated points on the plane; the code then figures out where the laser must have been given the angle deltas from the known points.

![Hand-laid circuit board](/wag-labs/images/orbit_visualizer/orbit_visualizer_1.png)
*Hand-laid circuit board*

![Completed device](/wag-labs/images/orbit_visualizer/orbit_visualizer_2.png)
*Completed device*

![Drawing a circular orbit](/wag-labs/images/orbit_visualizer/orbit_visualizer_3.png)
*Drawing a circular orbit*

![Circuit diagram](/wag-labs/images/orbit_visualizer/orbit_visualizer_4.png)
*Circuit diagram*
