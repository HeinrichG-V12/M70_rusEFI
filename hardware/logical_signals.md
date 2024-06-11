# Motronic M1.7 logical signal definitions

- TD: Drehzahlsignal, 1x pro Zündung:
    - 60Hz Enspricht dabei:
        - 1200RPM beim R6 und V12
        - 1800RPM beim R4
        - 900RPM beim V8
- TR: Drehzahlsignal, 3x pro KW-Umdrehung

## Umrechnung

BMW sagt, dass 60Hz 

- 1800 U/m beim R4
- 1200 U/m beim R6 und V12
- 900 U/m beim V8

entsprechen.

### Umrechnung beim R4

Je NW-Umdrehung entspricht zwei KW-Umdrehungen. Je NW-Umdrehung entspricht vier Zündimpulsen, also 2 Impulse pro KW-Umdrehung:

> Drehzahl = (Frequenz / 2) * 60

alternativ

> Drehzahl = Frequenz * 30

### Umrechnung beim V8

Je NW-Umdrehung entspricht zwei KW-Umdrehungen. Je NW-Umdrehung entspricht acht Zündimpulsen, also 4 Impulse pro KW-Umdrehung:

> Drehzahl = (Frequenz / 4) * 60

alternativ

> Drehzahl = Frequenz * 15

### Umrechnung beim R6 und V12

Je NW-Umdrehung entspricht zwei KW-Umdrehungen. Je NW-Umdrehung entspricht sechs Zündimpulsen, also 3 Impulse pro KW-Umdrehung:

> Drehzahl = (Frequenz / 3) * 60

alternativ

> Drehzahl = Frequenz * 20
