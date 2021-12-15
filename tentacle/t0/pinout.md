# <i class="fas fa-plug"></i> Pinout

![Whitebox T0 Pinout](/_media/whitebox-t0-pinout.svg)

## Microcontroller side

| Pin # | Signal | Description                               | min   | max    | Remarks                   |
|-------|-------:|:------------------------------------------|:------|:-------|---------------------------|
| 1     | VIN    | Supply voltage for the power isolator     | VSIG  | 5.5 V  | Can be separate from VSIG |
| 2     | VSIG   | Supply voltage for the signal isolator    | 3.3 V | 5.5 V  | Can be separate from VIN  |
| 3     | GND    | Ground                                    | -     | -      |                           |
| 4     | EN     | Enable/disable isolator. Active high GPIO | 2.0 V | 5.5 V  | do not leave floating     |
| 5     | SDA    | I2C Data line                             | VSIG  | 5.5 V  | no on-board pull-up       |
| 6     | SCL    | I2C Clock                                 | VSIG  | 5.5 V  | no on-board pull-up       |

## Isolated side

| Pin # | Signal | Description               | min   | max    | Remarks                   |
|-------|-------:|:--------------------------|:------|:-------|---------------------------|
| 7     | VISO    | Isolated voltage output  | 3.8  | 4.0 V   | Can be used for power indication LED, max draw 5mA. Do not connect to microcontroller gpio. |
| 8     | GND_ISO | Isolated GND             | -    | -       | Can be used for power indication LED. Do not connect to any other GND.  |
| 9     | PRB_GND | Probe Ground             | -    | -       |                           |
| 10    | PRB     | Probe Coax Signal        | -    | -       |                           |
| 11    | PRB_GND | Probe Ground             | -    | -       |                           |
| 12    | NC      | not connected            | -    | -       | leave floating            |

### EZO

| Pin # | Signal  | Description              | min  | max    |
|-------|--------:|:-------------------------|:-----|:-------|
| EZO 1 | GND_ISO | Isolated voltage output  | -    | -      |
| EZO 2 | SDA_ISO | Isolated I2C Data line   | 3.8V | 4.0 V  |
| EZO 3 | SCL_ISO | Isolated I2C Clock       | 3.8V | 4.0 V  |
| EZO 4 | VISO    | Isolated voltage output  | 3.8  | 4.0 V  |
| EZO 5 | PRB     | Probe Signal             | -    | -      |
| EZO 6 | PRB_GND | Probe Ground             | -    | -      |
