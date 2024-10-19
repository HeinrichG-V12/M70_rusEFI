# Proteus trigger settings #

- Trigger Pattern
  - Wheel type: 60/2 (60 teeth, 2 missing teeth)
  - What kind of engine: Four Stroke
  - Skipped wheel location: On crankshaft
  - use only rising edge: true
  - Trigger angle advance (deg btdc): 84° (means: if the first cylinder is on TDC, the distance between *sensor* and the *reference mark* is 84° or 14 teeth)

- Trigger input
  - Crank Sensor (Primary channel): VR1
  - Invert Primary: false

![alt text][trigger_!]

![alt text][trigger_2]

[trigger_!]: ./pictures/trigger_settings.jpg "Trigger settings"
[trigger_2]: ./pictures/motronic_trigger_angle.jpg "Motronic 1.1 - 1.3 trigger angle BTDC"
