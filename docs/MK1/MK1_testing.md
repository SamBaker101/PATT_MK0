# MK1 Testing and Adjustments

## Speed testing
I've been having a consistant issue where the actual time of a print is signifigantly more than the estimate given by Cura or Octoprint. I suspect that the slicer speed is not aligned with the firmware limits. To that end Ill be running a few tests and making some adjustments to try to optimize the speed. Printing a 3dBenchy using Cura "Normal" settings (0.15mm layer height)

| Test Name | Slicer Estimate| Slicer Speed | Octo Estimate | Actual Time | Notes                                                                              |
|-----------|----------------|--------------|---------------|-------------|------------------------------------------------------------------------------------|
|3dBenchy200| 49min          | 200          | 57min         | 1:28        |                                                                                    |
|3dBenchy400| 46min          | 400          | 55min         | 1:27        | Estimate and Actual barely affected by slicer speed                                |
|3dBenchy40 | 1:46           | 40           | 1:50          | 2:08        | Slicer controls speed below FW max, Estimate much more closely but still off       |

Sent Commands:
M203 X200 Y200 Z100 : Set max feedrate for each axis
M500                : Save change

My suspicion is that max feedrate in FW was still set to 80 for X and Y and 60 for Z so even at slicer speed 100 it should be faster than all three previous tests and should increase at 150 and 200 (Though the printer may not be able to handle those speeds).

| Test Name | Slicer Estimate| Slicer Speed | Octo Estimate | Actual Time | Notes                                                                              |
|-----------|----------------|--------------|---------------|-------------|------------------------------------------------------------------------------------|
|3dBenchy100| 1:00           | 100          | 1:07          | 1:33        | I expected better... That's discouraging                                           |
|3dBenchy150| 52min          | 150          | 1:00          | -           | Skipping for now                                                                   |
|3dBenchy200| 49min          | 200          | 57min         | 1:26        | I see...                                                                           |

No meaningful change... Clearly comething else (acceleration?) is still bottlenecking the speed.

Extruder max feedrate is still only 80.
The internet tells me ideal acceleration to feed rate is 10:1 to 20:1 which I'm well below.

M201 X2000.00 Y2000.00 Z300.00 E30000.00
M203 X200.00 Y200.00 Z100.00 E100.00
M500                : Save change

I only bumped the extruder slightly as I'm not sure how my hot end will respond, increased to max accelleration quite a bit.

| Test Name | Slicer Estimate| Slicer Speed | Octo Estimate | Actual Time | Notes                                                                              |
|-----------|----------------|--------------|---------------|-------------|------------------------------------------------------------------------------------|
|3dBenchy100| 1:00           | 100          | 1:11          | 1:11        | Some speed gain, Octo estimate accurate, Some Y-shifting (unclear if speed related)|
|3dBenchy150| 52min          | 150          | 1:00          | 1:05        | Some speed gain again, still not as high as expected, Some Y-shift (less though)   |
|3dBenchy200| 49min          | 200          | 57min         | 1:03        | Hmm... No Y-shift on this one though                                               |

I am now seeing soem speed gains though not nearly as high as I would expect based on the difference in speed setting between the different prints. I am now seeing some glitches introduced in the Y axis so I may need to pull back the acceleration in that direction.