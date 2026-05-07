---
layout: inner
title: ARUW Sentry robot
permalink: /aruw-sentry/
---
<img src="/img/Sentry/Robot1.jpg" width="50" alt="Render" />

# Sentry  

<img src="/img/Sentry/Render_1.jpg" width="100" alt="Render" />
<table>
 <tr> 
  <td><img src="/img/Sentry/Render_back.png" width="250" alt="Render" /></td>
  <td><img src="/img/Sentry/Render_up.png" width="250" alt="Render" /></td>
  </tr>
</table>

---

### Table of contents 

[1. Design Requirements](#1-design-requirements) 

[2. Turret Major](#2-turret-major)

[3. V2 Changes](#3-v2-changes)

[4. Manufacturing](#4-manufacturing)

[5. Ballpath Testing](#5-ballpath)

[6. Four Bar Suspension](#6-four-bar)

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
<img src="/img/Sentry/CAD_iso.png" width="100" alt="Sentry Redesign 1" />
<table>
 <tr> 
  <td><img src="/img/Sentry/CAD_electronics.png" width="250" alt="Sentry Redesign 1" /></td>
  <td><img src="/img/Sentry/CAD_back.png" width="250" alt="Sentry Redesign 2" /></td>
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

<table>
 <tr> 
  <td><img src="/img/Sentry/Major_2.png" width="250" alt="Turret Major" /></td>
  <td><img src="/img/Sentry/Major_1.png" width="250" alt="Turret Major" /></td>
  </tr>
</table>

---

## 4. Manufacturing
<img src="/img/Sentry/waterjet_al.jpg" alt="ballpath testing" style="float: right; width: 300px; margin-left: 30px;" />

We made sure to design for easy manufacturing and assembly. This is why most of our parts are waterjet or 3D printed, leaving only the turret major and chassis standoffs, aluminum inserts in the carbon fiber neck, the 6020 motor plate, and belt tensioners to require machine shop tools usage. We used two UW waterjets and Omax's facilities in Kent, WA. 
For the rest of the parts. We used a mix of PLA and ASA for our 3D printed parts, defaulting to PLA and using ASA only for high stress parts.

We manufactured all of our carbon fiber plates ourselves. The team received donations of expired prepreg CF rolls from Boeing and the UW composites shop. Then, we: 
1. Cut the sheets into 2'x2' and 1'x1' squares in both 0 degree and 45 degree weave orientations
2. Bag the correct number of sheets of each orientation, based on the thickness of the plate
3. Store bags in freezer until layup
4. Create CF layups by stacking sheets in alternating orientations and rolling out any air in between
5. Place sheet inside platen press for ~4 hours, checking in every 30 min or when it changes phases
6. Waterjet CF sheets at Omax's facilities
7. Post-process by sealing edges with superglue and drilling out any undersized holes

<img src="/img/Sentry/cf_sheets.png" alt="ballpath testing" style="float: left; width: 300px; margin-right: 30px;" />

To track all of our parts (totalling over a thousand) we have a manufacturing tracker in notion, with each part, quantity, material, manufacturing method, and status. By constantly updating those, we know the state of our progress at all times and know how to most efficiently use our time. We also bagged all of our screws beforehand, to verify that we have all the screws that we need. 

This process is gruelling, with our squad members spending double or triple our usual meeting time in the lab during manufacturing season. But due to all of our committment, the manufacturing went as smooth as it could be. We were manufacturing so quickly that we were being blocked by the waterjet runs giving us new plates to work with. 

## 5. Ballpath Testing
<img src="/img/Sentry/ballpath_fulltest.jpg" alt="ballpath testing" style="float: right; width: 300px; margin-left: 30px;" />

The Sentry ballpath was a critical system to test before assembly. In 2025, the failure of the ballpath was a major reason why the Sentry was unable to perform well. This year, I was tasked with verifying and testing the ballpath system so we could build the robot with confidence. 

The ballpath consists of an agitator, ballpath that extends forwards then up, a GM6020 motor, the neck of the turret minor, and the firing system. The agitator is what drives the entire system, so having a short ballpath in both length and height is crucial for motor safety. The entire length of the ballpath has ptfe tubes lining the inside, to reduce friction. The only location where there aren't tubes is inside the 6020 motor, where the balls pass through the internal core. 

From CAD and what was discussed in the Sentry design reviews, the requirements for the ballpath are:
- Move balls up the ballpath at 30 Hz
- Pitch 10 degrees up, 40 degrees down
- Run without jamming for an entire match length (5 min)

Over winter break, I spent multiple long days verifying those conditions. 

<img src="/img/Sentry/ballpath_initialtest.jpg" alt="initial testing" style="float: left; width: 300px; margin-right: 30px;" />

I initially started with this simple mockup of the design. I kept as many things as possible the same as what would be on the final robot, but due to some parts being impossible to assemble without waterjet carbon fiber and aluminum plates, I modified those interfacing parts while keeping the original design as much as possible. I also segmented the test to narrow down any failure points. After fixing print defects and misalignments, the initial test fed balls through very consistently.

After that, I printed out and tested the entire ballpath, from agitator to turret minor. I had to make some janky prints in order to assemble the system, but after having the entire path printed, I marked the +10 and -30 degree pitches and started testing. It looked promising, until it noticeably failed at the extremes of its pitch. Having the full pitch range is crucial to hitting robots far across the field, on the elevated platform, or right against our bumpers. 

After analyzing the ballpath, I realized where the jam condition likely was - the firing system pitch. There, the ptfe tubes flare out to provide a seamless transition into the barrel and flywheels. However, I noticed the steep flare out angle caused the tubes to be pushed inwards in the open gap between the flared piece and the rest of the neck, which was further aggravated at the extreme angles. I made the sweeps defining the ptfe tubes less steep to see if that would help.

After testing, it did! I pushed the turret to +10 degrees and way past the -30 degrees and the balls flowed out like they were at a neutral angle. I ran the test for a couple minutes to verify consistency, for a couple trials as well. 

## 6. Four Bar Suspension
![fourbarsuspension](/img/Sentry/suspension_spread.jpg)

The four bar suspension was designed over summer 2025 and built in Feburary 2026. The suspension is required for our robots due to there being bumps in the game field, and the Chinese version of the game having a 2ft drop test. Otherwise, design requirements are as follows: 
- Lighter than previous year
- Smaller (height, width)
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

After assembling one suspension, we tested the effective spring force by hooking it to a force meter. One suspension module took 10.15kg of force to fully bottom out. Although tha, across 20mm of spring travel, was not enough energy absorption to absorb all of the energy from a drop test, our springs are not meant to do that. Otherwise a ridiculously stiff spring would be needed. That would be the role of the suspension's hard stop.

We are currently manufacturing our custom omni wheels but after that, we will characterize and test the entire system. 