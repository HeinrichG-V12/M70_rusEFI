# BMW M70B50 engine electronic throttle bodies and pedal position sensor PWG #

[General Bosch ETBs](https://www.bosch-motorsport.com/content/downloads/Raceparts/en-GB/51017995147518219.html)

## Electronic throttle body ##

- Voltage: approx. 4.6V to 1V, depends on throttle flap angle

### ETB cylinder 1..6 pinout ###

|Pin#|Function|Description|
|:---|:----------|:-------|
|1|Throttle flap angle >17° switch|connected to EML, Pin 38, high (+5v) if flap closed|
|2|not used||
|3|Throttle actuator|connected to EML, Pin 17, positive|
|4|not used||
|5|Throttle actuator|connected to EML, Pin 35, negative|
|6|Throttle flap angle|connected to EML, Pin 27|
|7|Sensor power (5V)|connected to EML, Pin 12|
|8|Sensor ground (SGND)|connected to EML, Pin 26|

### ETB cylinder 7..12 pinout ###

|Pin#|Function|Description|
|:---|:----------|:-------|
|1|Throttle flap angle >17° switch|connected to EML, Pin 40, high (+5v) if flap closed|
|2|not used||
|3|Throttle actuator|connected to EML, Pin 18, positive|
|4|not used||
|5|Throttle actuator|connected to EML, Pin 34, negative|
|6|Throttle flap angle|connected to EML, Pin 28|
|7|Sensor power (5V)|connected to EML, Pin 11|
|8|Sensor ground (SGND)|connected to EML, Pin 10|

## Pedal position sensor PWG ##

- Voltage: approx. 0.4V to 4V, depends on pedal angle

### PWG pinout ###

|Pin#|Function|Description|
|:---|:----------|:-------|
|1|Pedal position|connected to EML, Pin 7 via X21.6|
|2|||
|3|||
|4|Sensor ground (SGND)|connected to EML, Pin 2 via X21.9|
|5|||
|6|Pedal position angle >9° switch|connected to EML, Pin 46 via X21.10|
|7|Sensor poti power (5V)|connected to EML, Pin 9 via X21.6|
|8|Sensor switch power (5V)|connected to EML, Pin 1 via X21.7|

For Proteus suitable PWG (1712009):

![alt text](./pictures/pwg.jpg "PWG")

|Pin#|Function|Description|
|:---|:----------|:-------|
|1|Sensor 1 signal output||
|2|Sensor 2 power (+5V)||
|3|||
|4|Sensor 2 ground||
|5|Sensor 2 signal output||
|6|Sensor 1 power (+5V)||
|7|||
|8|Sensor 1 ground||
