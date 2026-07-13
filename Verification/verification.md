
<h1>Test and Evaluation Master Plan (TEMP)</h1>

<h2>1. System Introduction</h2>

<h3>Mission Description</h3>
<p>
The Rocket Flight Data Acquisition System is an avionics system designed 
to collect and store flight data during model rocket operations. The 
system measures barometric pressure, acceleration, and timing data to support 
post-flight performance analysis and future flight validation.
</p>

<h3>Operational Environment</h3>
<p>
The avionics system is intended to operate within a model rocket environment 
characterized by:
</p>

<ul>
  <li>High acceleration during powered ascent</li>
  <li>Rapid altitude changes</li>
  <li>Short-duration flight operations</li>
  <li>Limited onboard power and storage capacity</li>
</ul>

<h3>System Description</h3>
<p>
The system consists of a Raspberry Pi Pico microcontroller, BMP280 barometric 
pressure sensor, MPU-6050 accelerometer, microSD storage module, battery power 
source, and 3D printed avionics enclosure. The system collects sensor data, 
timestamps measurements, and stores the data for post-test analysis.
</p>

<h3>Critical Technical Parameters</h3>

<table>
<tr>
<th>Parameter</th>
<th>Requirement</th>
</tr>

<tr>
<td>Pressure and acceleration Sampling Rate</td>
<td>&ge;45 Hz</td>
</tr>

<tr>
<td>Pressure and Acceleration Measurement</td>
<td>Continuous sensor acquisition</td>
</tr>

<tr>
<td>Timestamping</td>
<td>Measurement time recorded at intervals &le;22.2 ms </td>
</tr>

<tr>
<td>Data Storage Duration</td>
<td>&ge;180 seconds</td>
</tr>

<tr>
<td>Data Output</td>
<td>Stored flight data file for analysis</td>
</tr>

</table>


<h2>2. Integrated Test Program Summary</h2>

<p>
The integrated test program evaluates avionics system performance through 
incremental developmental testing followed by future operational testing.
</p>

<table>
<tr>
<th>Test Phase</th>
<th>Test ID</th>
<th>Description</th>
<th>Status</th>
</tr>

<tr>
<td>Developmental Test</td>
<td>DT-01</td>
<td>Data acquisition rate, timestamping, and data storage verification</td>
<td>Complete</td>
</tr>

<tr>
<td>Developmental Test</td>
<td>DT-02</td>
<td>Continuous operation and 180-second storage verification</td>
<td>Complete</td>
</tr>

<tr>
<td>Developmental Test</td>
<td>DT-03</td>
<td>Shock and Acceleration Load verification</td>
<td>Planned</td>
</tr>

<tr>
<td>Operational Test</td>
<td>OT-01</td>
<td>Integrated rocket flight test and mission performance evaluation</td>
<td>Planned</td>
</tr>

</table>


<h2>3. Developmental Test and Evaluation (DT&E)</h2>

<h3>Purpose</h3>

<p>
Developmental testing verifies individual avionics system functions and confirms 
that the prototype satisfies critical technical requirements and specifications prior to operational 
flight testing.
</p>

<h3>DT-01: Data Acquisition Performance Test</h3>

<h4>Method of Approach</h4>

<p>
The avionics system was powered on and configured to continuously collect pressure, 
acceleration, and timestamp data. Recorded test data was analyzed to determine 
sampling performance, timestamp consistency, and successful data storage.
</p>

<h4>Configuration Description</h4>

<ul>
<li>Raspberry Pi Pico microcontroller</li>
<li>BMP280 pressure sensor</li>
<li>MPU-6050 accelerometer</li>
<li>MicroSD storage module</li>
<li>AA Battery power source</li>
</ul>

<h4>Test Objectives</h4>

<ul>
<li>Verify minimum data acquisition rate requirement.</li>
<li>Verify timestamp generation.</li>
<li>Verify data storage functionality.</li>
</ul>

<h4>Results</h4>

<table>
<tr>
<th>Parameter</th>
<th>Result</th>
</tr>

