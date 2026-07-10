---
title: "LQR Crane Sway Reducer"
date: 2026-05-22
draft: false
tags: ["simulink", "lqr", "controls", "matlab"]
cover:
  image: "/wag-labs/images/lqr-crane/Animation.png"
  alt: "Gantry crane pendulum animation"
  relative: false
---

## Overview
An LQR controller that reduces cable sway as a gantry crane moves its payload to a target location.

- Dynamics modeled and then linearized using the Simulink linearizer
- LQR controller tuned to reduce cable sway as the gantry moves to a target location

![Controller](/wag-labs/images/lqr-crane/Controller.png)
*Controller*

![Animation](/wag-labs/images/lqr-crane/Animation.png)
*Animation*
