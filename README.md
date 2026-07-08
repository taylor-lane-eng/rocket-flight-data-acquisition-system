# 🚀 Rocket Flight Data Acquisition System

## Overview

This project involves the development of a model rocket avionics system designed to collect, store, and analyze flight data.

An initial prototype was developed to demonstrate technical feasibility of embedded sensor integration and flight data acquisition. Following prototype development, a formal systems engineering process is being applied to define requirements, establish architecture, and develop verification methods.

---

# Project Objectives

The system is being developed to:

- Measure rocket altitude and 3-axis acceleration during flight
- Collect and store flight data
- Support post-flight flight performance analysis
- Demonstrate a requirements-based systems engineering workflow

---

# Current Project Status

**Current Phase: System Definition and Design Maturation**

## Completed

- ✅ Initial avionics prototype developed  
- ✅ System requirement development 
- ✅ Functional Decomposition and traceability
- ✅ System architecture development (physical architecture traceability to functions)

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
      <img src="images/prototype.png" width="400" height="600">
    </td>
    <td align="center">
      <strong>CAD avionics bay</strong><br>
      <img src="images/cad_proto3.png" width="400" height="600">
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
System Architecture
        ↓
Trade Studies
        ↓
Verification and Validation
```
This approach establishes traceability between system requirements, functions, components and the verification process.

---
# System Requirements

The requirements process started with operational requirements and got more refined moving to system requirements > performance requirements > component requirments 

## Performance requirements

<img src="images/perf_requirements.png" width="700" height="800">

---
# Functional Analysis 
<img src="images/functional block diagram.png" width="700">

# Function - Requirement traceability 


<table>
  <tr>
    <td align="center">
      <strong>Function-Requirement Table</strong><br>
      <img src="images/function allocation table.png" width="700">
    </td>
    <td align="center">
      <strong>Requirements</strong>
      <ul align="left">
        <li>REQ-001: Maintain CG aft of CP</li>
        <li>REQ-002: Maintain structural and system integrity</li>
        <li>REQ-003: Collect flight telemetry data</li>
      </td>
  </tr>
</table>



