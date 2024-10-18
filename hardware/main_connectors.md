# BMW M70 engine harness connectors

![alt text][def]

## X20 pinout, male on engine harness side

|Pin #|Name|Comes from|Goes to|Comment|
|-----|----|----------|-------|-------|
|1|D+|Alternator D+|ABS/ASC X7.27||
|2|Oil level sensor|B205 oil level sensor, X6230.3|A25 EKM, X41.26|Oil sufficient level indicator (static)|
|3|Injection signal 1|A6010 DME1, X6010.17|A25 EKM, X41.4|Injection signal (ti signal 1)|
|4|Coolant temperature sender|EKM X41.16|B207 temp sensor, X6232.1||
|5|VBat|E-Box Fan X8506.3|X41.6|VBat for oil pressure switch. Oil pressure switch pull this to GND (closed), if pressure 0.2 to 0.5 Bar|
|6|||||
|7|Ignition switch status|S2 ignition switch|Ignition coils 1&2, DMEs pin 56|Ignition switch status, position 2 & 3|
|8|DWA|A25 EKM, X41.18|DME1 & 2, pin 81|DWA3, startup blocking if VBat|
|9|TD signal|A6010 DME1, X6010.74|A25 EKM, X41.7|engine speed signal, 1/min|
|10|Oil level sensor|B205 oil level sensor, X6230.1|A25 EKM, X41.15|Oil low level indicator (dynamic)|
|11|SI|D100.7|X41.8 EKM|Service reset|
|12|Check engine|DME 1 & 2, pin 8|Instrument cluster, X16.1|Check engine lamp|
|13||Fuel pump relay 1, pin 87|P90, Fuse 23, Fuel pump 1|Power supply for fuel pump 1|
|14|Vehicle speed signal|A25 EKM, X39.14|DME1 & 2 (Pin 73), EML (Pin 8), D100.13|Vehicle speed signal, Tacho-A|
|15|Starter lock|X69.10|K1 starter relais, X55, close relais if high|P/N recognition|
|16|RxD signal|||Diagnostic link|
|17|TxD signal|||Diagnostic link|
|18|Starter status|K1 starter relay 87 (pin 6)|Diagnostic connector D100.11||
|19|||||
|20|Coolant temperature sender|B207 temp sensor, X6232.2|EKM, X41.14, sensor ground||

## X21 pinout, female on engine harness side

|Pin #|Name|Comes from|Goes to|Comment|
|-----|----|----------|-------|-------|
|1|PPS|Pedal position sensor X73.1|EML X6004.7|sensor value|
|2|PPS|EML X6004.1|Pedal position sensor X73.7, sensor value|5v voltage|
|3|PPS|EML X6004.9|Pedal position sensor X73.8, angle > 9°|5v voltage|
|4|PPS|Pedal position sensor X73.4|EML X6004.2|sensor ground|
|5|PPS|Pedal position sensor X73.8|EML X6004.46|voltage divider for angle > 9° switch|
|6|PPS|DME2 X6020.62|Pedal position sensor X73.2|5v, pedal status, depressed/released switch|
|7|A/C status signal||EML X6004.44|AUX fan 6454.0|
|8|A/C compressor on|Lock sensor ECU X77.5|EML X6004.41|Automatic climate control 6450.0|
|9|||||
|10|Brake pedal position|Brake switch X78.2|EML X6004.53||
|11|Clutch pedal position|EML X6004.54|Clutch swith X121.2|in auto cars X121.1 and .2 shorted and .2 is GND|
|12||Fuel pump relay 2, pin 87|P90, Fuse 24, Fuel pump 2|Power supply for fuel pump 2|
|13|Compressor cut-off signal|Compressor cut-off relay X10042.10|DME1 X6010.48|DME1 low side switch|
|14|||A2 instrument cluster, X16.3|Auxilary alternator|
|15|PPS|DME1 X6010.62|Pedal position sensor X73.5|5v, pedal status, depressed/released switch|
|16|Cruise control|EML X6004.43|cc switch X72.6|5v, cruise control switch|
|17|EML lamp 1|EML X6004.15|A2 instrument cluster, X16.7||
|18|EML lamp 2|EML X6004.15|A2 instrument cluster, X16.20||
|19|Cruise control|EML X6004.31|cc switch X72.5|GND cruise control switch|
|20|Injection signal 2|DME2, X6020.17|EKM X41.17|Injection signal 2 (ti signal 2)|

## X69 pinout, male on engine harness side

|Pin #|Name|Comes from|Goes to|Comment|
|:----|:---|:---------|:------|:-------|
|1||ABS/ASC X7.45|DME X6010.83, X6020.83|Ignition cut-off|
|2|Program|EGS X8500.4|EML X6004.52|S-Program identifier|
|3|DKE|ABS/ASC X7.48 **or** ABS/ASC+T X7.8|EML X6004.22|Increase throttle|
|4|DKR|ABS/ASC X7.46 **or** ABS/ASC+T X7.6|EML X6004.4|Decrease throttle|
|5|DKV|EML X6004.23|EGS X8500.32, ABS/ASC X7.43 **or** ABS/ASC+T X7.14|Throttle position|
|6|ME|EGS X8500.24|DME X6010.64, X6020.64|Engine (ignition angle) intervention|
|7|Power|Main Relais 1, X6310.5|X18055|Power from main relais 1, terminal 87a for EGS X8500.35|
|8|WK|EGS X6500.25|DME X6010.63, X6020.63|torque convertor clutch valve|
|9|Injection signal 1|X20.3|EGS X8500.11|Injection signal comes from DME1 and goes to EKM and EGS|
|10|Starter lock|Automatic stransmission swtich, X8509.7|X20.15|P/N recognition|
|11|TR|Fuel pump relais 1 X6311.4|EGS X8500.21|TR Signal, GND with superimposed speed signal|
|12|Kick down|EML X6004.20|EGS X8500.2||
|13||ABS/ASC X7.47|DME X6010.82, X6020.82|Timing control (ASC), Injection control (MSR)|
|14|||||
|15|||||
|16|||||
|17|||||
|18|||||
|19|||||
|20|TD Signal|X20.9|X7.55 ABS / ASC+T ECU||

[def]: ./pictures/engine_harness.jpg "Main connectors"
