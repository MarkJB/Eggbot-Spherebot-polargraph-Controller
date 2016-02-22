CCNC 2015 Copyright Mark Benson etc etc

This is my Arduino Nano/Stepstick Eggbot/Shperebot/Polargraph control board. The reason this uses an Arduino Nano and external stepstick drivers is that they can be found on ebay for not much money and I wanted this to be an affordable way to build the electronics for various drawing machines.

This has been used sucessfully with a 3d printed Eggbot and Polargraph. Firmwares adapted for this board available in github.com/markjb.

BoM:
| QTY | Description |
| 1 | PCB |
| 1 | Arduino Nano |
| 2 | Stepstick stepper motor driver boards (DRV8825 or A4988) |
| 2 | 100uF 35v Electrolitic Capacitor |
| 4 | 8 way female header |
| 2 | 15 way female header (these are hard to come by, but 16 way headers are much easier to find and work if you cut off one of the end pins) |
| 1 | 6 way male header |
| 4 | 4 way male header |
| 1 | 3 way male header |
| 1 | 2 way male header |
| 1 | 2 way jumper |
| 1 | DC socket |

EXT PWR = External Power. Enables or disables powering the Arduino from the DC supply. I've had a few Arduino Nano clones go up in smoke when used with both external and USB power. Leave the jumper off EXT PWR unless you have a really good reason for wanting to power the Arduino from the DC supply. I had hoped to be able to enable the SPI SD card and load the command queue onto that and run long Polargrapgh drawings from that on DC power alone, but there are issues with firmware size.

End stops are optional. Might be useful on an Eggbot/Spherebot.

Designed in Kicad and custom kicad libs included.

![PCB](https://github.com/MarkJB/Eggbot-Spherebot-Polargraph-Controller/blob/master/drv8825_arduino_pro_pcb.png?raw=true)
