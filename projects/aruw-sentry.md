---
layout: inner
title: ARUW Sentry robot
permalink: /aruw-sentry/
---

## Sentry
![Sentry CAD](/img/Sentry/CAD.png)

The 2026 Sentry robot is a fully autonomus robot with three turrets (two turret minors mounted on a turret major) and a constantly spinning chassis. The robot features a bottom fed mechanism where balls are routed up the neck of the two turret minors to be shot. The drive train is omni wheel x drive mounted on a linear suspension. The turret major houses all the major electronics, Nvidia Jetson, and LiDAR, and Arducams for vision. The chassis consists of bent box tube bumpers mounted on a box tube and carbon fiber sandwich chassis frame. 

We heavily reduced the chassis diameter and weight compared to last year. The weight is still unknown because the CAD is still in progress but we decreased the chassis diameter  from 680 to 550mm. The main reason for this is because we expanded the height of turret major down to below the agitators, which allowed it to be a smaller diameter, and the chassis below it to be smaller as well. 

### Turret Major
<img src="/img/Sentry/Major_2.png" alt="Sentry Turret Major" style="float: right; width: 400px; margin-left: 30px;" />
The turret major contains all the major electronics in the robot, serves as a base for the two turret minors, and houses the hopper, agitator and feeding system. The structure consists of a top and bottom carbon fiber plate held up by four standoffs and six M4x120 screws. The electronics are mounted vertically for easier wiring access.

<img src="/img/Sentry/Major_1.png" alt="Sentry Turret Major" style="float: left; width: 350px; margin-right: 30px;" />
The diameter is only 365mm this year (compared to about 420 past year), with the main reason being pushing the bottom plate of turret major down past the agitators. In the past, the bottom plate lat on the same plane as the top of the agitators, leaving ltos of empty space under the bottom plate. By shifting the bottom plate down, we were able to significantly decrease the diameter of turret minor, as well as mount electronics vertically which should allow for better wiring. The half of turret major without the hoppers can be accessed by removing one large cover, allowing for easy wiring, debugging and testing. 