<tr>
<td>Average Sample Interval</td>
<td>15 ms</td>
</tr>

<tr>
<td>Average Sampling Frequency</td>
<td>66.7 Hz</td>
</tr>

<tr>
<td>Timestamp Recording</td>
<td>Verified</td>
</tr>

<tr>
<td>Data Storage</td>
<td>Verified</td>
</tr>

</table>


<h3>DT-02: Continuous Operation and Storage Test</h3>

<h4>Method of Approach</h4>

<p>
The avionics system was operated continuously for a minimum duration of 180 seconds 
while recording telemetry data. The resulting data file was inspected for 
completeness and storage integrity.
</p>

<h4>Configuration Description</h4>

<p>
The same avionics configuration utilized during DT-01 was used for this test.
</p>

<h4>Test Objectives</h4>

<ul>
<li>Verify three-minute operational duration requirement.</li>
<li>Verify continuous data recording.</li>
<li>Verify stored data integrity.</li>
</ul>

<h4>Results</h4>

<table>
<tr>
<th>Parameter</th>
<th>Status</th>
</tr>

<tr>
<td>180-second operating requirement</td>
<td>Verified</td>
</tr>

<tr>
<td>Test data file generation</td>
<td>Verified</td>
</tr>

<tr>
<td>Data integrity</td>
<td>Verified</td>
</tr>

</table>

<h3>DT-03: Shock and Acceleration Load Test</h3>

<h4>Planned Approach</h4>

<p>
The avionics system will be subjected to controlled acceleration loading up to 
15g to evaluate the ability of the hardware and electrical connections to 
maintain functionality under expected launch loading conditions. Following 
exposure, system operation and telemetry storage capability will be evaluated.
</p>

<h4>Planned Configuration Description</h4>

<p>
The test configuration will consist of the integrated avionics assembly including 
the microcontroller, sensors, power system, and data storage components. The final 
test fixture and loading method will be determined prior to test execution.
</p>

<h4>Test Objectives</h4>

<ul>
<li>Verify avionics functionality following exposure to up to 15g acceleration loading.</li>
<li>Verify continued sensor operation after applied loading.</li>
<li>Verify telemetry storage capability remains functional.</li>
<li>Identify any mechanical or electrical failures resulting from acceleration loading.</li>
</ul>

<h4>Results</h4>

<table>
<tr>
<th>Parameter</th>
<th>Status</th>
</tr>

<tr>
<td>15g acceleration load exposure</td>
<td>Planned</td>
</tr>

<tr>
<td>Post-test system functionality</td>
<td>Planned</td>
</tr>

<tr>
<td>Telemetry storage integrity</td>
<td>Planned</td>
</tr>

</table>



<h2>4. Operational Test and Evaluation (OT&E)</h2>

<h3>Purpose</h3>

<p>
Operational testing will evaluate the complete avionics system under representative 
rocket flight conditions and determine system performance within the intended 
operational environment.
</p>


<h3>Configuration Description</h3>

<p>
The operational test configuration will consist of the integrated avionics system 
installed within the model rocket platform.
</p>

<ul>
<li>Flight vehicle integration</li>
<li>Onboard power system</li>
<li>Flight sensors</li>
<li>Flight Data storage system</li>
<li>Avionics Bay</li>
</ul>


<h3>Test Objectives</h3>

<ul>
<li>Verify successful system operation during launch.</li>
<li>Evaluate sensor performance during flight acceleration.</li>
<li>Generate altitude and acceleration flight profiles.</li>
<li>Recover and analyze stored flight data.</li>
<li>Evaluate system survivability after flight loads.</li>
</ul>



