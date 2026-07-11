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

# Systems Engineering Approach

Following initial prototype development, the system is being matured using the following structured systems engineering process:

```
[Performance Requirements](#perfromance Requirements)
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
# Performance Requirements

An estimation of the rocket trajectory - apogee, acceleration, velocity and total operation time (pre-launch to recovery) were made to develop these performance requirements for the flight of a 1:10 scale Nike Smoke rocket with a C6:5 engine. From the engine specifications sheet, the C6:5 will have a max thrust of 14.1 N, and it was determined that the rocket avionics system must withstand up to 15g Forces.

From these calculations, the apogee was estimated to be 412 meters. With a minimum sampling rate of 45 Hz, the avionics system would acquire 206 pressure and acceleration samples upon reaching its apogee which satisfies an intial baseline performance for a minimum sampling rate. 

In addition, the total operation time from pre-launch to recovery was estimated as 104 seconds. This total oepration time drove the power capacity requirement. The power performance requirement was set to 180 seconds to provide a safety factor in case of unexpected recovery conflicts.

The full calucations can be seen here: [Full Engineering Requirement Calculations](Calculations/req_calculations.pdf)



<table style="border-collapse: collapse; width: 100%; font-family: Arial, sans-serif;">
    <tr style="background-color:#c9c9c9;">
        <th colspan="2" align="left" style="padding:14px; font-size:28px; border:1px solid #999;">
            Performance Requirements
        </th>
    </tr>
    <tr>
        <td width="24%" valign="top" style="padding:14px; font-size:24px; font-weight:bold; border:1px solid #999;">
            REQ-01
        </td>
        <td style="padding:14px; font-size:22px; border:1px solid #999;">
            The system shall accept a user-initiated power-on command through the designated power switch.
        </td>
    </tr>
    <tr>
        <td valign="top" style="padding:14px; font-size:24px; font-weight:bold; border:1px solid #999;">
            REQ-02
        </td>
        <td style="padding:14px; font-size:22px; border:1px solid #999;">
            The system shall sample atmospheric pressure at a minimum rate of 45 Hz during powered ascent, coast, and descent.
        </td>
    </tr>
    <tr>
        <td valign="top" style="padding:14px; font-size:24px; font-weight:bold; border:1px solid #999;">
            REQ-03
        </td>
        <td style="padding:14px; font-size:22px; border:1px solid #999;">
            The system shall sample three-axis acceleration at a minimum rate of 45 Hz from launch detection until end of flight logging.
        </td>
    </tr>
    <tr>
        <td valign="top" style="padding:14px; font-size:24px; font-weight:bold; border:1px solid #999;">
            REQ-04
        </td>
        <td style="padding:14px; font-size:22px; border:1px solid #999;">
            The system shall assign timestamps to all measurements with a resolution of ≤22.2 ms.
        </td>
    </tr>
    <tr>
        <td valign="top" style="padding:14px; font-size:24px; font-weight:bold; border:1px solid #999;">
            REQ-05
        </td>
        <td style="padding:14px; font-size:22px; border:1px solid #999;">
            The system shall record all acquired timestamped sensor measurements to onboard storage.
        </td>
    </tr>
    <tr>
        <td valign="top" style="padding:14px; font-size:24px; font-weight:bold; border:1px solid #999;">
            REQ-06
        </td>
        <td style="padding:14px; font-size:22px; border:1px solid #999;">
            The system shall remain fully functional after exposure to shock loads up to 15g peak acceleration and vibration representative of model rocket ignition and ascent.
        </td>
    </tr>
    <tr>
        <td valign="top" style="padding:14px; font-size:24px; font-weight:bold; border:1px solid #999;">
            REQ-07
        </td>
        <td style="padding:14px; font-size:22px; border:1px solid #999;">
            The system shall support continuous operation for at least 3 minutes of active logging time.
        </td>
    </tr>
    <tr>
        <td valign="top" style="padding:14px; font-size:24px; font-weight:bold; border:1px solid #999;">
            REQ-08
        </td>
        <td style="padding:14px; font-size:22px; border:1px solid #999;">
            The system shall ensure the rocket center of gravity remains at least 1.0 body diameter forward of the center of pressure for all flight configurations.
        </td>
    </tr>
</table>

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

# Component Selection and Trade Studies

The process for selecting components was the following:

- Define the criteria to compare the alternatives (based on meeting the performance requirements)
- Assign a weight to each of the criteria (total weight across all criteria must be one, higher score means greater importance). 
- Rate (1-5) each candidate component on how well they perform the criteria (1 is worst, 5 is best).
- Score each candidate component (weigh X Rate = Score).
- Plot the scores of each candidate component across each of the grading criteria

<table>
  <tr>
    <td width="60%" align="center">
      <img src="Component Selection/mcu selection.png" width="600">
    </td>
    <td width="40%" valign="top">

### Microcontroller Selection

Three microcontrollers were evaluated against the project requirements for flash memory, weight, cost, BUS speed, and number of BUS channels. The **Raspberry Pi Pico** was selected as the system's microcontroller because it provides sufficient processing performance to sample and timestamp multiple sensors above 65 Hz (REQ-04
) while being light weight and low cost. See the link below for specifications of the microcontrollers that were analyzed and the weight scale and score for each of the criteria.

</td>
  </tr>

  <tr>
    <td width="60%" align="center">
      <img src="Component Selection/accelerometer selection.png" width="600">
    </td>
    <td width="40%" valign="top">

### Accelerometer Selection

Three inertial measurement units were compared using acceleration range, weight, Output Data Rate (ODR), and cost. The **MPU-6050** was selected because it is the cheapest alternative that still meets the performance requirements - specifically on achieving a minimum sampling rate of 65 Hz (REQ-03). The MPU 6050 meets the performance requirement of measuring acceleration up to 15g (REQ-06) while being a lightweight sensor.

</td>
  </tr>

  <tr>
    <td width="60%" align="center">
      <img src="Component Selection/pressure selection.png" width="600">
    </td>
    <td width="40%" valign="top">

### Pressure Sensor Selection

Pressure sensors were evaluated based on pressure accuracy, weight, output data rate, and cost. The **BMP280** was selected due to its ability to successfully satisfy accurate pressure measurements at a sampling rate of 65 hz (REQ-02) at the lowest cost. These characteristics make it well suited for estimating rocket altitude while remaining within the project's size, weight, and budget constraints.

</td>
  </tr>
</table>

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

----

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

For a full Verification Cross-Reference Matrix (VCRM) along with the documented test results and further details, see the following link:
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



