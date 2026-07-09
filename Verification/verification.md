# Verification Cross-Reference Matrix (VCRM)

The Verification Cross-Reference Matrix (VCRM) maps system requirements to their planned verification method and current verification status. Verification methods include Test, Demonstration, Inspection, and Analysis.

<table>
  <tr>
    <th>REQ ID</th>
    <th>Requirement Description</th>
    <th>Verification Method</th>
    <th>Evidence / Supporting Documents *** make these links!</th>
    <th>Pass / Fail Status</th>
  </tr>

  <tr>
    <td><b>REQ-01</b></td>
    <td>System accepts user ON/OFF input</td>
    <td>Demonstration</td>
    <td>user input results</td>
    <td><span style="color:green"><b>Pass</b></span></td>
  </tr>

  <tr>
    <td><b>REQ-02</b></td>
    <td>System samples barometric pressure at 45 Hz</td>
    <td>Test</td>
    <td>BMP 280 barometric pressure test data</td>
    <td><font color="green"><b>Pass</b></font></td>
  </tr>

  <tr>
    <td><b>REQ-03</b></td>
    <td>System samples 3-axis acceleration at 45 Hz</td>
    <td>Test</td>
    <td>MPU 6050 IMU Acceleration test data</td>
    <td><font color="green"><b>Pass</b></font></td>
  </tr>

  <tr>
    <td><b>REQ-04</b></td>
    <td>System timestamps data at 22.2 ms intervals</td>
    <td>Test</td>
    <td>timestamp test data </td>
    <td><font color="green"><b>Pass</b></font></td>
  </tr>

  <tr>
    <td><b>REQ-05</b></td>
    <td>System stores data to onboard micro SD card module</td>
    <td>Test</td>
    <td>micro SD storage test file/td>
    <td><font color="green"><b>Pass</b></font></td>
  </tr>

  <tr>
    <td><b>REQ-06</b></td>
    <td>System maintains function across forces up to 15g</td>
    <td>Test</td>
    <td> </td>
    <td><font color="orange"><b>Pending</b></font></td>
  </tr>

  <tr>
    <td><b>REQ-07</b></td>
    <td>Continuous data logging for 180 seconds</td>
    <td>Test</td>
    <td>SD card logging test data</td>
    <td><font color="green"><b>Pass</b></font></td>
  </tr>

  <tr>
    <td><b>REQ-08</b></td>
    <td>System maintains rocket CG aft of CP by 49 mm</td>
    <td>Analysis</td>
    <td> </td>
    <td><font color="orange"><b>Pending</b></font></td>
  </tr>

</table>

---

# Test Results

<img src="../Verification/Test Results/bench_test_sensors.png" width="400">
---