---


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
    <td>Test [DT-01]</td>
    <td>user input results</td>
    <td><span style="color:green"><b>Pass</b></span></td>
  </tr>

  <tr>
    <td><b>REQ-02</b></td>
    <td>System samples barometric pressure at 45 Hz</td>
    <td>Test [DT-01]</td>
    <td>BMP 280 barometric pressure test data</td>
    <td><font color="green"><b>Pass</b></font></td>
  </tr>

  <tr>
    <td><b>REQ-03</b></td>
    <td>System samples 3-axis acceleration at 45 Hz</td>
    <td>Test [DT-01]</td>
    <td>MPU 6050 IMU Acceleration test data</td>
    <td><font color="green"><b>Pass</b></font></td>
  </tr>

  <tr>
    <td><b>REQ-04</b></td>
    <td>System timestamps data at 22.2 ms intervals</td>
    <td>Test [DT-01]</td>
    <td>timestamp test data </td>
    <td><font color="green"><b>Pass</b></font></td>
  </tr>

  <tr>
    <td><b>REQ-05</b></td>
    <td>System stores data to onboard micro SD card module</td>
    <td>Test [DT-01]</td>
    <td>micro SD storage test file/td>
    <td><font color="green"><b>Pass</b></font></td>
  </tr>

  <tr>
    <td><b>REQ-06</b></td>
    <td>System maintains function across forces up to 15g</td>
    <td>Test [DT-03]</td>
    <td> </td>
    <td><font color="orange"><b>Pending</b></font></td>
  </tr>

  <tr>
    <td><b>REQ-07</b></td>
    <td>Continuous data logging for 180 seconds</td>
    <td>Test [DT-02]</td>
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

# Developmental Test 01 [DT-01] 

