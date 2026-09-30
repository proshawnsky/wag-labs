---
title: "MATLAB Speech-to-Piano"
date: 2026-05-18
draft: false
tags: ["matlab", "dsp", "fft", "audio"]
cover:
  image: "/wag-labs/images/speech-to-piano/Mapped%20to%20Piano%20Keys.png"
  alt: "Piano key press timing and volumes"
  relative: false
---

## Overview
A MATLAB experiment that reconstructs spoken audio using only the 88 frequencies available on a piano.

- Performs an FFT on audio files, discretizes the frequencies, and applies temporal smoothing
- Reconstructs and replays audio using only the 88 available frequencies on a piano
- Spoken words are easily discernible
- Currently attempting to convert results into legible sheet music

![Audio File](/wag-labs/images/speech-to-piano/Audio%20File.png)
*Audio File*

![Mapped to Piano Keys](/wag-labs/images/speech-to-piano/Mapped%20to%20Piano%20Keys.png)
*Mapped to Piano Keys*
