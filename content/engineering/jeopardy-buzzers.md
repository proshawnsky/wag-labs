---
title: "Jeopardy Buzzers"
date: 2026-09-01
draft: false
cover:
  image: "/wag-labs/images/jeopardy_buzzers/jeopardy_1.png"
  alt: "Jeopardy-style buzzer system"
  relative: false
---

## Overview
My family enjoys watching Jeopardy and playing along with the contestants. These 3D printed buttons are connected to an Arduino which taps into the solder pads of the play/pause button of a knockoff TV remote. Now, when one of us thinks we know an answer, we press our button, which illuminates and pauses the TV. A timer starts, and that person has 5 seconds to answer. The blue button is run by a volunteer host and resumes the episode.

If another player thinks player 1's answer is wrong, they can buzz in during player 1's 5 seconds, and their light will illuminate once player 1's time expires. Subsequent players can join the guessing order by buzzing in. Each player can only buzz in once per question, and the blue button resets everyone's buzzers.

When plugged into a serial monitor, it displays the time delay between buzzers. It's always fun to see that a player was 20 milliseconds too late on the buzzer compared to another player's initial press.

When the game is over, the buttons pack up into a small box.

![](/wag-labs/images/jeopardy_buzzers/jeopardy_1.png)

![](/wag-labs/images/jeopardy_buzzers/jeopardy_2.png)

![](/wag-labs/images/jeopardy_buzzers/jeopardy_3.png)

![](/wag-labs/images/jeopardy_buzzers/jeopardy_4.png)
