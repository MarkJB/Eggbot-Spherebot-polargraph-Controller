CCNC 2015 Copyright Mark Benson etc etc

![PCB](https://github.com/MarkJB/Eggbot-Spherebot-Polargraph-Controller/blob/master/eggbot-spherebot-polargraph-controller_front.png)

__Note: The v2.1 board is missing a power track between U2 & U3. You will need to solder a jumper wire between the Vin pins or Stepper1 (U2) will not move!__ (This has been fixed with v2.2)

This is my Arduino Nano/Stepstick Eggbot/Shperebot/Polargraph control board. The reason this uses an Arduino Nano and external stepstick drivers is that they can be found on ebay for not much money and I wanted this to be an affordable way to build the electronics for various drawing machines.

This has been used sucessfully with a 3d printed Eggbot and Polargraph. Firmwares adapted for this board available in github.com/markjb. I've also seen it working with the Gocupi firmware.

Micro-stepping is software controlled and both steppers share the same 3 Arduino pins, so you only need configure those 3 pins to set the micro stepping for both steppers.

Assembly should be straight forward.

Orientation of U1, U2 & U3 can be determined by matching the pin names.

Orientation of C1 & C2 is negative to white half of silkscreen.

P1 & P2 (Stepper motors) are wired (from pin 1) A1, A2, B1, B2

P3 & P4 (End stops) are wired for 'Makerbot' style end stops and are wired (from pin 1) Vcc, Gnd, Gnd, Signal

P5 (Servo) is wired (from pin 1) Signal, Vcc, Gnd

BoM

| QTY | Description |
| --- | ---|
| 1 | PCB |
| 1 | Arduino Nano (U1) |
| 2 | Stepstick stepper motor driver boards (DRV8825 or A4988) (U2,U3) |
| 2 | 100uF 35v Electrolitic Capacitor (C1, C2) |
| 4 | 8 way female header (U2,U3) |
| 2 | 15 way female header (these are hard to come by, but 16 way headers are much easier to find and will work if you cut off one of the end pins) (U1) |
| 1 | 6 way female header (P7) |
| 4 | 4 way male header (P1,P2,P3,P4) |
| 1 | 3 way male header (P5) |
| 1 | 2 way male header (P6) |
| 1 | 2 way jumper (P6) |
| 1 | DC socket (CON1) |

EXT PWR = External Power. Enables or disables powering the Arduino from the DC supply. I've had a few Arduino Nano clones go up in smoke when used with both external and USB power. Leave the jumper off EXT PWR unless you have a really good reason for wanting to power the Arduino from the DC supply. I had hoped to be able to enable the SPI SD card and load the command queue onto that and run long Polargrapgh drawings from that on DC power alone, but there are issues with firmware size.

End stops are optional. Might be useful on an Eggbot/Spherebot.

Designed in Kicad 4.0.x. Custom kicad libs included.

PCBs manufactured by iTead Studios PCB prototyping service https://www.itead.cc/open-pcb/pcb-prototyping.html


