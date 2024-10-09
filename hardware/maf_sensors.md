# MAF (Mass Air Flow sensor) #

## M70 original MAF sensor ##

**Important:**
Since Proteus does not support two MAF sensors at the moment, I will make a workaround:

- both MAF sensors are installed and connected to Proteus
- IAT sensor of first MAF ist connected to Proteus
- an additional MAP sensor is installed to detect the load

### Proteus suitable MAF sensors ###

![alt text][maf_sensor]

#### Sensor 1 (I'm using a couple of this) ####

- Bosch 0 280 218 019
- HFM5 - 4.7 analog sensor
- with NTC
- Range: -30 - 640kg/h
- Size: 70 x 96mm
- Plug Housing: 1928403836
- Pins
  - 1987280103 0.5mm² - 1mm²; Gasket: 1987280106
  - 1987280105 1.5mm² - 2.5mm²; Gasket: 1987280107

Output voltage Ua = f(Qm)
|Qm, kg/h|Ua, V|
|--------|-----|
|8|1.2390|
|10|1.3644|
|15|1.5241|
|30|1.8748|
|60|2.3710|
|120|2.9998|
|250|3.7494|
|370|4.1695|
|480|4.4578|

Temperature sensor
|Temperature, °C|Resistance, Ohm|
|--------|-----|
|-40|39260|
|-30|22960|
|-20|13850|
|-10|8609|
|0|5499|
|10|3604|
|20|2420|
|30|1662|
|40|1166|
|50|835|
|60|609|
|70|452|
|80|340|
|90|261|
|100|202|
|110|159|
|120|127|
|130|102|

### Sensor 2 ###

- Bosch 0 280 218 081
- HFM5 - 4.7 analog sensor
- with NTC
- Range: 10 - 480kg/h
- Size: 70 x 96mm
- Plug Housing: 1928403836
- Pins
  - 1987280103 0.5mm² - 1mm²; Gasket: 1987280106
  - 1987280105 1.5mm² - 2.5mm²; Gasket: 1987280107

Output voltage Ua = f(Qm)
|Qm, kg/h|Ua, V|
|--------|-----|
|8|1.2968|
|10|1.3700|
|15|1.5201|
|30|1.8577|
|60|2.3517|
|120|2.9658|
|250|3.7090|
|370|4.1266|
|480|4.4093|

Temperature sensor
|Temperature, °C|Resistance, Ohm|
|--------|-----|
|-40|39260|
|-30|22960|
|-20|13850|
|-10|8609|
|0|5499|
|10|3604|
|20|2420|
|30|1662|
|40|1166|
|50|835|
|60|609|
|70|452|
|80|340|
|90|261|
|100|202|
|110|159|
|120|127|
|130|102|


[maf_sensor]: ./pictures/MAF.jpg "MAF"