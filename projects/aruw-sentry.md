---
layout: inner
title: ARUW Sentry robot
permalink: /aruw-sentry/
---

## Sentry
![Sentry CAD](/img/Sentry/SentryCAD_WIP.png)

The 2026 Sentry robot is a fully autonomus robot with three turrets (two turret minors mounted on a turret major) and a constantly spinning chassis. The robot features a bottom fed mechanism where balls are routed up the neck of the two turret minors to be shot. The drive train is omni wheel x drive mounted on a linear suspension. The turret major houses all the major electronics, Nvidia Jetson, and LiDAR, and Arducams for vision. The chassis consists of bent box tube bumpers mounted on a box tube and carbon fiber sandwich chassis frame. 

We heavily reduced the chassis diameter and weight compared to last year. The weight is still unknown because the CAD is still in progress but we decreased the chassis diameter  from 680 to 550mm. The main reason for this is because we expanded the height of turret major down to below the agitators, which allowed it to be a smaller diameter, and the chassis below it to be smaller as well. 

### Turret Major
The turret major contains all the major electronics in the robot, serves as a base for the two turret minors, and houses the hopper, agitator and feeding system. I worked on the overall structure of the turret major, which consists of a top and bottom carbon fiber plate held up by four standoffs and six M4x120 screws. The electronics are mounted vertically for easier wiring access. 