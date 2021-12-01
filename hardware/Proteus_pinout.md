### BMW M70B50 engine with rusEFI Proteus ###

[Proteus pinout found here](https://rusefi.com/docs/pinouts/proteus/)<br/>
[Proteus github](https://github.com/mck1117/proteus/)<br/>
<br/>
[FAQ basic wiring and connection](https://github.com/rusefi/rusefi/wiki/FAQ-Basic-Wiring-and-Connections)

#### General specs: ####
- **Outputs**
  - 16x 4A low-side drivers
  - 12x 5v ignition (or general purpose) outputs
  - Dual H-bridges for electronic throttle (also supports stepper idle valve!)
  - 4x 12v 3A high-side outputs

- **Inputs**
  - 12x Analog voltage inputs
  - 4x Analog temperature (5v pullup) inputs
  - 2x VR crank/cam/vehicle speed inputs
  - 6x hall cam/crank or digital input

- **Power Supply**
  - Full operation from 6-24v supply
  - Limited operation from 4-6v
  - Dual 5v sensor supplies, 150mA and 0.1% precision each, fully protected. realized with [Infineon TLS150](https://www.infineon.com/cms/de/product/power/linear-voltage-regulator/linear-voltage-regulators-for-automotive-applications/tls115d0ej/)
  - Dual protected 12v external sensor supply

- **max. current carrying capacity of the FLRY wires (VDE 0298/4)**
  - 0.35mm²: 1.5A
  - 0.5mm²: 3A
  - 0.75mm²: 6A
  - 1.0mm²: 10A
  - 1.5mm²: 16A
  - 2.5mm²: 25A
  - 4.0mm²: 32A
  - 6.0mm²: 40A

#### Black 23pin ####
|Pin#|TS Name                  |Type|Function|Wire size|E31 Connector|E31 Sensor|E31 Acquator|
|:---|:------------------------|:---|:---------------|:--------|:------------|:---------|:-----------|
|1|Digital 2|din|Digital trigger/switch input|||||
|2|Digital 3|din|Digital trigger/switch input|||||
|3|Digital 4|din|Digital trigger/switch input|||||
|4||vr|Variable Reluctance #2 positive|||||
|5||vr|Variable Reluctance #1 positive|||crank sensor||
|6||etb|ETB 1 negative||||ETB Bank1, falling signal from amp|
|7||etb|ETB 1 positive||||ETB Bank1, rising signal|
|8||etb|ETB 2 negative||||ETB Bank2, falling signal from amp|
|9|Digital 5|din|Digital trigger/switch input|||||
|10|Digital 1|din|Digital trigger/switch input|||||
|11|Digital 6|din|Digital trigger/switch input|||||
|12||vr|Variable Reluctance #2 negative|||||
|13||vr|Variable Reluctance #1 negative|||crank sensor||
|14||gnd|Ground||X6400|||
|15||etb|ETB 2 positive||||ETB Bank2, rising signal|
|16||can|CAN bus low|||||
|17||can|CAN bus high|||||
|18|Battery Sense|12v|Ignition power / ECU power source. Connect this pin to the output of your ignition switch.|0.5mm²|X20.12|||
|19||gnd|Power GND||X6400|||
|20||gnd|Power GND||X6400|||
|21|||CAN2 software not ready|||||
|22|||CAN2 software not ready|||||
|23||12v|"Power supply from main relay. Connect this pin to the output of the car's main relay that also powers injectors, coils, etc. Supplies power to electronic throttle drivers and high side outputs."|2.5mm²|Main relay. Pin 87|||

#### Black 35pin ####
|Pin#|TS Name             |Type|Function|Wire size|E31 Connector|E31 Sensor|E31 Acquator|
|:---|:-------------------|:---|:---------------|:--------|:------------|:---------|:-----------|
|1|Highside 2|hs|output||||
|2|Highside 1|hs|output||||
|3|Lowside 1|ls|Injector #1|0.5mm²|||Injector cylinder 1
|4|Lowside 3|ls|Injector #3|0.5mm²|||Injector cylinder 3
|5|Lowside 5|ls|Injector #5|0.5mm²|||Injector cylinder 5
|6|Lowside 6|ls|Injector #6|0.5mm²|||Injector cylinder 6
|7|Lowside 7|ls|Injector #7|0.5mm²|||Injector cylinder 7
|8|Lowside 9|ls|Injector #9|0.5mm²|||Injector cylinder 9
|9|Lowside 11|ls|Injector #11|0.5mm²|||Injector cylinder 11
|10|Lowside 13|ls|main relay|0.5mm²|Main relay, Pin 85||
|11|Lowside 14|ls|Lowside output||||
|12|Lowside 15|ls|radiator fan relay||||
|13|Highside 3|hs|output||||
|14|Highside 4|hs|output||||
|15|Lowside 2|ls|Injector #2|0.5mm²|||Injector cylinder 2
|16|Lowside 4|ls|Injector #4|0.5mm²|||Injector cylinder 4
|17||gnd|Power GND||X6400||
|18||gnd|Power GND||X6400||
|19|Lowside 8|ls|Injector #8|0.5mm²|||Injector cylinder 8
|20|Lowside 10|ls|Injector #10|0.5mm²|||Injector cylinder 10
|21|Lowside 12|ls|Injector #12|0.5mm²|||Injector cylinder 12
|22|Ign 3|hl|Ignition cylinder 3|0.5mm²|||COP cylinder 3
|23|Lowside 16|ls|Fuel Pump||||Fuel pump relay
|24||gnd|Power GND||X6400||
|25|Ign 12|hl|Ignition cylinder 12|0.5mm²|||COP cylinder 12
|26|Ign 11|hl|Ignition cylinder 11|0.5mm²|||COP cylinder 11
|27|Ign 10|hl|Ignition cylinder 10|0.5mm²|||COP cylinder 10
|28|Ign 9|hl|Ignition cylinder 9|0.5mm²|||COP cylinder 9
|29|Ign 8|hl|Ignition cylinder 8|0.5mm²|||COP cylinder 8
|30|Ign 7|hl|Ignition cylinder 7|0.5mm²|||COP cylinder 7
|31|Ign 6|hl|Ignition cylinder 6|0.5mm²|||COP cylinder 6
|32|Ign 5|hl|Ignition cylinder 5|0.5mm²|||COP cylinder 5
|33|Ign 4|hl|Ignition cylinder 4|0.5mm²|||COP cylinder 4
|34|Ign 2|hl|Ignition cylinder 2|0.5mm²|||COP cylinder 2
|35|Ign 1|hl|Ignition cylinder 1|0.5mm²|||COP cylinder 1

#### White 35pin ####
|Pin#|TS Name             |Type|Function                    |Wire size|E31 Connector|E31 Sensor|E31 Acquator|
|:---|:-------------------|:---|:---------------------------|:--------|:------------|:---------|:-----------|
|1||sgnd|Sensor GND||||
|2||sgnd|Sensor GND||||
|3||sgnd|Sensor GND||||
|4||sgnd|Sensor GND||||
|5||sgnd|Sensor GND||||
|6||sgnd|Sensor GND||||
|7||sgnd|Sensor GND||||
|8||sgnd|Sensor GND||||
|9||5v|Analog Voltage +5 supply #1||||
|10||5v|Analog Voltage +5 supply #2||||
|11||12v|12V protected output for sensors||||
|12||12v|12V protected output for sensors||||
|13|Analog Volt 1|av|ETB Bank 1 - Sensor 1|0.5mm²||ETB1 - Sensor 1|
|14|Analog Volt 3|av|ETB Bank 1 - Sensor 2|0.5mm²||ETB1 - Sensor 2|
|15|Analog Volt 5|av|Accelerator pedal (AP) - Sensor 1|0.5mm²||AP - Sensor 1|
|16|Analog Volt 7|av|Accelerator pedal (AP) - Sensor 2|0.5mm²||AP - Sensor 2|
|17|Analog Volt 9|av|Analog Voltage Input #9||||
|18|Analog Volt 11|av|Analog Voltage Input #11||||
|19|Analog Temp 1|at|Intake air temperature - Bank 1|0.5mm²||IAT1|
|20|Analog Temp 3|at|Intake air temperature - Bank 2|0.5mm²||IAT2|
|21||5v|Analog Voltage +5 supply #1||||
|22||5v|Analog Voltage +5 supply #2||||
|23||sgnd|Sensor GND||||
|24|Analog Volt 2|av|ETB Bank 2 - Sensor 1|0.5mm²||ETB2 - Sensor 1|
|25|Analog Volt 4|av|ETB Bank 2 - Sensor 2|0.5mm²||ETB2 - Sensor 2|
|26|Analog Volt 6|av|Analog Voltage Input #6||||
|27|Analog Volt 8|av|MAF sensor bank 1|0.5mm²||MAF1|
|28|Analog Volt 10|av|MAF sensor bank 2|0.5mm²||MAF2|
|29||sgnd|Sensor GND||||
|30|Analog Temp 2|at|Coolant temperature|0.5mm²||CLT|
|31|Analog Temp 4|at|Analog Thermistor Input #4||||
|32||5v|Analog Voltage +5 supply #1||||
|33||5v|Analog Voltage +5 supply #2||||
|34|||Knock input 1||||
|35|||Knock input 2||||

#### Analog Voltage +5 supply #1 and #2 ####
- realized with [Infineon TLS150](https://www.infineon.com/cms/de/product/power/linear-voltage-regulator/linear-voltage-regulators-for-automotive-applications/tls115d0ej/), 5v, 150mA, 0.1% precision