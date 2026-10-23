# MK1 - It Prints Itself?

<img src=".\images\full_build_mk1.jpg" alt="pic" width="400"/>

## Background

The primary goal of MK1 is to move from the somewhat hacked together MK0 to a more robust and coherent platform that I can build on for future developements. This primarily involves replacing the wood panel parts with 3d printed ones. The majority of the zip ties should also be removed during this step. In adition I have added an Orange Pi to run an OctoPrint server.  

## Build Overview

The basic structure of the printer is unchanged however the brackets, carriages and clips have been replaced by 3d printed PLA parts of my own design. I have added a textured, magnetic build plate and a housing for the electronics. Additionally I added an Orange Pi to the design to run an Opctoprint server sllowing me to send or manage print jobs from anywhere on my local network with any of my devices.

## Lessons

### Vibrations in Wiring
The need for a proper wiring harness has become very clear. Aside from the asthetic issues with the current wiring it makes it very difficult to debug any connection issues and causes problems when there is a need to disconnect the electronics from the printer.

Additionally Since there is no hardpoint between the printhead and the pin connectors on the RepRap board I have encountered issues with the printhead pulling or vibrating the connectors loose during use.

### Part Flex
Some of the new parts (Particularily the z_carriages) are not sturdy enough and are flexing under tension. These will need to be redesigned and/or printed with greater/different configurations.

### Belt Tensioning
I still only have fairly rudementary belt tensioning without the ability for fine adjustment. This alongside the part flex mentioned above limits my control and causes print issues.

### Bed Leveling Issues
This issue is a hold over from MK0 which still needs further attention. I have iterated on the existing system to make it more stable and robust however it can still be difficult to use. The following issues still need attention. 

- 4 Adjustment points are being used when only 3 are required
- Bolt must be held while nut is turned
- Nuts/Bolts can be very hard to reach

It would also be incredibly useful to have some kind of feedback sensor which can be tuned and then used to reliably set the level at each corner, each time, even if this is still done manually.

## Next Steps

- Full Wiring Harnesses
- Iterate on Custom Parts 
- Mount Power Supply and Electronics Box
- Revisit Bed Leveling and Belt Tensioning Systems