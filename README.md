# DMXIOBOARD
PCB for DMX IO from an Arduino Nano via MAX485 or SN75176 chip

### Purpose
This PCB is is designed to use an Arduino Nano to either receive(and optionally loop through) DMX or send DMX via RS485 driverchips.

### Layout
All pins of the Arduino are accesible in the 5.08 mm pitch rows in the middle of the board.
For addressing the potential DMX device a dipswitch footprint is also provided.  
The pins used for the dipswitch are also connected to the center rows as well.

### Usage

#### Hardware
As a bare minimum an Arduino Nano and a RS485 driver chip are needed.
The Maxim MAX485 or Texas Instruments SN75176 are pin-identical driver chips and can be used either in a DIP8 or SO8 package on the receiving or transmitting side.
Pin one is marked by a white dot on the PCB.
The dipswitch switches its input pins to ground, so pinMode(<addrPin>,INPUT_PULLUP) should be used.

#### configuring the board




