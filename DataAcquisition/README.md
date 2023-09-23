# KXR.LTI "*Name TBD*" DAQ & Telemetry

This directory will contain all code related to the "*Name TBD*" combined Data
Acquisition (DAQ) and Telemetry system. This document will act as an outline
for the requirements and tasks for this system, and will be updated as needed.

###### README by KXR.LTI Back-end Software Development Team Lead [Will Serface](https://discord.com/users/609211773303652372).

___

## Summary

The Data Acquisition (DAQ) and Telemetry system is vital for
monitoring and controlling the state of any rockets or test stands.
It must be able to recieve data from the Embedded Design team's FPGA
implementation to both record and send live data. This will involve decoding
a binary stream to relevant data, sending the processed data to long-term
storage, and creating or implementing an API that allows the secure transfer
of data and control for and the Front-end team's telemetry system.

### Requirements

1. Recieve raw data from the Embedded Design team's FPGA system
2. Decode raw data into relavant datatypes
3. Store processed data to long-term storage for later analysis
4. Send data from FPGA to Control Panel, and recieve commands from Control Panel
5. Ensure secure 2-way communications from all connected devices

### Hardware

There is currently no decision regarding what hardware this system will run on,
however it is very likely it will be an Arduino-based microcontroller.

___

## Tasks

### 9/25 LTI Computing Systems Meeting

- Determine hardware requirements from Embedded Design team
- Choose DAQ microcontroller according to requirements, inventory, and budget
- Determine what communication protocol to use between DAQ and Control Panel