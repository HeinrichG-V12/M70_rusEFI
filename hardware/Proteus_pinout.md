### BMW M70B50 engine with rusEFI Proteus ###

[Proteus pinout found here](https://rusefi.com/docs/pinouts/proteus/)<br/>
[Proteus github](https://github.com/mck1117/proteus/)<br/>
<br/>
[FAQ basic wiring and connection](https://github.com/rusefi/rusefi/wiki/FAQ-Basic-Wiring-and-Connections)
<br/>
[HOWTO Crimp AMPSEAL](https://github.com/rusefi/rusefi/wiki/HOWTO-Crimp-Ampseal)
<br/>
[AMPSEAL Connector Instructions](https://www.youtube.com/watch?v=uXTkm_XV2OY)
<br/>
[AMPSEAL Connector Crimp Tool IWISS SN-28B]()

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

- **TE Ampseal terminals:**
  - 16-20 AWG: 770854-1 (0.5mm² - 1.5mm²)

**Wire colors**
|color code|color|
|----------|-----------|
|BU|blue|
|BR|brown|
|BK|black|
|YE|yellow|
|RD|red|
|VT|violet|
|GN|green|
|GY|grey|
|OG|orange|
|PK|pink|
|WH|white|

#### P1
#### 23pin black (plug housing black 770680-1, white 770680-2, *grey 770680-4*, blue 770680-5) ####

|Pin#|TS Name                  |Type|Function|Wire size|E31 Connector|E31 Sensor|E31 Acquator|Wire color|
|:---|:------------------------|:---|:---------------|:--------|:------------|:---------|:-----------|:-----------|
|1|Digital 2|din|Digital trigger/switch input||||||
|2|Digital 3|din|Digital trigger/switch input||||||
|3|Digital 4|din|Digital trigger/switch input||||||
|4||vr|Variable Reluctance #2 positive||||||
|5||vr|Variable Reluctance #1 positive|||crank sensor|||
|6||etb|ETB 1 negative|1.5mm2 / VT-BK|||ETB Bank1, negative||
|7||etb|ETB 1 positive|1.5mm2 / BK-VT|||ETB Bank1, positive||
|8||etb|ETB 2 negative|1.5mm² / OR-BK|||ETB Bank2, negative||
|9|Digital 5|din|Digital trigger/switch input||||||
|10|Digital 1|din|Digital trigger/switch input||||||
|11|Digital 6|din|Digital trigger/switch input||||||
|12||vr|Variable Reluctance #2 negative||||||
|13||vr|Variable Reluctance #1 negative|||crank sensor|||
|14||gnd|Ground|1.5mm² / BK|X6400||||
|15||etb|ETB 2 positive|1.5mm² BK-OR|||ETB Bank2, positive||
|16||can|CAN bus low||||||
|17||can|CAN bus high||||||
|18|Battery Sense|12v|Ignition power / ECU power source. Connect this pin to the output of your ignition switch.|0.5mm² / GN|X20.7||||
|19||gnd|Power GND|1.5mm² / BK|X6400||||
|20||gnd|Power GND|1.5mm² / BK|X6400||||
|21|||CAN2 software not ready||||||
|22|||CAN2 software not ready||||||
|23||12v|"Power supply from main relay. Connect this pin to the output of the car's main relay that also powers injectors, coils, etc. Supplies power to electronic throttle drivers and high side outputs."|1.5mm² / RD-BU|Main relay. Pin 87||||

#### P2
#### 35pin black (plug housing black 776164-1, natural 776164-2, grey 776164-4, blue 776164-5, orange 776164-6) ####
|Pin#|TS Name             |Type|Function|Wire size / color|E31 Connector|E31 Sensor|E31 Acquator|
|:---|:-------------------|:---|:---------------|:------------------------|:------------|:---------|:-----------|
|1|Highside 2|hs|output|||||
|2|Highside 1|hs|output|||||
|3|Lowside 1|ls|Injector #1|0.5mm² / VT-BU|||Injector cylinder 1|
|4|Lowside 3|ls|Injector #3|0.5mm² / VT-GY|||Injector cylinder 3|
|5|Lowside 5|ls|Injector #5|0.5mm² / VT-RD|||Injector cylinder 5|
|6|Lowside 6|ls|Injector #6|0.5mm² / VT-WH|||Injector cylinder 6|
|7|Lowside 7|ls|Injector #7|0.5mm² / OG-BU|||Injector cylinder 7|
|8|Lowside 9|ls|Injector #9|0.5mm² / OG-GY|||Injector cylinder 9|
|9|Lowside 11|ls|Injector #11|0.5mm² / OG-RD|||Injector cylinder 11|
|10|Lowside 13|ls|Main relay|0.5mm² / BK-YE|Main relays, terminal 85|||
|11|Lowside 14|ls|Fuel Pump|0.5 mm² / BN-GN|Fuel pump relay, terminal 85|||
|12|Lowside 15|ls||||||
|13|Highside 3|hs|output|||||
|14|Highside 4|hs|output|||||
|15|Lowside 2|ls|Injector #2|0.5mm² / VT-YE|||Injector cylinder 2|
|16|Lowside 4|ls|Injector #4|0.5mm² / VT-GN|||Injector cylinder 4|
|17||gnd|Power GND|1.5mm² / BK|X6400|||
|18||gnd|Power GND|1.5mm² / BK|X6400|||
|19|Lowside 8|ls|Injector #8|0.5mm² / OG-YE|||Injector cylinder 8|
|20|Lowside 10|ls|Injector #10|0.5mm² / OG-GN|||Injector cylinder 10|
|21|Lowside 12|ls|Injector #12|0.5mm² / OG-WH|||Injector cylinder 12|
|22|Ign 3|hl|Ignition cylinder 3|0.5mm²|||COP cylinder 3|
|23|Lowside 16|ls||||||
|24||gnd|Power GND|1.5mm² / BK|X6400|||
|25|Ign 12|hl|Ignition cylinder 12|0.5mm²|||COP cylinder 12|
|26|Ign 11|hl|Ignition cylinder 11|0.5mm²|||COP cylinder 11|
|27|Ign 10|hl|Ignition cylinder 10|0.5mm²|||COP cylinder 10|
|28|Ign 9|hl|Ignition cylinder 9|0.5mm²|||COP cylinder 9|
|29|Ign 8|hl|Ignition cylinder 8|0.5mm²|||COP cylinder 8|
|30|Ign 7|hl|Ignition cylinder 7|0.5mm²|||COP cylinder 7|
|31|Ign 6|hl|Ignition cylinder 6|0.5mm²|||COP cylinder 6|
|32|Ign 5|hl|Ignition cylinder 5|0.5mm²|||COP cylinder 5|
|33|Ign 4|hl|Ignition cylinder 4|0.5mm²|||COP cylinder 4|
|34|Ign 2|hl|Ignition cylinder 2|0.5mm²|||COP cylinder 2|
|35|Ign 1|hl|Ignition cylinder 1|0.5mm²|||COP cylinder 1|

#### P3
#### 35pin white (plug housing black 776164-1, natural 776164-2, grey 776164-4, blue 776164-5, orange 776164-6) ####
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
|9||5v|Analog Voltage +5 supply #1|0.5mm² / OR|||
|10||5v|Analog Voltage +5 supply #2|0.5mm² / PK|||
|11||12v|12V protected output for sensors||||
|12||12v|12V protected output for sensors||||
|13|Analog Volt 1|av|ETB Bank 1 - Sensor 1|0.5mm² / OG-YE||ETB1 - Sensor 1|
|14|Analog Volt 3|av|ETB Bank 1 - Sensor 2|0.5mm² / OG-GN||ETB1 - Sensor 2|
|15|Analog Volt 5|av|Accelerator pedal (AP) - Sensor 1|0.5mm²||AP - Sensor 1|
|16|Analog Volt 7|av|Accelerator pedal (AP) - Sensor 2|0.5mm²||AP - Sensor 2|
|17|Analog Volt 9|av|Analog Voltage Input #9||||
|18|Analog Volt 11|av|Analog Voltage Input #11||||
|19|Analog Temp 1|at|Intake air temperature - Bank 1|0.5mm²||IAT1|
|20|Analog Temp 3|at|Intake air temperature - Bank 2|0.5mm²||IAT2|
|21||5v|Analog Voltage +5 supply #1||||
|22||5v|Analog Voltage +5 supply #2||||
|23||sgnd|Sensor GND||||
|24|Analog Volt 2|av|ETB Bank 2 - Sensor 1|0.5mm² / GN-PK||ETB2 - Sensor 1|
|25|Analog Volt 4|av|ETB Bank 2 - Sensor 2|0.5mm² / BK-PK||ETB2 - Sensor 2|
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

### Unused outputs
- Low side: Lowside 15, Lowside 16
- High side: Highside 1-4

### [Relays](./relays.md)
#### Main relays
##### Main relay 1

|Terminal|Connected to|Wire size / color|
|:-------|:-----------|:----------------|
|30|B+|4mm² / RD|
|85|lowside 13|0.5mm² / BK-YE|
|86|B+|0.5mm² / RD|
|87|Bank 1 injectors UBat|4mm²|
|87|Bank 1 MAF Sensor|1.5mm²|
|87|Fuel pump relay 1, terminal 86|0.5mm²|
|87a|P1.23|1.5mm² / RD-BU|
|87a|X69.7|1.5mm² / RD-BU|

##### Main relay 2

|Terminal|Connected to|Wire size / color|
|:-------|:-----------|:----------------|
|30|B+ |4mm² / RD|
|85|Main relay 1, terminal 85|0.5mm² / BK-YE|
|86|B+|0.5mm² / RD|
|87|Bank 2 injectors UBat|4mm²|
|87|Bank 2 MAF Sensor|1.5mm²|
|87|Fuel pump relay 2, terminal 86|0.5mm²|
|87a|P1.23|1.5mm² / RD-BU|
|87a|X69.7|1.5mm² / RD-BU|

##### Fuel pump relay 1

|Terminal|Connected to|Wire size / color|
|:-------|:-----------|:----------------|
|30|B+|4mm² / RD|
|85|lowside 14|0.5mm² / BK-YE|
|86|Main relay 1, terminal 87|0.5mm² / RD|
|87|X20.13|1.5mm²|
|87a|X21.12|1.5mm²|
