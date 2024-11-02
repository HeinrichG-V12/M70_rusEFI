# BMW M70 engine with rusEFI Proteus

Proteus pinout can be find [here](https://rusefi.com/docs/pinouts/proteus/)

- Black 23: B23
- Black 35: B35
- White 35: W35

## Pinning

### Blach 23 pin connector

|Pin#|TS Name|Type|Function|Wire size|E31 Connector|E31 Sensor|E31 Acquator|
|:---|:------------------------|:---|:---------------|:--------|:------------|:---------|:-----------|
|1|Digital 2|din|Digital trigger/switch input|||||
|2|Digital 3|din|Digital trigger/switch input|||||
|3|Digital 4|din|Digital trigger/switch input|||||
|4|VR2|vr|Variable reluctance #2 positive|||||
|5|VR1|vr|Variable reluctance #1 positive|||Crank sensor Pin 1||
|6|ETB1|etb|ETB 1 negative|1.5 VT/BK|||ETB 1 Pin 5|
|7|ETB1|etb|ETB 1 positive|1.5 BK/VT|||ETB 1 Pin 3|
|8|ETB2|etb|ETB 2 negative|1.5 OR/BK|||ETB 2 Pin 5|
|9|Digital 5|din|Digital trigger/switch input|||||
|10|Digital 1|din|Digital trigger/switch input|||||
|11|Digital 6|din|Digital trigger/switch input|||||
|12|VR2|vr|Variable reluctance #2 negative|||||
|13|VR1|vr|Variable reluctance #1 negative|||Crank sensor Pin 2||
|14|gnd|gnd|Ground|1.5mm² BL||||
|15|ETB2|etb|ETB 2 positive|1.5 BR/OR|||ETB 2 Pin 3|
|16|CAN1|can|CAN 1 low|0.35mm² GN||||
|17|CAN1|can|CAN 1 high|0.35mm² GN/WH||||
|18|Battery|pwr|Power supply from ignition switch|2.5mm² GN||||
|19|pgnd|gnd|Power ground|1.5mm² BL||||
|20|pgnd|gnd|Power ground|1.5mm² BL||||
|21|CAN2|can|CAN 2 low|0.35mm² VI||||
|22|CAN2|can|CAN 2 high|0.35mm² VI/WH||||
|23|PWR|pwr|Power supply from main relay|1.5mm² RD/BU||||
