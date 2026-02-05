---
layout: inner
title: ARUW Sentry robot
permalink: /voron02/
---

# Voron 0.2
![Voron 0.2](/img/Voron0.2/voron_no_tophat.jpg)

Below documents the process of my build of the Voron 0.2 and helpful resources I found.

## Formbot Kit
I used [this formbot kit](https://www.formbot3d.com/products/voron-v02-corexy-3d-printer-kit-with-high-quality-parts?VariantsId=11024). 

The kit itself contained all the parts I needed. All of the wires were pre-crimped, packaged separately and labeled clearly, and there were foam cutouts to house each component. The pre-cut and crimped wires gave me less flexibility on electronics placement because the wire lengths were fixed.

#### Filament
For filament, I used Polymaker ASA in Natural and Army Green. I used [this website](www.3dprinter-color-configurator.com/voron-color-configurator.html) to help me visualize my color combinations.

- [Print settings](https://docs.vorondesign.com/sourcing.html)
- [Printed parts list](https://docs.google.com/spreadsheets/d/1MSgTiXazJwyfcTe7QqNIMWwQ_lfM8cOXmiMWPZ2HkEI/edit?gid=0#gid=0)

## Mechanical Assembly
The mechanical assembly of the Voron 0.2 was fairly self-explanatory, as Voron has extensive [documentation](https://docs.vorondesign.com/) and a clear [manual](https://raw.githubusercontent.com/VoronDesign/Voron-0/Voron0.2/Manuals/VORON_V0.2_Assembly_Manual.pdf). 


The Formbot kit contained two mods: the kirigami bed and umbillical cord. Both are popular community mods but aren't reflected in the manual. 

- [Kirigami bed](https://docs.vorondesign.com/) 
- [Umbilical](https://github.com/VoronDesign/Voron-Hardware/tree/master/V0-Umbilical)

Before starting, it's recommended to regrease your linear rails, which involves cleaning it with isopropyl alcohol and adding your own grease to it. The grease that comes with the linear rail is just to protect it during transit, but we want to replace it with better quality grease. I used the Super Lube 21030, but any lube with NLGI Grade 1 or 2 should work. 

- [Youtube video on process](https://www.youtube.com/watch?v=UYvhYjkBFTY)
- [LDO motors documentation](https://docs.ldomotors.com/en/guides/rail_grease_guide)
- [Amazon link to lube](https://www.amazon.com/dp/B000XBH9HI?ref=ppx_yo2ov_dt_b_fed_asin_title&th=1)

The Formbot kit contained all the parts I needed, but I had to get tools (allen key set, multimeter) for the build. I also purchased a linear rail because I accidentally slid off the carriage from the rail and lost a lot of the ball bearings. 

## Wiring
Wiring was also fairly self-explanatory, as the pinouts for the BTT SKR Pico and BTT Pi are both available on the BTT GitHub. The wires were crimped and labeled, which made the process a lot easier. I checked my progress along the way using my multimeter, and turned on and tested the SKR Pico before connecting it to the Pi. 

- [SKR Pico Pinout](https://docs.vorondesign.com/build/electrical/v02_skr_pico_wiring.html)
- [SKR Pico Github](https://github.com/bigtreetech/SKR-Pico/blob/master/BTT%20SKR%20Pico%20V1.0%20Instruction%20Manual.pdf)
- [Wiring Diagram by SrgntBallistic](https://raw.githubusercontent.com/SrgntBallistic/Formbot-V0/v0.2/Images/Wiring/formbot-voron-v0.2r1-kit-wiring-diagram.png)

## Software Config
It was the roughest part for me, but there are plenty of resources online.
- [Klipper Web Interfaces](https://docs.vorondesign.com/build/software/)
- [Klipper Flashing](https://github.com/bigtreetech/SKR-Pico/tree/master/Klipper)
- [Klipper Flashing (more)](https://docs.vorondesign.com/build/software/skrPico_klipper.html)
- [Linux Terminal SSH](https://docs.vorondesign.com/build/software/ssh.html)
- [V0 Display](github.com/VoronDesign/Voron-Hardware/blob/master/V0_Display/Documentation/Setup_and_Flashing_Guide.md)

## Tuning



## Resources
[Tuning guide](https://ellis3dp.com/Print-Tuning-Guide/articles/misconceptions.html)
[Voron 0.2 Github](https://github.com/VoronDesign/Voron-0/tree/Voron0.2r1)
