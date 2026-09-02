---
title: "Motorized Dobsonian Telescope"
date: 2026-05-25
draft: false
tags: ["simulink", "stepper motor", "telescope", "controls", "astronomy"]
cover:
  image: "/wag-labs/images/dobsonian-telescope/Actual%20Photo%20after%20Slew%20Command%20to%20Moon.png"
  alt: "Moon photographed after a slew request"
  relative: false
---

## Overview
A motorized alt-azimuth Dobsonian telescope that converts celestial ephemerides into pointing commands, modeled and controlled with Simulink.

- Driven by stepper motors with 1/256 microstepping and actively tensioned GT2 belts
- Converts celestial object ephemerides from J2000 to local Azimuth/Elevation
- Modeled the open-loop controller and plant in Simulink, including the plant, belts, and backlash
- Achieves ~10–20 arcsecond pointing accuracy (0.0027°)
- Currently working on an "inertial hold" mode that calculates tracking rates without a target

![Top-Level Simulink Model](/wag-labs/images/dobsonian-telescope/Top-Level%20Simulink%20Model.png)
*Top-Level Simulink Model*

![Telescope Plant Model](/wag-labs/images/dobsonian-telescope/Telescope%20Plant%20Model.png)
*Telescope Plant Model*

![Actual Photo after Slew Command to Moon](/wag-labs/images/dobsonian-telescope/Actual%20Photo%20after%20Slew%20Command%20to%20Moon.png)
*Actual Photo after Slew Command to Moon*
