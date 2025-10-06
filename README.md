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
    <th>No.</th>
    <th>Equipment</th>
    <th>Device name</th>
    <th>Quantity</th>
  </tr>
  <tr><td>1</td><td>VCU</td><td>Pi Zero 2w (3.3V)</td><td>1</td></tr>
  <tr><td>2</td><td>ECU</td><td>STM32F415RGTX (3.3V)</td><td>1</td></tr>
  <tr><td>3</td><td>Capture card</td><td>llano 3.0 Fullhd 60Hz</td><td>1</td></tr>
  <tr><td>4</td><td>UART to com</td><td>CH340</td><td>1</td></tr>
  <tr><td>5</td><td>Encoder 600RPM pnp type</td><td>YT06-OP-600F-1M-5-24V</td><td>1</td></tr>
  <tr><td>6</td><td>Battery sensor</td><td>Potentiometer 10K Ohm</td><td>1</td></tr>
  <tr><td>7</td><td>Button</td><td>Momentary Push Buttons</td><td>5</td></tr>
  <tr><td>8</td><td>Breadboard</td><td>MB-102 400 8.5x5.5x1cm</td><td>1</td></tr>
  <tr><td>9</td><td>Jump wire</td><td>Male-female wires</td><td>20</td></tr>
  <tr><td>10</td><td>Display wire</td><td>Mini HDMI to HDMI</td><td>1</td></tr>
  <tr><td>11</td><td>Power wire</td><td>Mini USBA to USBA</td><td>1</td></tr>
  <tr><td>12</td><td>SDCard</td><td>SDCard 64Gb</td><td>1</td></tr>
  <tr><td>13</td><td>STM32 circuit debugger</td><td>STLink v2</td><td>1</td></tr>
  <tr><td>14</td><td>Power</td><td>Adapter 10 VDC</td><td>1</td></tr>
  <tr><td>15</td><td>Power converter</td><td>Power module 10V to 3.3/5V</td><td>1</td></tr>
  <tr><td>16</td><td>Logic Shift</td><td>TXS0108E 8 Channel Logic 1.4V-5.5V</td><td>1</td></tr>
</table>



### 2. Setup Enviroment (in-progress)
[/IPC-System/Enviroment](https://github.com/tdzlng/IPC-System/Enviroment)
