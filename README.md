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
As a bare minimum an arduino aano and a RS485 driver chip are needed.
The Maxim MAX485 or Texas Instruments SN75176 are pin-identical driver chips and can be used either in a DIP8 or SO8 package on the receiving or transmitting side.
Pin one is marked by a white dot on the PCB.
The dipswitch switches its input pins to ground, so pinMode(<addrPin>, INPUT_PULLUP) should be used.
As connectors footprints for a 3-pin 5.08 mm pitch screwterminal or a XLR connector are provided.
The XLR footprint is for n Neutrik NC3MD-H (male horizontal) or a NC3FD-H (female horizontal) connector.
  
#### configuring the board

##### connecting Tx/Rx
The Tx an Rx Pins of the arduino are by default NOT connected to the driver chips and therefore nothing can be send or received.
To connect the Tx/Rx pins a solder bridge or a jumper header must be soldered on the board.
This was done because having those pins connected to the driver chips prohibits uploading a sketch.

##### configuring the output
The XLR female connector and the corresponding screwterminal can be either DMX output from the arduino or passing through the dmx input.
To decide what is does two more jumperpads most be soldered. They are labeled (solder fort XLR f = DMX Through/DMXOUT".

#### Design files
The Project was done using Kicad 6.0. You`ll find a Gerber folder in the Projekt folder that should be accepted by JLCPCB.com and other manufacturers.


