# KXR.LTI "*Name TBD*" Control Panel System

This directory will contain all code related to the "*Name TBD*" Control Panel
system. This document will act as an outline for the requirements and tasks
for this system, and will be updated as needed.

###### README by KXR.LTI Back-end Software Development Team Lead [Will Serface](https://discord.com/users/609211773303652372).

___

## Summary

The Control Panel will be to provide Ground Support crew with an easy and
reliable way of interfacing with the DAQ and telemetry system. This will include
a series of switches, buttons, and LEDs that enable both information and control
to any current or future KXR flight computer or motor test stand.

### Requirements

1. Connect with DAQ/Telemetry to send commands and recieve data
2. Use a series of switches and buttons to determine what commands to send
3. Display current status of switches, buttons and rocket/stand on arrays of LEDs
4. Implement API for Front-end team to access live telemetry data
5. Ensure secure 2-way communications from all connected devices

### Hardware

There is currently no decision regarding what hardware this system will run on,
however it is very likely it will be an Arduino-based microcontroller.

___

## Tasks

### 9/28 LTI Integration Meeting

- Meet with Mechanisms and Electrical teams to brainstorm ideas for Control Panel
- Choose microcontroller according to requirements, inventory, and budget
- Determine whether to use existing API or create a new API for Front-end