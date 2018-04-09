LT3042/LT3045 Breakout Board
===================

This repository contains the KiCAD PCB project files for a breakout board for the Linear Technologies LT3042/LT3045  ultralow noise, ultrahigh PSRR, 200/500 mA LDO regulator (http://www.linear.com/product/LT3042, http://www.linear.com/product/LT3045).

![LT3045 breakout board](/images/LT3045_breakout.png)

About
-----
This breakout board supports both the LT3042 and LT3045 LDO regulator. The package is designed as a drop-in replacement for the popular 78xx series.

The root folder contains the KiCAD files and the bill of materials, while the gerber files can be found in the [/gerber](gerber/) folder.

Thermal considerations
-----
The breakout board was tested with an LT3045 with different heatsink configurations to give an estimate on the expected temperature rise. This should help with the decision whether to add a heatsink or not. The test was done using a 35 µm (1 oz./ft²) Copper board. The LT3045 was configured for an 11 V output from a 13 V input running at ~500 mA.

Using a thermal imaging camera the temperature was measured and the thermal resistance was calculated using the known ambient temperature (~23 °C).

##### No Heatsink
![LT3045 No heatsink](/images/thermal_no_heatsink.bmp)

##### Summary Table

|Heatsink|Power Dissipated|Thermal Resistance|
|--------|----------------|------------------|
|None    |~1W             |~44 K/W           |

I do recommend using a heatsink when running the LT3045 @ 500 mA. Although the chip is within its design specifications, running it at more than 60 °C will shorten its live and touching it can be rather unpleasant.

Related Repositories
-------------
See the following repositories for more information

KiCAD footprints: https://github.com/PatrickBaus/footprints.pretty

KiCAD 3D models: https://github.com/PatrickBaus/footprints.3dshapes

KiCAD schematic libraries: https://github.com/PatrickBaus/KiCad-libraries

License
-------

This work is released under the Cern OHL v.1.2
See www.ohwr.org/licenses/cern-ohl/v1.2 or the included LICENSE file for more information.
