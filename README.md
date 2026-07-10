# Rocket Flight Data Acquisition System

## Overview
This project involves the development of a model rocket avionics system designed to collect, store, and analyze flight data. 

An initial prototype was developed to demonstrate initial technical feasibility of embedded sensor integration and flight data acquisition. Following prototype development, a formal systems engineering process is being applied to define requirements and functions, establish architecture, and conduct verificationa and validation.

---
# Project Objectives

The system is being developed to:

- Measure rocket flight altitude and acceleration
- Collect and store flight data
- Support post-flight flight performance analysis
- Demonstrate a requirements-based systems engineering workflow
  
---
# Current Project Status
**Current Phase: Verificaiton and Validation of requirements
## Completed
- ✅ Initial avionics prototype developed  
- ✅ System requirement development 
- ✅ Functional Decomposition and traceability
- ✅ System architecture development (physical architecture traceability)

## In Progress

- 🔄 Trade Studies
- 🔄 Verification and Validation (V&V)
  
---

# Prototype Overview

The initial prototype demonstrates:

- Microcontroller-based flight data acquisition
- I²C sensor communication
- SPI data storage
- Embedded flight data logging

## Prototype Hardware Configuration

| Component | Function |
|---|---|
| Raspberry Pi Pico | Flight computer |
| BMP280 | Barometric altitude sensing |
| MPU6500 | 3-axis acceleration measurement |
| MicroSD Module | Flight data storage |
| Battery System | Distributed Power source |

## Initial Prototype

<table>
  <tr>
    <td align="center">
      <strong>Prototype</strong><br>
      <img src="images/cad_proto3.png" width="250">
    </td>
    <td align="center">
      <strong>CAD Avionics Bay</strong><br>
      <img src="images/avionics_bay.png" width="250">
    </td>
    <td align="center">
      <strong>Avionics Bay</strong><br>
      <img src="images/prototype.png" width="250">
    </td>
  </tr>
</table>

---

# Systems Engineering Approach

Following initial prototype development, the system is being matured using the following structured systems engineering process:

```
System Requirements
        ↓
Functional Analysis
        ↓
Functional Allocation
        ↓
Physical Architecture
        ↓
Component Selection / Trade off Analysis
        ↓
Prototype Build
        ↓
Verification Planning (VCRM)
        ↓
Verification Testing
        ↓
Validation
```
This approach establishes traceability between system requirements, functions, components and the verification process.

---
# System Requirements

The requirements process started with operational requirements and got more refined moving to system requirements > performance requirements > component requirments. The performance requirements are listed below.

## Performance requirements

<img src="images/performance requirements.png" width="700" height="800">

---
# Functional Analysis 
After developing the performance requirements, functions were developed to satisfy the performance requirements. A functional block diagram was developed to model the function flow and point-out all interfaces.

## Functional Block Diagram
<img src="images/functional block diagram.png" width="700">

## Functional Traceability Matrix
After modeling the functions in the functional block diagram, the functions were traced to their corresponding requirements in a functional traceability matrix to ensure that all requirements are met.

<table width="100%">
  <tr>
    <td width="65%" align="center">
      <strong>Functional Traceability Matrix</strong><br>
      <img src="images/function allocation table.png" width="700">
    </td>
    <td width="35%" align="left" valign="top">
      <strong>Requirements</strong>
      <ul style="font-size: 11px; line-height: 1.2;">
        <li><strong>REQ-001:<strong> The system shall accept a user-initiated power-on command through the designated power switch.</li>
        <li><strong>REQ-002:<strong> The system shall sample atmospheric pressure at a minimum rate of 45 Hz during powered ascent, coast, and descent.</li>
        <li><strong>REQ-003:<strong> The system shall sample three-axis acceleration at a minimum rate of 45 Hz from launch detection until end of flight logging.</li>
        <li><strong>REQ-004:<strong> The system shall assign timestamps to all measurements with a resolution of ≤22.2 ms.</li>
        <li><strong>REQ-005:<strong> The system shall record all acquired timestamped sensor measurements to onboard storage.</li>
        <li><strong>REQ-006:<strong> The system shall remain fully functional after exposure to shock loads up to 15g peak acceleration and vibration representative of model rocket ignition and ascent.</li>
        <li><strong>REQ-007:<strong> The system shall support continuous operation for at least 3 minutes of active logging time.</li>
        <li><strong>REQ-008:<strong> The system shall ensure the rocket center of gravity remains at least 1.0 body diameter forward of the center of pressure for all flight configurations.</li>
      </ul>
    </td>
  </tr>
</table>

# System Architecture

## Physical Architecture

After conducting a functional analysis, the system's physical architecture was defined and components were mapped to specific functions in an architecture allocation matrix to ensure that the selected physical architecture met the defined system functions.

<strong>Physical Architecture Allocation Matrix</strong><br>

<img src="images/physical architecture.png" width="700">
---

# Verification and Testing

After determining the appropriate hardware to utilize and assembling a prototype, a systematic V&V process was conducted to ensure all of the requirments are met at the neccessary standard. Below is a verification table that highlights the verificaiton process across the system.

