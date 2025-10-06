# IPC-System Project
Instrument Panel Cluster (IPC) for car


## I. Project Objective 
### 1. Techinical Objectives

*  **Digital instrument cluster (IPC) system:** capable of flexibly and in real time displaying vehicle information. The system will be built on a **Raspberry Pi microprocessor platform**, using the **Qt/QML framework** for graphical user interface design.

*  **Vehicle Control Unit (VCU):** The VCU will act as the **central brain**, responsible for managing the vehicle’s operating states (e.g., Off, Charging, Driving), processing data from simulated **Electronic Control Units (ECUs)**, and making decisions to control the **Human-Machine Interface (HMI)** display.

### 2. Perfomance Objectives
* **Achieve high performance**, with a system boot time of under 2 seconds and a smooth graphical interface that responds instantly to user interactions.

* **Ensure reliability and absolute accuracy** of all critical data displayed to the driver — particularly speed, energy level, and safety warnings.

* **Design the HMI** in compliance with core functional safety principles under the **ISO 26262** standard and use **internationally standardized symbols (tell-tales)** as defined in **ISO 2575**, ensuring familiarity and easy recognition for users.

* **Deliver a final product** featuring an intuitive, visually appealing interface that can **adapt flexibly to different contexts**, such as dynamically changing the display according to the driving mode (Eco, Normal, Sport).


## II. Scope
### 1. In-Scope
* **Hardware:** Design and assemble a complete hardware model including the VCU (Raspberry Pi), ECU nodes (STM32), simulated sensors (encoder, potentiometer, push buttons), and an HMI display.

* **Software:** Develop software for both main components:

    * Firmware for the ECU on STM32.
    * VCU/HMI software on Raspberry Pi using C++ and Qt/QML.

* **HMI Interface:** Develop a fully functional user interface with dedicated screens for the vehicle’s main operating modes: Driving (with Eco/Normal/Sport variants) and Battery Charging.

* **VCU Functions:** Simulate the core functionalities of a VCU, including vehicle state machine management, basic diagnostic trouble code (DTC) handling and storage, and driving mode management.

* **Testing:** Create and execute a testing plan covering different testing levels, from unit testing to full system testing.


### 2. Out-of-scope

**Standards Compliance:** The project will follow the principles of ISO 26262 but will not undergo the official certification process, which is costly and complex.

**ADAS System:** Advanced Driver Assistance System (ADAS) features—such as Adaptive Cruise Control or Lane Keeping—will not be integrated.

**Network Connectivity:** Wireless connections (Wi-Fi, Bluetooth) and cloud-based services will not be implemented.

**Physical Systems:** The project will only simulate signals from mechanical and power electronic systems (such as brakes, motor, and real battery). The actual physical systems themselves will not be developed.

## III. Hardware device and Settup Enviroment
### 1. BOM Hardware

List of equipment device in below table:

<table border="1" cellpadding="6" cellspacing="0">
  <tr>
    <th align="left">No.</th>
    <th align="left">Equipment</th>
    <th align="left">Device name</th>
    <th align="left">Quantity</th>
  </tr>
  <tr><td align="left">1</td><td align="left">VCU</td><td align="left">Pi Zero 2w (3.3V)</td><td align="left">1</td></tr>
  <tr><td align="left">2</td><td align="left">ECU</td><td align="left">STM32F415RGTX (3.3V)</td><td align="left">1</td></tr>
  <tr><td align="left">3</td><td align="left">Capture card</td><td align="left">llano 3.0 Fullhd 60Hz</td><td align="left">1</td></tr>
  <tr><td align="left">4</td><td align="left">UART to com</td><td align="left">CH340</td><td align="left">1</td></tr>
  <tr><td align="left">5</td><td align="left">Encoder 600RPM pnp type</td><td align="left">YT06-OP-600F-1M-5-24V</td><td align="left">1</td></tr>
  <tr><td align="left">6</td><td align="left">Battery sensor</td><td align="left">Potentiometer 10K Ohm</td><td align="left">1</td></tr>
  <tr><td align="left">7</td><td align="left">Button</td><td align="left">Momentary Push Buttons</td><td align="left">5</td></tr>
  <tr><td align="left">8</td><td align="left">Breadboard</td><td align="left">MB-102 400 8.5x5.5x1cm</td><td align="left">1</td></tr>
  <tr><td align="left">9</td><td align="left">Jump wire</td><td align="left">Male-female wires</td><td align="left">20</td></tr>
  <tr><td align="left">10</td><td align="left">Display wire</td><td align="left">Mini HDMI to HDMI</td><td align="left">1</td></tr>
  <tr><td align="left">11</td><td align="left">Power wire</td><td align="left">Mini USBA to USBA</td><td align="left">1</td></tr>
  <tr><td align="left">12</td><td align="left">SDCard</td><td align="left">SDCard 64Gb</td><td align="left">1</td></tr>
  <tr><td align="left">13</td><td align="left">STM32 circuit debugger</td><td align="left">STLink v2</td><td align="left">1</td></tr>
  <tr><td align="left">14</td><td align="left">Power</td><td align="left">Adapter 10 VDC</td><td align="left">1</td></tr>
  <tr><td align="left">15</td><td align="left">Power converter</td><td align="left">Power module 10V to 3.3/5V</td><td align="left">1</td></tr>
  <tr><td align="left">16</td><td align="left">Logic Shift</td><td align="left">TXS0108E 8 Channel Logic 1.4V-5.5V</td><td align="left">1</td></tr>
</table>



### 2. Setup Enviroment (in-progress)
[/IPC-System/Enviroment](https://github.com/tdzlng/IPC-System/tree/main/Enviroment)
