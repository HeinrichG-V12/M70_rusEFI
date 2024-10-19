# BMW M70 engine injectors #

![alt text][inj_connector]

Pinout

|Pin #|Signal|
|-----|------|
|1|-, lowside switch|
|2|+, common UBat|

Plug:

- Housing: BMW 12521732460
- Pins: MDK4 2.8
  - BMW 0.5-1.0mm²: 1252 1737772
  - BMW 1-2.5mm²: 1252 1737773

M70 original Bosch injector (I'm using this)

- Bosch Number: 0280150715 (0 280 150 715)
- BMW Number: 1364 1706162
- Type: EV1
- Resistance (Ohm): 15.9
- Pressure (kPa/Bar): 300/3
- Q-Stat at 300kPa (g/min): 116.5
- Q-Stat at 300kPa (ml/min): 166
- Spray type: A (one outlet hole)
- total length: 74mm

dead times (comes from bin file):

|Voltage, v|8.5|12.7|13.8|14.9|16.0|
|-----|------|------|------|------|------|
|Dead time, ms|2.55|1.24|0.96|0.67|0.47|

Alternative Bosch injector (new part)

- Number: 0280156346 (0 280 156 346)
- Type: EV6
- Resistance (Ohm): 15.95
- Pressure (kPa/Bar): 300/3
- Q-Stat at 300kPa (g/min): 117
- Q-Stat at 300kPa (ml/min): 167
- Spray type: C (four outlet holes)
- total length: 74mm

![alt text][bosch_injectors]

[inj_connector]: ./pictures/injector_connectors.jpg "Injector connectors"
[bosch_injectors]: ./pictures/ev1_ev6_injectors.jpg "Bosch EV1 and EV6 injectors"
