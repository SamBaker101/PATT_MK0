# MK1 Testing and Adjustments

## Speed testing
I've been haaving a consistant issue where the actual time of a print is signifigantly more than the estimate given by Cura or Octoprint. I suspect that the slicer speed is not aligned with the firmware limits. To that end Ill be running a few tests and making some adjustments to try to optimize the speed.

| Test Name | Changeds Made        | Slicer Speed | Expected Time | Actual Time | Notes                                                 |
|-----------|----------------------|--------------|---------------|-------------|-------------------------------------------------------|
|3dBenchy200|None                  | 200          | 57min         | 1:28        |                                                       |
|3dBenchy400|Increase Slicer Speed | 400          | 55min         |             | Estimate barely affected by slicer speed            |
|3dBenchy400|Decrease Slicer Speed | 40           |               |             |       |