<table>
  <tr>
    <th>REQ ID</th>
    <th>Requirement Description</th>
    <th>Verification Method</th>
    <th>Pass / Fail Status</th>
  </tr>

  <tr>
    <td><b>REQ-01</b></td>
    <td>System accepts user ON/OFF input</td>
    <td>Demonstration</td>
    <td><span style="color:green"><b>Pass</b></span></td>
  </tr>

  <tr>
    <td><b>REQ-02</b></td>
    <td>System samples barometric pressure at 45 Hz</td>
    <td>Sensor Bench Test</td>
    <td><font color="green"><b>Pass</b></font></td>
  </tr>

  <tr>
    <td><b>REQ-03</b></td>
    <td>System samples 3-axis acceleration at 45 Hz</td>
    <td>Sensor Bench Test</td>
    <td><font color="green"><b>Pass</b></font></td>
  </tr>

  <tr>
    <td><b>REQ-04</b></td>
    <td>System timestamps data at 22.2 ms intervals</td>
    <td>Sensor Bench Test</td>
    <td><font color="green"><b>Pass</b></font></td>
  </tr>

  <tr>
    <td><b>REQ-05</b></td>
    <td>System stores data to onboard micro SD card module</td>
    <td>Sensor Bench Test</td>
    <td><font color="green"><b>Pass</b></font></td>
  </tr>

  <tr>
    <td><b>REQ-06</b></td>
    <td>System maintains function across forces up to 15g</td>
    <td>Test</td>
    <td><font color="orange"><b>Pending</b></font></td>
  </tr>

  <tr>
    <td><b>REQ-07</b></td>
    <td>Continuous data logging for 180 seconds</td>
    <td>Data Storage Test</td>
    <td><font color="green"><b>Pass</b></font></td>
  </tr>

  <tr>
    <td><b>REQ-08</b></td>
    <td>System maintains rocket CG aft of CP by 49 mm</td>
    <td>Analysis</td>
    <td><font color="orange"><b>Pending</b></font></td>
  </tr>

</table>

For a full Verification Cross-Reference Matrix (VCRM) along with the documented test results and further details, please look at the verificaiton section.  
      <p>
        <a href="Verification/verification.md">See Verification Cross-Reference Matrix (VCRM) here.</a>
        </a>
      </p>

---
# Verification and Testing 

The Sensor Bench Test assessed the performance of the avionics system prototype by turning the system on at the base of a standard 3-meter staricase and taking the system to the top of the stairscase. After briefly pausing at the top, the system prototype decended 1.5-meters down the staircase and puased briefly before returning the the starting position at the bottom of the staircase. 

<table>
  <tr>
    <!-- Graph -->
    <td width="70%" align="center">
      <h3>Sensor Bench Test Results</h3>
      <img src="Verification/Test%20Results/bench_test_sensors.png" width="600">
    </td>
    <!-- Data Table -->
    <td width="30%" align="center">
      <h3>Raw Sensor Data</h3>
      <table>
        <tr>
          <th>Time</th>
          <th>Alt</th>
          <th>Ax</th>
          <th>Ay</th>
          <th>Az</th>
        </tr>
        <tr>
          <td>0.338</td>
          <td>2.83</td>
          <td>0.24</td>
          <td>-0.27</td>
          <td>9.20</td>
        </tr>
        <tr>
          <td>0.353</td>
          <td>3.12</td>
          <td>0.24</td>
          <td>-0.25</td>
          <td>9.27</td>
        </tr>
        <tr>
          <td>0.366</td>
          <td>2.46</td>
          <td>0.16</td>
          <td>-0.35</td>
          <td>9.38</td>
        </tr>
        <tr>
          <td>0.380</td>
          <td>3.43</td>
          <td>0.09</td>
          <td>-0.30</td>
          <td>9.47</td>
        </tr>
      </table>
      <p>
        <a href="../Verification/Test Results/sensor_data_raw.csv">
          Sample data shown. Full dataset available here.
        </a>
      </p>
    </td>
  </tr>
</table>

This system verified the following requirements:

- ✅ REQ-01: The system succesfully accepetd the ON/OFF command from the user - component requirement satisfied by a switch on the power source.
- ✅ REQ-02: The system acquired pressure measurements which were converted to altitude values. The average sampling rate across the pressure measurements was 67 Hz (67 samples/sec) 
- ✅ REQ-03: The system acquired 3-axis acceleration measurements. The sampling rate across the accelerations measurements was 67 Hz (67 samples/sec).  
- ✅ REQ-04: The system succesfully timestamped all data measurements at an avaerge interval of 15 ms.
- ✅ REQ-05: The system succesfully stored all of the data to a CSV in the onboard micro SD card.




---

# Next Steps
## Mmoving forward to V1.1:
Building on flight data acquisition system V1.0, further testing will be completed for structural integrity under flight loads as well as simulations to ensure that the embedded avionivs system satisfies the center of gravity requirement, ensuring in-flight rocket stability. 

Upon completion and success of verificaiton and validation, an initial launch will be conducted to test the complete embedded system and analyze the flight of a 1:10 scale Nike Smoke model rocket on a C6:5 engine. 

In addition, further trade studies will be conducted to make incremental advances on the performance of this avionivs system.

---



