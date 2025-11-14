# Avy Dawgs Senior Capstone 

## Team Members 
* Aidan Leary 
* Hiram Perez 
* Dax Jennings 
* Noah Sikorski

## Project Overview 
The goal of this project is to develop a drone-based approach to avalanche search and rescue. 
This includes the development of a custom receiver for an avalanche beacon signal, the 
integration with an autonomous drone, and the modification of open-source ground control 
software.
Our final system will be configured and launched by the ground control software, will 
autonomously scan the configured search area, sending back the coordinates of victim 
locations.

Physically, the system is divided into two main subsystems: the drone, and the base station. 
The base station consists of a laptop or tablet running ground control software and a telemetry 
radio to communicate with the drone. 
The drone consists of the drone itself, a companion computer, (Raspberry Pi Zero 2 W) and our 
custom receiver.

Functionally, the base station is the end user interface, providing the ability to configure and 
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

## Design Files 
* [System Definition](https://github.com/Avy-Dawgs/system-definition)
* Receiver
    * [PCB](https://github.com/Avy-Dawgs/receiver-pcb)
    * [FPGA Firmware](https://github.com/Avy-Dawgs/receiver-fpga) 
* Companion Computer 
    * [Signal Location software](https://github.com/Avy-Dawgs/Signal-Map)
* Base Station 
    * [Custom QGroundControl](https://github.com/Avy-Dawgs/QGroundControl-Custom-Base-Station)