The purpose of Developmental Test 01 was to determine if the component selection and fully constructed prototype could meet the performance requirements (See the [Performance Requirements](../README.md#performance-requirements) section.) - mainly powering on via user input signal (REQ-01), acheive a data sampling rate of no less than 45 Hz (REQ-02, REQ-03) and successfully store the timestamped data with an interval of no more than 22.2 ms (REQ-04) in onboard micro SD card storage (REQ-05).

Developmental Test 01 (DT-01) was conducted to verify that the avionics prototype could successfully measure changes in altitude and acceleration while recording data for post-test performance analysis. The test began by powering on the avionics prototype using the onboard power system and orienting the system in its nominal flight configuration, with the y-axis parallel to the force of gravity. Following system initialization, the prototype was carried up a 3-meter staircase to simulate an ascent. At the top of the staircase, the system remained stationary for a brief period before descending halfway down the staircase, where it again paused briefly. The prototype then returned to its original starting position at the base of the staircase. After the test sequence was complete, the system was powered off and the microSD card was removed for data retrieval and post-test analysis. The recorded altitude and acceleration measurements were evaluated to determine whether the system accurately captured the motion profile and produced data suitable for reconstructing the test event.

<h3>DT-01 Test Procedure</h3>

<p>
The following procedure was used to verify that the avionics system could satisfy the
data acquisition, timestamping, and onboard data storage requirements.
</p>

<table>
<tr>
<th>Step</th>
<th>Procedure</th>
<th>Expected Result</th>
</tr>

<tr>
<td><strong>1</strong></td>
<td>
Orient the avionics system consisting of the Raspberry Pi Pico, BMP280
barometric pressure sensor, MPU-6050 accelerometer, microSD storage module,
and battery power source in flight configuration in which the accelerometer's y-axis is parallel with the gravitational force.
</td>
<td>
Hardware oriented and ready for operation.
</td>
</tr>

<tr>
<td><strong>2</strong></td>
<td>
Power on the avionics system and allow the firmware to initialize.
</td>
<td>
Successful system initialization and data logging begins.
</td>
</tr>

<tr>
<td><strong>3</strong></td>
<td>
Allow the system to continuously acquire and record pressure, acceleration,
altitude, and timestamp data for the duration of the test procedure.
</td>
<td>
Continuous sensor acquisition without interruption.
</td>
</tr>

<tr>
<td><strong>4</strong></td>
<td>
Power off the system after data collection is complete. Remove the microSD
card and transfer the recorded test data file to a computer for analysis.
</td>
<td>
Test data file successfully recovered and accessible.
</td>
</tr>

<tr>
<td><strong>5</strong></td>
<td>
Import the telemetry data into Python and calculate the sample interval,
average sampling frequency, and timestamp consistency.
</td>
<td>
Sampling performance metrics successfully calculated.
</td>
</tr>

<tr>
<td><strong>6</strong></td>
<td>
Generate engineering plots including altitude vs. time, pressure vs. time, and
acceleration vs. time.
</td>
<td>
Plots generated for engineering analysis and verification.
</td>
</tr>

<tr>
<td><strong>7</strong></td>
<td>
Compare measured system performance against the applicable system
requirements and document verification results. 
</td>
<td>
Requirements verified and verification status documented.
</td>
</tr>

</table>

<h4>Success Criteria</h4>

<ul>
<li>System accepted user power on input.</li>
<li>Pressure and acceleration data were continuously acquired.</li>
<li>Average sampling frequency met or exceeded 45 Hz.</li>
<li>Timestamps were successfully recorded for each measurement with an average interval rate no greater than 22.2 ms.</li>
<li>Telemetry data was successfully stored to the microSD card.</li>
<li>The recorded data was successfully imported and analyzed.</li>
</ul>


<table>
  <tr>
    <!-- Graph -->
    <td width="70%" align="center">
      <h3> DT-01 Test Results</h3>
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

<table width="100%">
  <tr>
    <th align="left" width="15%">Requirement</th>
    <th align="left" width="45%">Requirement Description</th>
    <th align="left" width="40%">Verification Result</th>
  </tr>

  <tr>
    <td><strong>REQ-01</strong></td>
    <td>The system shall accept a user-initiated power-on command through the designated power switch.</td>
    <td>
      <strong>PASS:</strong> The system successfully powered on and initialized following user power-on input.
    </td>
  </tr>

  <tr>
    <td><strong>REQ-02</strong></td>
    <td>The system shall sample atmospheric pressure at a minimum rate of 45 Hz during powered ascent, coast, and descent.</td>
    <td>
      <strong>PASS:</strong> The system achieved an atmospheric pressure sampling rate of 66.7 Hz during DT-01.
    </td>
  </tr>

  <tr>
    <td><strong>REQ-03</strong></td>
    <td>The system shall sample three-axis acceleration at a minimum rate of 45 Hz from launch detection until end of flight logging.</td>
    <td>
      <strong>PASS:</strong> The system achieved a three-axis acceleration sampling rate of 66.7 Hz during DT-01.
    </td>
  </tr>

  <tr>
    <td><strong>REQ-04</strong></td>
    <td>The system shall assign timestamps to all measurements with a resolution of ≤22.2 ms.</td>
    <td>
      <strong>PASS:</strong> The system timestamped all measurements with an average time interval of 15 ms.
    </td>
  </tr>

  <tr>
    <td><strong>REQ-05</strong></td>
    <td>The system shall record all acquired timestamped sensor measurements to onboard storage.</td>
    <td>
      <strong>PASS:</strong> The system successfully recorded all test data to the onboard microSD card storage.
    </td>
  </tr>
</table>

Accelerometer measurements are presented as raw sensor outputs. Variations were expected due to manual movement with the system during the test and sensor orientation changes. Additional filtering will be implemented in future iterations for flight-quality acceleration estimation. 

---

# Developmental Test 02 [DT-02] 

The purpose of Developmental Test 02 was to verify that the fully constructed avionics prototype could continuously operate and record test data for the required mission duration. This test specifically evaluated the system's ability to maintain continuous data acquisition and onboard storage for a minimum duration of 180 seconds [(REQ-07)](../README.md#performance-requirements). 

Developmental Test 02 was conducted to verify that the avionics prototype could successfully record continuous timestamped sensor measurements for the required test duration. The test began by powering on the avionics prototype using the onboard power system. Following system initialization, the avionics system was allowed to continuously collect and store sensor measurements for a duration exceeding 180 seconds. Upon completion of the test duration, the system was powered off and the microSD card was removed for data retrieval and analysis. The recorded dataset was evaluated to verify that the system maintained continuous operation and successfully stored the complete test duration without data loss or interruption.

<h3>DT-02 Test Procedure</h3>

<p>
The following procedure was used to verify the avionics system's continuous operation
and onboard data storage duration requirements.
</p>

<table>
<tr>
<th>Step</th>
<th>Procedure</th>
<th>Expected Result</th>
</tr>

<tr>
<td><strong>1</strong></td>
<td>
Power on the avionics system with the onbaord power source.
</td>
<td>
Hardware initialized and continuous data recording begins.
</td>
</tr>

<tr>
<td><strong>2</strong></td>
<td>
Allow the system to continuously acquire and store timestamped sensor measurements for a minimum duration of 180 seconds.
</td>
<td>
System maintains uninterrupted operation and records test data for the required duration.
</td>
</tr>

<tr>
<td><strong>3</strong></td>
<td>
Power off the system, remove the microSD card, and transfer the recorded dataset to a computer for analysis.
</td>
<td>
Complete test dataset successfully recovered.
</td>
</tr>

<tr>
<td><strong>4</strong></td>
<td>
Analyze the recorded dataset to determine total recording duration and verify data completeness.
</td>
<td>
Recorded duration meets or exceeds 180 seconds with no data loss.
</td>
</tr>

<tr>
<td><strong>5</strong></td>
<td>
Compare measured system performance against applicable system requirements and document verification results.
</td>
<td>
Requirement verification status documented.
</td>
</tr>

</table>

<h4>Success Criteria</h4>

<ul>
<li>System accepted user power on input.</li>
<li>Pressure and acceleration data were continuously acquired for a duration of 180 seconds.</li>
<li>Average sampling frequency met or exceeded 45 Hz.</li>
<li>Timestamped test data was successfully recorded and stored to onboard microSD storage. </li>
<li>Recorded data was successfully recovered and analyzed.</li>
<li>REQ-07 was successfully verified.</li>
</ul>

<table>
  <tr>
    <!-- Graph -->
    <td width="70%" align="center">
      <h3> DT-01 Test Results</h3>
      <img src="../Verification/Test Results/DT02.png" width="600">
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

<table width="100%">
  <tr>
    <th align="left" width="15%">Requirement</th>
    <th align="left" width="45%">Requirement Description</th>
    <th align="left" width="40%">Verification Result</th>
  </tr>

  <tr>
    <td><strong>REQ-01</strong></td>
    <td>The system shall accept a user-initiated power-on command through the designated power switch.</td>
    <td>
      <strong>PASS:</strong> The system successfully powered on and initialized following user power-on input.
    </td>
  </tr>

  <tr>
    <td><strong>REQ-02</strong></td>
    <td>The system shall sample atmospheric pressure at a minimum rate of 45 Hz during powered ascent, coast, and descent.</td>
    <td>
      <strong>PASS:</strong> The system achieved an atmospheric pressure sampling rate of 66.7 Hz during DT-01.
    </td>
  </tr>

  <tr>
    <td><strong>REQ-03</strong></td>
    <td>The system shall sample three-axis acceleration at a minimum rate of 45 Hz from launch detection until end of flight logging.</td>
    <td>
      <strong>PASS:</strong> The system achieved a three-axis acceleration sampling rate of 66.7 Hz during DT-01.
    </td>
  </tr>

  <tr>
    <td><strong>REQ-04</strong></td>
    <td>The system shall assign timestamps to all measurements with a resolution of ≤22.2 ms.</td>
    <td>
      <strong>PASS:</strong> The system timestamped all measurements with an average time interval of 15 ms.
    </td>
  </tr>

  <tr>
    <td><strong>REQ-05</strong></td>
    <td>The system shall record all acquired timestamped sensor measurements to onboard storage.</td>
    <td>
      <strong>PASS:</strong> The system successfully recorded all test data to the onboard microSD card storage.
    </td>
  </tr>
</table>

Accelerometer measurements are presented as raw sensor outputs. Variations were expected due to manual movement with the system during the test and sensor orientation changes. Additional filtering will be implemented in future iterations for flight-quality acceleration estimation. 

