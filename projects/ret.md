---
layout: inner
title: Rapid Everting Tamponade
permalink: /ret/
---

## Rapid Everting Tamponade
![RET](/img/RET/handheld_vessel.png)

The Rapid Everting Tamponade, or RET, is a handheld device that everts a plastic tube into a thoracic wound to occlude the wound. I worked as a part of the BioRobotics Lab to develop this. The image above is the current testing prototype, as the device is still being developed. 

### Plastic Tube Sealing 
I modified a Creality CR-30 using springs and rollers and tuned the printer to seal plastic with the hot end of the nozzle. Two 0.05mm TPU sheets and parchment paper layers above and below them are fed through the printer. 
A tube shape is first sketched in CAD, then thin extruded at a width of 1.5mm and height of 1mm. Then, the model is sliced in ideaMaker, then the gcode is modified by removing all filament extrusions and flattening Y levels to ensure better contact with the surface. 

### CR-30 modifications
<img src="/img/RET/brl_roller_1.jpg" alt="CR30 rollers" style="float: right; width: 300px; margin-left: 30px;" />
There are two rollers as a part of the design. The first one is mounted onto the side extrusions of the printer and applies pressure onto the print bed using springs. This ensures the plastic and parchment paper do not get moved around when the nozzle touches the layers. The second roller is mounted behind and slightly under the end of the belt print bed, to roll up any extra material. 
There was also a lot of tuning involved with this design. Initially, seals came out patchy and lines could be seen where the printer did each layer pass. By adjusting slicer settings (nozzle temperature, layer height, z hop, travel speed, etc) and raising the bed height, I was able to get nice, even seals on the plastic. 

### Everting Tests
We conducted eversion tests in both rigid and silicone phantoms, to test how effective the RET was at stopping blood leakage. We found that having a tube diameter slightly larger than the wound resulted in enough pressure against the walls of the wound to fully stop bleeding. 