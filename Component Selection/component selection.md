# Component Selection

The process for component selection follows the Subjective Value Method in which several criterion are selected to compare candidate components. The criterion are valued on a 1-5 scale based on their relative utility (1 = poor, 2 = fair, 3 = satisfactory, 4 = good, 5 = Superior). The candidate compoents are then weighted in how well they perform each of the criterion (the total weights for each candidate component must be 100%). The components are the scored on each of the creiterion using the following formula : 

Score = weight x value

After scoring each candidate component, each of the component alternatives are compared to each other. In this instance, the results were documented in graphs. 

# Microcontroller Selection

<table>
  <tr>
    <td align="center">
      <strong>Microcontroller Weight Table</strong><br>
      <img src="trade%20analysis%20data/MCU%20weight%20table.png" width="450">
    </td>
    <td align="center">
      <strong>Microcontroller Alternatives</strong><br>
      <img src="trade%20analysis%20data/mcu%20alts.png" width="450"><br><br>
      <strong>Component Selection Graph</strong><br>
      <img src="mcu%20selection.png" width="450">
    </td>
  </tr>
</table>

Number of BUS channels and BUS speed was weighted the most in the microcontroller criertion due to the fact that multiple sensors would be running simultanelously. In addition, with more channels, the avionics system is given room to scale up in the future with additional sensors. The Raspberry Pi Pico was ultimately selected due to its excellent performance and cost. 

---

# Barometer Selection

<table>
  <tr>
    <td align="center">
      <strong>Barometer Weight Table</strong><br>
      <img src="trade%20analysis%20data/pressure%20weight%20table.png" width="450">
    </td>
    <td align="center">
      <strong>Barometer Alternatives</strong><br>
      <img src="trade%20analysis%20data/pressure%20alts.png" width="450"><br><br>
      <strong>Component Selection Graph</strong><br>
      <img src="pressure%20selection.png" width="450">
    </td>
  </tr>
</table>


The output data rate (ODR) was identified as the primary evaluation criterion for the barometer because it directly affects the system's achievable sampling rate. The BMP280 was selected as the preferred component because it met the required sampling performance while providing the lowest cost among the candidate barometers, resulting in the highest overall value.


---

# Acceleromter Selection

<table>
  <tr>
    <td align="center">
      <strong>Acceleromter Weight Table</strong><br>
      <img src="trade%20analysis%20data/accel%20weight%20table.png" width="450">
    </td>
    <td align="center">
      <strong>Acceleromter Alternatives</strong><br>
      <img src="trade%20analysis%20data/accel%20alts.png" width="450"><br><br>
      <strong>Component Selection Graph</strong><br>
      <img src="accelerometer%20selection.png" width="450">
    </td>
  </tr>
</table>

The output data rate (ODR) was identified as the primary evaluation criterion for the accelerometer because it directly affects the system's achievable sampling rate. The MPU-6050 was selected as the preferred component because it met the required sampling performance while providing the lowest cost among the candidate accelerometers, resulting in the highest overall value.



