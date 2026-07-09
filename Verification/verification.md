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

<img src="../Verification/Test Results/bench_test_sensors.png" width="800">
---

# raw data sample:

<table>
  <tr>
    <th>Time (s)</th>
    <th>Altitude (m)</th>
    <th>Accel_X (m/s²)</th>
    <th>Accel_Y (m/s²)</th>
    <th>Accel_Z (m/s²)</th>
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

  <tr>
    <td>0.393</td>
    <td>2.26</td>
    <td>0.38</td>
    <td>-0.21</td>
    <td>9.60</td>
  </tr>

  <tr>
    <td>0.407</td>
    <td>3.14</td>
    <td>0.67</td>
    <td>-0.04</td>
    <td>9.69</td>
  </tr>

  <tr>
    <td>0.420</td>
    <td>3.21</td>
    <td>0.81</td>
    <td>-0.13</td>
    <td>9.76</td>
  </tr>

  <tr>
    <td>0.433</td>
    <td>2.78</td>
    <td>0.89</td>
    <td>-0.03</td>
    <td>9.88</td>
  </tr>

  <tr>
    <td>0.447</td>
    <td>2.78</td>
    <td>1.29</td>
    <td>0.03</td>
    <td>9.84</td>
  </tr>

  <tr>
    <td>0.460</td>
    <td>3.22</td>
    <td>1.48</td>
    <td>0.09</td>
    <td>9.90</td>
  </tr>

  <tr>
    <td>0.474</td>
    <td>3.37</td>
    <td>1.72</td>
    <td>0.29</td>
    <td>10.09</td>
  </tr>

  <tr>
    <td>0.487</td>
    <td>3.09</td>
    <td>2.16</td>
    <td>0.30</td>
    <td>10.41</td>
  </tr>

  <tr>
    <td>0.500</td>
    <td>2.80</td>
    <td>2.52</td>
    <td>0.29</td>
    <td>10.52</td>
  </tr>

</table>



testing something: 

<table>
  <tr>
    <td align="center" width="50%">
      <b>Accelerometer Bench Test Results</b><br><br>
      <img src="../Verification/Test Results/bench_test_sensors.png" width="600">
    </td>
    <td align="center" width="50%">
      <b>Raw Sensor Data</b><br><br>
      <table>
        <tr>
          <th>Time (s)</th>
          <th>Altitude (m)</th>
          <th>Accel_X (m/s²)</th>
          <th>Accel_Y (m/s²)</th>
          <th>Accel_Z (m/s²)</th>
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
        <tr>
          <td>0.393</td>
          <td>2.26</td>
          <td>0.38</td>
          <td>-0.21</td>
          <td>9.60</td>
        </tr>
        <tr>
          <td>0.407</td>
          <td>3.14</td>
          <td>0.67</td>
          <td>-0.04</td>
          <td>9.69</td>
        </tr>
        <tr>
          <td>0.420</td>
          <td>3.21</td>
          <td>0.81</td>
          <td>-0.13</td>
          <td>9.76</td>
        </tr>
        <tr>
          <td>0.433</td>
          <td>2.78</td>
          <td>0.89</td>
          <td>-0.03</td>
          <td>9.88</td>
        </tr>
        <tr>
          <td>0.447</td>
          <td>2.78</td>
          <td>1.29</td>
          <td>0.03</td>
          <td>9.84</td>
        </tr>
        <tr>
          <td>0.460</td>
          <td>3.22</td>
          <td>1.48</td>
          <td>0.09</td>
          <td>9.90</td>
        </tr>
      </table>
    </td>
  </tr>
</table>
