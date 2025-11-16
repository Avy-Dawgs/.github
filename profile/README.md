# Avy Dawgs Avalanche Search Drone Senior Capstone
Our goal is to create a drone that demonstrates autonomous 
location identification of avalanche beacon signals.
We aim to show that this technology can improve the current 
standard avalanche search and rescue procedure, potentially 
saving lives.

## Team Members 
#### Aidan Leary 
B.S. Computer Engineering student at the University of Utah. 
Avid skier that grew up ski racing in New Hampshire before moving to 
Utah for college and developing an interest in backcountry and big mountain 
skiing.

#### Hiram Perez 
#### Dax Jennings 
#### Noah Sikorski

## Project Overview 
The user will configure a search area on a laptop or tablet running ground control software and 
will use this software to launch the drone.
The drone will autonomously scan the configured search area and will send back RSSI readings which 
will create a heatmap on the ground control software's map. 
The drone will also determine the victim locations algorithmically, sending these coordinates back to the 
ground control software.
The user can use the heatmap to manually identify victim locations, or they can use automated 
victim locations.

### Physical Description
The system is divided into two main subsystems: the drone, and the base station. 
The base station consists of a laptop or tablet running ground control software and a telemetry 
radio to communicate with the drone. 
The drone consists of the drone itself, a companion computer, (Raspberry Pi Zero 2 W) and our 
custom receiver.
![](https://github.com/Avy-Dawgs/system-definition/diagrams/system-diagram.drawio.svg)

### Functional Description
The base station is the end user interface, providing the ability to configure and 
launch the drone, as well as the ability to display the locations of discovered victims. 
The other important piece of the functional system is the companion computer. 
This computer performs the main logic of the design, interpreting signal strength data coming from the receiver 
along with location data coming from the drone's flight controller to find the locations of buried victims.

## Current Progress
As of now we are in the progress of testing each of our subsystems before 
we perform the final integration. 
Our drone has all the hardware that we need to fly it autonomously, we just have some configuration to 
do before we test. 
The receiver has been mostly assembled, but we have to tune our antenna, and finish up the FPGA firmware 
development before it can be tested.

We have decided to focus on our backup plan for signal strength measuring, which is to measure WiFi 
signals, so that we have a working demonstration. 
Once we have demonstrated the system working with this approach, we will work on integrating our 
custom receiver into the system.

## Design File Repositories 
* [System Definition](https://github.com/Avy-Dawgs/system-definition)
* [Drone Wiring Diagram](https://github.com/Avy-Dawgs/wiring-diagram)
* Receiver
    * [PCB](https://github.com/Avy-Dawgs/receiver-pcb)
    * [FPGA Firmware](https://github.com/Avy-Dawgs/receiver-fpga) 
* Companion Computer 
    * [Signal Location software](https://github.com/Avy-Dawgs/Signal-Map)
* Base Station 
    * [Custom QGroundControl](https://github.com/Avy-Dawgs/QGroundControl-Custom-Base-Station)
