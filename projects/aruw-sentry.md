---
layout: inner
title: ARUW Sentry robot
permalink: /aruw-sentry/
---


<div class="two-col">
  <div class="half">
    <h1>Sentry</h1>
    <p>The 2026 Sentry robot is a fully autonomus robot with three turrets (two turret minors mounted on a turret major) and a constantly spinning chassis. The robot features a bottom fed mechanism where balls are routed up the neck of the two turret minors to be shot. The drive train is omni wheel x drive mounted on a linear suspension. The turret major houses all the major electronics, Nvidia Jetson, and LiDAR, and Arducams for vision. The chassis consists of bent box tube bumpers mounted on a box tube and carbon fiber sandwich chassis frame. Having two turret minors are for a strategic advantage, to aim and shoot at two robots at once independently. </p>
  </div>

  <div class="half">
    <img src="/img/Sentry/CAD.png" alt="CAD ">
  </div>
</div>


## Sentry V2 - Nov 2025
![Sentry Redesign 1](/img/Sentry/SentryRedesign_drawing1.jpg){: .img-left }

![Sentry Redesign 1](/img/Sentry/SentryRedesign_drawing2.jpg){: .img-right } <br><br>


During the end of October, as we were wrapping up the full robot CAD, the rules for RMUL, RMUC, and ARCC (the North American branch of Robomasters) released. With it, they banned dual-headed sentries. They also banned reloading projectiles during the match. This required us to restructure 
With the new rules, we also took the opportunity to heavily skeletonize turret major, to optimize weight even more. 

Main changes:   
- Removed turret minor
- Hopper capacity increased from 500 to 800
- Removed most of major top plate, leaving only the minor and hopper support structure

## Sentry V1 - Aug 2025-Oct 2025
![Sentry CAD](/img/Sentry/CAD.png)

The 2026 Sentry robot is a fully autonomus robot with three turrets (two turret minors mounted on a turret major) and a constantly spinning chassis. The robot features a bottom fed mechanism where balls are routed up the neck of the two turret minors to be shot. The drive train is omni wheel x drive mounted on a linear suspension. The turret major houses all the major electronics, Nvidia Jetson, and LiDAR, and Arducams for vision. The chassis consists of bent box tube bumpers mounted on a box tube and carbon fiber sandwich chassis frame. Having two turret minors are for a strategic advantage, to aim and shoot at two robots at once independently. 

We heavily reduced the chassis diameter and weight compared to last year. The weight is still unknown because the CAD is still in progress but we decreased the chassis diameter  from 680 to 550mm. The main reason for this is because we expanded the height of turret major down to below the agitators, which allowed it to be a smaller diameter, and the chassis below it to be smaller as well. 

### Turret Major
![Sentry Turret Major](/img/Sentry/Major_2.png){: .img-right }
The turret major contains all the major electronics in the robot, serves as a base for the two turret minors, and houses the hopper, agitator and feeding system. The structure consists of a top and bottom carbon fiber plate held up by four standoffs and six M4x120 screws. The electronics are mounted vertically for easier wiring access.
![Sentry Turret Major](/img/Sentry/Major_1.png){: .img-right }

The diameter is only 365mm this year (compared to about 420 past year), with the main reason being pushing the bottom plate of turret major down past the agitators. In the past, the bottom plate lat on the same plane as the top of the agitators, leaving ltos of empty space under the bottom plate. By shifting the bottom plate down, we were able to significantly decrease the diameter of turret minor, as well as mount electronics vertically which should allow for better wiring. The half of turret major without the hoppers can be accessed by removing one large cover, allowing for easy wiring, debugging and testing. 