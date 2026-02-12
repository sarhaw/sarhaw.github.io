---
layout: inner
title: ARUW Sentry robot
permalink: /aruw-sentry/
---

<img src="/img/Sentry/CAD.png" style="max-height: 360px" alt="CAD ">

# Sentry

> *Note: This is an ongoing project. Current status is manufacturing CF plates and waterjetting aluminum sheets. Please note that some sections are currently being documented.*

---

### Table of contents 

[1. Design Requirements](#1-design-requirements) 

[2. Turret Major](#2-turret-major)

[3. V2 Changes](#3-v2-changes)

[4. Manufacturing](#4-manufacturing)

[5. Four Bar Suspension](#5-fourbar)

---

## 1. Design Requirements

The 2026 Sentry robot is a fully autonomus robot with three turrets (two turret minors mounted on a turret major) and a constantly spinning chassis. The robot features a bottom fed mechanism where balls are routed up the neck of the two turret minors to be shot. The drive train is omni wheel x drive mounted on a linear suspension. The turret major houses all the major electronics, Nvidia Jetson, and LiDAR, and Arducams for vision. The chassis consists of bent box tube bumpers mounted on a box tube and carbon fiber sandwich chassis frame. Having two turret minors are for a strategic advantage, to aim and shoot at two robots at once independently. 

However, this year the rules for the Robomaster competition got changed to allow for only one speed monitor (projectile launcher), requiring us to redo a large portion of our CAD after it was almost completed. 

Design requirements for this year include: 
- Weight savings for faster acceleration (25kg max)
- Smaller chassis diameter for faster maneuverability (600mm max)
- Deadwheel odometry 
- Climb 15 degree ramp 
- Fully autonomous

---
## 2. Turret Major

<table>
 <tr> 
  <td><img src="/img/Sentry/Major_2.png" width="250" alt="Turret Major" /></td>
  <td><img src="/img/Sentry/Major_1.png" width="250" alt="Turret Major" /></td>
  </tr>
</table>

The turret major contains all the major electronics in the robot, serves as a base for the two turret minors, and houses the hopper, agitator and feeding system. The structure consists of a top and bottom carbon fiber plate held up by four standoffs and six M4x120 screws. The electronics are mounted vertically for easier wiring access.

The diameter of turret major is only 365mm this year (compared to about 420 past year), with the main reason being pushing the bottom plate of turret major down past the agitators. In the past, the bottom plate lat on the same plane as the top of the agitators, leaving ltos of empty space under the bottom plate. By shifting the bottom plate down, we were able to significantly decrease the diameter of turret minor, as well as mount electronics vertically which should allow for better wiring. The half of turret major without the hoppers can be accessed by removing one large cover, allowing for easy wiring, debugging and testing. 

We heavily reduced the chassis diameter and weight compared to last year. The weight is now 18.6kg compared to past year's 23kg, and we decreased the chassis diameter from 680 to 585mm. One of the main reasons for this is because we expanded the height of turret major down to below the agitators, which allowed it to be a smaller diameter, and the chassis below it to be smaller as well. We also only have one turret minor instead of two. But most importantly, we kept weight savings in mind during the entire design process, opting for lighter plates when possible and doing calculations on the stresses a part will be under and need to withstand. 

---

## 3. V2 Changes

<table>
 <tr> 
  <td><img src="/img/Sentry/SentryRedesign_drawing1.jpg" width="250" alt="Sentry Redesign 1" /></td>
  <td><img src="/img/Sentry/SentryRedesign_drawing2.jpg" width="250" alt="Sentry Redesign 2" /></td>
  </tr>
</table>

During the end of October, as we were wrapping up the full robot CAD, the rules for RMUL, RMUC, and ARCC (the North American branch of Robomasters) released. With it, they banned dual-headed sentries. They also banned reloading projectiles during the match. This required us to restructure 
With the new rules, we also took the opportunity to heavily skeletonize turret major, to optimize weight even more. 

Main changes:   
- Removed turret minor
- Hopper capacity increased from 500 to 900
- Removed most of major top plate, leaving only the minor and hopper support structure

---

## 4. Manufacturing
We made sure to design for easy manufacturing and assembly. This is why most of our parts are waterjet or 3D printed, leaving only the turret major and chassis standoffs, aluminum inserts in the carbon fiber neck, the 6020 motor plate, and belt tensioners to require machine shop tools usage. We used two UW waterjets and Omax's facilities in Kent, WA for the rest of the parts. We used a mix of PLA and ASA for our 3D printed parts, defaulting to PLA and using ASA for only high stress parts.

## 5. Ballpath testing
<table>
 <tr> 
  <td><img src="/img/Sentry/suspension_assembly.jpg" width="250" alt="Sentry Redesign 1" /></td>
  <td><img src="/img/Sentry/suspension_forcemeter.jpg" width="250" alt="Sentry Redesign 2" /></td>
  </tr>
</table>

## 5. Four Bar Suspension
![fourbarsuspension](/img/Sentry/suspension_spread.jpg)

The four bar suspension was designed over summer 2025 and built in Feburary 2026. The suspension is required for our robots due to there being bumps in the game field, and the Chinese version of the game having a 2ft drop test. Otherwise, design requirements are as follows: 
- Lighter than previous year
- Smaller
- Stiffer (better stability on solid ground)
- Use less stiff springs to maintain shock quality

This design, like the previous year's, uses RC car shocks. However, although RC cars often weigh in the hundreds of grams, our robots weigh 15kg. So there is a lot more load on these shocks in this use case.
To combat this, I fit in two shocks in this year's design, to allow us to decrease the load on each individual spring by having two springs contribute to the suspension. For springs in parallel, the effective spring constant is the sum of each individual spring (as opposed to decreasing in series). 

<table>
 <tr> 
  <td><img src="/img/Sentry/suspension_assembly.jpg" width="250" alt="Sentry Redesign 1" /></td>
  <td><img src="/img/Sentry/suspension_forcemeter.jpg" width="250" alt="Sentry Redesign 2" /></td>
  </tr>
</table>