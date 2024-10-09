# Motronic M1.7 logical signal definitions

- TD: rpm signal / speed signal / rotation speed signal, 1x per ignition:
    - 60Hz corresponds:
        - 1200RPM for R6 and V12
        - 1800RPM for R4
        - 900RPM for V8
- TR: rpm signal / speed signal / rotation speed signal, 3x per crankshaft revolution

## Calculation TD signal

### Calculation for R4

Each camshaft revolution corresponds to two crankshaft revolutions. Each camshaft revolution corresponds to four ignition pulses, i.e. 2 pulses per crankshaft revolution: 

> rpm = (frequency / 2) * 60

alternatively

> rpm = frequency * 30

### Calculation for V8

Each camshaft revolution corresponds to two crankshaft revolutions. Each camshaft revolution corresponds to eight ignition pulses, i.e. 4 pulses per crankshaft revolution: 

> rpm = (frequency / 4) * 60

alternatively

> rpm = frequency * 15

### Calculation for R6 and V12

Each camshaft revolution corresponds to two crankshaft revolutions. Each camshaft revolution corresponds to six ignition pulses, i.e. 3 pulses per crankshaft revolution:

> rpm = (frequency / 3) * 60

alternatively

> rpm = frequency * 20

> What kind of fungus amongus is this?