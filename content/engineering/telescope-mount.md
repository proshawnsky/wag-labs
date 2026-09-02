---
title: "Motorized Telescope Mount"
date: 2026-06-03
draft: false
tags: ["astrophotography", "stepper motor", "3d printing", "embedded", "telescope"]
cover:
  image: "/wag-labs/images/telescope%20mount/mount.jpeg"
  alt: "Jupiter captured with motorized telescope mount"
  relative: false
---

Proper astrophotography requires long-exposures and therefore a mechanism to track celestial objects as the Earth's rotation causes them to move across the sky. To achieve this, I upgraded our telescope's equatorial mount with a motorized tracking system.

![Mount](/wag-labs/images/telescope%20mount/mount.jpeg)

## Mechanical Design

I designed and 3D printed a stepper motor bracket to drive our telescope's Right Ascension (RA) axis using a timing belt. A tensioning screw, held by a captive nut added during the 3D print, tensions the belt by pivoting the entire bracket assembly.

![Casing](/wag-labs/images/telescope%20mount/casing.jpeg)

## Electronics

I fabricated a control board which sends discrete motor step commands separated by a calibrated number of microseconds in order to achieve the correct tracking rate. With 64:1 microstepping, the 2:1 belt reduction, and the 144:1 RA axis worm gear reduction, the system delivers a step resolution of 0.35 arcseconds (0.000098 degrees) — over 100x smaller than Jupiter's typical angular diameter.

![Components](/wag-labs/images/telescope%20mount/components.jpeg)

![Wiring](/wag-labs/images/telescope%20mount/wiring.jpeg)

## Results

The fine angular resolution, virtually non-existent backlash, and well-calibrated tracking rate enable crisp, long-exposure astrophotography for a fraction of the cost of commercial alternatives.

![Jupiter](/wag-labs/images/telescope%20mount/jupiter.jpeg)

![Right Ascension motor](/wag-labs/images/telescope%20mount/motorized_telescope_ra_motor.png)
*Right Ascension motor*
