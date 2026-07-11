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

# Sensor Bench Test - Test Results

<img src="../Verification/Test Results/Sensor Bench Test Results.png" width="600">v

"The system successfully recorded atmospheric pressure-derived altitude throughout the simulated flight profile. The data demonstrates acquisition, timestamping, and onboard storage functionality."



<table>
  <tr>
    <!-- Graph -->
    <td width="70%" align="center">
      <h3>Accelerometer Bench Test Results</h3>
      <img src="../Verification/Test Results/Sensor Bench Test Results.png" width="600">
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
