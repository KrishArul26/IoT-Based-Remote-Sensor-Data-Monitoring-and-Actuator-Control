<h2 align="center"> IOT-BASED-REMOTE-SENSOR-DATA-MONITORING-AND-ACTUATOR-CONTROL</h2>

<h3 align="left">System Implementation for the Water Tank Example
  

<p align="center">
  <img width="600" src="https://user-images.githubusercontent.com/74568334/139572476-985d0a61-1e2c-423e-85cb-359b29437cdc.png">
</p> 

<h3 align="left">Introduction 
  
  </h3>
  
<h4 align="left">As the current housing systems are moving towards automation, the focus on the systems used within the house is given more focus than the customer requirement. The systems available in the current market are complex and expensive. The objective of the “IoT based remote sensor data monitoring and actuator control” project is to create a partial open-source monitoring system that can be customized based on the individual requirements of the customer which is cheaper than the available market alternatives and user-friendly.
  </h4>
  
 
<h3 align="left">Componentes Used for this Project
  </h3>
  
<p align="center">
  <img width="700" src="https://user-images.githubusercontent.com/74568334/139572612-0775d268-d47c-4a05-85b3-2cf1852a10f6.jpg">
</p>
  
<h3 align="left">Sensors Used for this Project
  </h3>
  
<p align="center">
  <img width="700" src="https://user-images.githubusercontent.com/74568334/139572621-58d85a6d-d550-470b-9b62-968ebccbcfb7.jpg">
</p>
  
<h3 align="center">Process Explaination and Usage of Components
  
  </h3>

<h3 align="left"> Since this monitoring system can be used for various applications, it is difficult to reproduce every possible scenario. Hence the prototype for the 
use case of home water tank was built. 
  </h3>
  

  ```
  DHT11 - temperature and humidity readings.
  ```
  ```
  water level sensor - To avoid overflow of the water tank and emergency stop when desired level is reached
  ```
  ```
  MQTT - Use as communication protocol with between  sensor, between sensor and relay
  
  ```
  ```
  Raspberry pi zero - For getting the sensor data
  Raspberry pi 4 - To control relay & power supply
  
  ```
  
 
<h3 align="left"> The process flow of the system is as follows  
  
<p align="center">
  <img width="1000" src="https://user-images.githubusercontent.com/74568334/139573143-c6fdee30-5c51-4021-abb5-1040a6ec902c.jpg">
</p>
  

3. For enabling water level and DHT11 sensor streamingtime-seriesdata,Influx DB was 
used.
4. HiveMQ broker was used to test client published/subscribed messages.
5. Grafana was used for visualizing temperature and humidity data.
Figure 1 illustrates the monitoring system of the water level in a smart home network. Water 
level sensor and DHT11 sensor are connected to Raspberry pi zero. Both sensor streaming 
data is transmitted to Influx DB. The water and current flow are represented in blue and 
yellow arrows respectively.

  
  
  


