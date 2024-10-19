# Proteus harness description

- B+ source: RD
- Grond: BR
- bank 1 main color: VT
  - and second color for functions
- bank 1 central power (VBat), after work relay: VT
- bank 2 main color: OR
  - and second color for functions
- bank 2 central power (VBat), after work relay: OR

## main relay (blue)

- terminal 30: 4.0mm² RD, connected to B+
- terminal 85: 0.5mm² BK-YE, connected to Proteus B35.10 (lowside 13)
- terminal 87: 0.5mm² RD-BL, connected to:
  - work relay terminal 85
  - fuel relay terminal 85
  - ignition relay terminal 85
- temrinal 87: 1.5mm² RD-BU, connected to Proteus B23.23 (12v input)

## work relay (green)

- terminal 30: 6.0mm² RD, connected to B+
- terminal 85: terminal 87 main relay
- terminal 86: 0.5mm² BR, Ground
- terminal 87: 4.0mm² VT, spice in harness for bank 1
  - 6x 0.5mm² VT injection valves
  - 1x 0.5mm² VT MAF1 power
  - 1x 0.5mm² VT CAM Sensor
- terminal 87: 4.0mm² OR, spice in harness for bank 2
  - 6x 0.5mm² OR injection valves
  - 1x 0.5mm² OR MAF2 power

## fuel relay (green)

- terminal 30: 2.5m² RD, connected to B+
- terminal 85: 0.5mm² RD-BL, connected to main relay terminal 87
- terminal 86: 0.5mm² BN-GN, connected to Proteus B35.11 (lowside 14)
- terminal 87: 1.5mm² GN-VI, connected to X20.13
- terminal 87: 1.5mm² GN-GR, connected to X21.12

## ignition relay (green)

- terminal 30: 4.0² GN, connected to B+
- terminal 85: terminal 87 main relay
- terminal 86: 0.5mm² BR, Ground
- terminal 87: 2.5mm² Bank 1
- terminal 87: 2.5mm² Bank 2

https://www.kabelschuhe-shop.de/cembre-l1-m-stossverbinder-4-6mm
https://www.kabelschuhe-shop.de/cembre-s6-m3-5-quetschkabelschuh-ring-4-6mm-m3-5
