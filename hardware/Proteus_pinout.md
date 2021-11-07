### BMW M70B50 engine with rusEFI Proteus ###

#### Black 23pin ####
|Pin#|TS name|Type|Function|E31 connector|E31 sensor|E31 acquator|
|:---|:------|:---|:-------|:------------|:---------|:-----------|
|1|Digital 2 |din|Digital trigger/switch input|||
|2|Digital 3 |din|Digital trigger/switch input|||
|3|Digital 4 |din|Digital trigger/switch input|||
|4||vr|Variable Reluctance #2 positive|||
|5||vr|Variable Reluctance #1 positive||crank sensor|
|6||etb|ETB 1 negative|||ETB Bank1, falling signal from amp
|7||etb|ETB 1 positive|||ETB Bank1, rising signal
|8||etb|ETB 2 negative|||ETB Bank2, falling signal from amp
|9|Digital 5 |din|Digital trigger/switch input|||
|10|Digital 1 |din|Digital trigger/switch input|||
|11|Digital 6 |din|Digital trigger/switch input|||
|12||vr|Variable Reluctance #2 negative|||
|13||vr|Variable Reluctance #1 negative||crank sensor|
|14||gnd|Ground|X6400||
|15||etb|ETB 2 positive|||ETB Bank2, rising signal
|16||can|CAN bus low|||
|17||can|CAN bus high|||
|18|Battery Sense |12v|Ignition power / ECU power source. Connect this pin to the output of your ignition switch.|X20.7||
|19||gnd|Power GND|X6400||
|20||gnd|Power GND|X6400||
|21|||CAN2 software not ready|||
|22|||CAN2 software not ready|||
|23||12v|"Power supply from main relay. Connect this pin to the output of the car's main relay that also powers injectors, coils, etc. Supplies power to electronic throttle drivers and high side outputs."|||
