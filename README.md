# CAN-Bus-Example

This repository will hold all CAN bus code as well as links to important information.
<br />

/***************
5/30/2017
***************/
<br />
Pi/PC/Laptop Options:
<br />
- CAN Controller with SPI interface (ex. MCP2515, this will work with socketCAN). Might need a CAN transceiver as well, depending on if the controller already has one. This will only work with the pi (without buying extra stuff). If I'm going this route it is worth considering existing solutions such as PiCAN.
<br />
- USB2CAN from 8devices. USB interface and supported by the linux kernel, so this will work with rpi and pc. Link to guide with c code at bottom https://fabiobaltieri.com/2013/07/23/hacking-into-a-vehicle-can-bus-toyothack-and-socketcan/
<br />
- A different board altogether, maybe another piccolo. Arduino w/ CAN shield http://matthewcmcmillan.blogspot.com/2013/10/arduino-sending-data-over-can-bus.html
<br />
<br />

In order to implement CAN communication between the TI piccolo mcu and a laptop, two(?) CAN transceivers are necessary. The TI piccolo might have a built in transceiver which would mean only one transceiver would be necessary. It is possible to connect to a CAN bus directly by placing a diode on the CAN RX pins as outlined here http://electronics.stackexchange.com/questions/30564/is-a-can-enabled-microcontroller-sufficient-to-drive-a-can-bus, but this limits the baud rate and bus length and is overall not ideal. Transceivers are necessary on all nodes in order to connect to the bus and handle arbitration. Along with a transceiver, the laptop will also need a USB to CAN converter. This is not necessary on the piccolo as it has an internal CAN controller exposed via GPIO's. I need to verify if these pins are actually exposed on the launchpad.
<br />

CAN tutorials:
<br />
http://www.computer-solutions.co.uk/download/Peak/CAN-Tutorial.pdf
<br />
https://www.youtube.com/watch?v=pqwqNU--IbQ
<br />

CAN Implementation on TI Stellaris:
<br />
https://github.com/murix/canbus-stellaris
<br />
http://www.fischl.de/arm/can_bus_interface_for_stellaris_launchpad/
<br />

Potential transceivers:
<br />
http://www.ti.com/product/SN65HVD230
<br />

Potential USB to CAN converters:
<br />
http://www.can232.com/?page_id=14
  - Would a transceiver still be necessary with the above module?
