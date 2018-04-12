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
The breakout board was tested with an LT3045 with different heat sink configurations to give an estimate on the expected temperature rise. This should help with the decision whether to add a heat sink or not. The test was done using a 35 µm (1 oz./ft²) copper board. The LT3045 was configured for an 11 V output from a 13 V input running at ~500 mA.

Using a thermal imaging camera the temperature was measured and the thermal resistance was calculated using the known ambient temperature (~23 °C).

##### No Heat Sink
![LT3045 no heat sink](/images/thermal_no_heatsink.bmp)

##### Using a 25 K/W Heat Sink
![LT3045 + heat sink](/images/thermal_heatsink.bmp)
![Heat sink filed out](/images/heatsink_filed.jpg)

Dropping 2 V @ 500 mA, a Fischer Elekronik [FK 220 SA 220](http://www.fischerelektronik.de/web_fischer/en_GB/heatsinks/C02/Attachable%20heatsink/PR/FK220_SA_220_/datasheet.xhtml) heat sink was used without any thermal compound. Because of the mounting style of the pin header (contacts on the back side of the board) some slight modification of the heat sink is required. A small cutout needs to be made using a file. If the heatsink is to be attached permanetely some thermal adhesive to glue it in place is recommended.

##### Summary Table

|Heat Sink|Power Dissipated|Thermal Resistance|
|---------|----------------|------------------|
|None     |~1 W            |~44 K/W           |
|25 K/W   |~1 W            |~22 K/W           |

I do recommend using a heat sink or bolting the LT3045 PCB down onto the main PCB when running the LT3045 @ 500 mA. Although the chip is within its design specifications, running it at more than 60 °C will shorten its live and touching it can be rather unpleasant. Any small heat sink should be sufficient at room temperature, but your milage may vary.

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
