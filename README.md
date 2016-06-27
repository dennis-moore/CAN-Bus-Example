# CAN-Bus-Example

This repository will hold all CAN bus code as well as links to important information.
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
