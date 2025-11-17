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
B.S. Computer Engineering & Electrical Engineering at the University of Utah. No skiing/snowboarding 
experience, but interested in RF and circuit design. Utah native.
#### Dax Jennings 
B.S. Computer Engineering, University of Utah. Park/street skier that dabbles in backcountry skiing.

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

#### Physical Diagram
![](https://github.com/Avy-Dawgs/system-definition/blob/main/diagrams/system-diagram.drawio.svg)

### Functional Description
The base station is the end user interface, providing the ability to configure and 
launch the drone, as well as the ability to display the locations of discovered victims. 
The other important piece of the functional system is the companion computer. 
This computer performs the main logic of the design, interpreting signal strength data coming from the receiver 
along with location data coming from the drone's flight controller to find the locations of buried victims.

## Current Progress
As of now we are in the progress of testing each of our subsystems before 
we perform the final integration. 

### WiFi Signal Backup Plan
We have decided to prioritize our backup plan, which switching out our custom receiver 
for software that measures the strength of a WiFi signal. 
This allows us to test our system without having the receiver completed and integrated, 
which is the goal after this is completed.

### Drone Flight
Our drone is fully assembled, and we have done the initial testing and configuration 
in order to fly it manually. 
The next step is to fine tune the drone, and then fly it autonomously.

### Receiver
The receiver has been mostly assembled, but we have to tune our antenna, and finish up the 
FPGA firmware development before it can be tested.


## Design File Repositories 
* [System Definition](https://github.com/Avy-Dawgs/system-definition)
### Drone Subsystem
* [Drone Wiring Diagram](https://github.com/Avy-Dawgs/wiring-diagram)
* Receiver
    * [PCBs](https://github.com/Avy-Dawgs/receiver-pcb)
    * [FPGA Firmware](https://github.com/Avy-Dawgs/receiver-fpga) 
* Companion Computer 
    * [Signal Location Software](https://github.com/Avy-Dawgs/Signal-Map)

### Base Station Subsystem
* [Custom QGroundControl](https://github.com/Avy-Dawgs/QGroundControl-Custom-Base-Station)
