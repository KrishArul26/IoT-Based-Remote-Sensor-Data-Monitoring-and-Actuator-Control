<h2 align="center"> IoT-BASED-REMOTE-SENSOR-DATA-MONITORING-AND-ACTUATOR-CONTROL
  </h2>


<h3 align="left">System Implementation for the Water Tank Example
  
  </h3>
  


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
  ```
  HiveMQ broker - It was used to test published/subscribed messages.
  
  ```
  ```
  Influx-DB - It was used as Database For enabling water level and DHT11 sensor streamingtime-seriesdata.
  
  ```
  
  ```
  Grafana - It was used for visualizing temperature and humidity data
  ```
  
 
<h3 align="left"> The process flow of the system is as follows:
  
  </h3>
  
<p align="center">
  <img width="1500" src="https://user-images.githubusercontent.com/74568334/139573143-c6fdee30-5c51-4021-abb5-1040a6ec902c.jpg">
</p>

 <p style= 'text-align: justify;'> The above picture illustrates the monitoring system of the water level in a smart home network. Water  level sensor and DHT11 sensor are connected to Raspberry pi zero.Firstly, Raspberry-pi Zero is gathered streaming data from DHT11 – sensor, the water level – sensor and the ultrasonic sensor. Which values are converted to the action or messages and Those messages are published to the MQTT – Protocol to a particular topic. Next, RaspberryPi- 4 is giving a request to the MQTT protocol in order to get sensor values that are published by Raspberrypi Zero. Moreover, According to the message relay is handled by RaspberryPi- 4 in order to manage the power supply for the motor as well as Raspberry pi- 4 push data and message into the InfluxDB. After that,  Grafana is connected with InfluxDB to do data visualization.</p>

