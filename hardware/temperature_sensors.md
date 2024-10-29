# BMW M70 temerature sensors

![alt text][temp_sensors]

## Intake air temperature sensor

- Number 1 and 2 on the picture
- BMW Number: 13621725323 or 13621725324
- **not used for proteus, because of integrated IAT sensor in MAF sensor**
- Type: NTC, 2 pin, 2.5k

## Coolang temperature sensor for DME

- Number 3 on the picture
- BMW Number: 13621707366
- Type: double NTC, 3 pin, 2.5k

- Pinout X6236 (bold = used for Proteus)

|Pin|Connected to|Wire color|Comment|
|:---------------|:---------------|:---------------|:---------------|
|1|X6010.78|0.5mm² BR/RT/GE|Sensor 1|
|2|X6010.43|0.5mm² BR|Sensor ground, together with IAT temp sensor|
|3|X6020.78|0.5mm² BR/RT|Sensor 2|

## Coolant temperature sensor for EML

- Number 4 on the picture
- **used for proteus!**
- BMW Number: 12621288158
- Type: NTC, 2 pin

## Coolant temperature sensor for instrument cluster gauge

- Number 5 on the picture
- B207 Coolant temperature sender
- **directly connected to electronic body module (EKM)**
- BMW Number: 12621710535
- Type: NTC, 2 pin
- Pinout X6232

|Pin|Connected to|Wire color|
|:---------------|:---------------|:---------------|
|1|X20.4|0.5mm² BR/VT|
|2|X20.20|0.5mm² BR/YE|

## Value table for Bosch 2.5k sensors

|Temperature (°C)|Resistance (Ohm)|
|:---------------|:---------------|
|-40|45,313|
|-30|26,113|
|-20|15,462|
|-10|9,397|
|0|5,896|
|10|3,792|
|20|2,500|
|30|1,707|
|40|1,175|
|50|834|
|60|596|
|70|436|
|80|323|
|90|243|
|100|187|
|110|144|
|120|113|
|130|89|

[temp_sensors]: ./pictures/temp_sensors.jpg "Temperature sensors"
