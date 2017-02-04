---
published: true
title: Quadrupedes
layout: post
image: /imgs/atat.jpg
redirect_from: /projects/quadrupedes
---

In early 2016, I teamed up with Thierry, a colleague from Airbus, to prototype a small quadrupede robot. The idea was to build a sophisticated (but low-cost) platform for teaching robotics to high-school or university students.

Quadrupedes are tricky, because they are unstable, very nonlinear and have many degrees of freedom, unlike the typical wheeled robots that dominate the market of robots for education. We do not always realize that, because walking seems so easy to us. But walking smoothly on uneven terrain requires an incredible amount of dexterity and precision.

After two months of work, we got the robot to walk and even run rather well. Unfortunately this was then the end of my sabbatical year, and I went back to work for Airbus, leaving the project a bit on the side of the road. The next step would have been to work with teachers and students to get their feedback and perfect our design.

I had already open-sourced a [robot simulator](https://github.com/ericleib/RobotSim) built with the great [Processing](https://processing.org/) tool from MIT. The simulator allows to tune gait parameters (more than 15) in real time, in order to visualize and optimize the complex moves performed by the robot.

These moves and parameters perfectly mirror a [C++ implementation](https://github.com/ericleib/RobotCode) that runs directly in the "brain" of the robot, an Arduino DUE board. The move parameters (speed, attitude, gait,...) can all be tuned in real time, while the movement remains smooth thanks to continuous interpolation between these moves. For example, the robot can smoothly transition from standing to walking, then to turning, running, slowing down, stopping, etc...

The robot can be controlled remotely, with a smartphone, which can update any of the parameters through a Bluetooth connection. It is also possible to pre-record a sequence of moves on the robot and run them in complete open-loop mode.

The robot structure can be 3D-printed in a few hours. The robot has 12 servomotors (3 per leg), controled with PWM signals from the Arduino DUE. It weights around 500g (including the battery) and should cost between 100-150€ (parts only).

I never found time to properly document this work, which I am quite proud of (the work, not the lack of documentation)! As pictures are worth a thousand words, I post below some screenshots, animations and videos that illustrate the projects.

<div style="text-align:center;">
<img src="/imgs/robotsim.gif" alt="Robot Simulator" style="width: auto;max-width: 100%;">
<p><i>Screenshot from the Processing-based Robot simulator</i></p>
</div>

<div style="text-align:center;">
<iframe width="640" height="400" src="https://www.youtube.com/embed/nCLcqnA6c5Y">
</iframe>
<p><i>Our first prototype in action!</i></p>
</div>

<div style="text-align:center;">
<img src="/imgs/capture%20complete%202.JPG" alt="Robot CAD" style="width: auto;max-width: 100%;">
<p><i>Screenshot from the Solidworks CAD model</i></p>
</div>

<div style="text-align:center;">
<img src="/imgs/capture%20complete%20cyan.JPG" alt="Robot CAD" style="width: auto;max-width: 100%;">
<p><i>Next generation design (including force sensors on legs)</i></p>
</div>
