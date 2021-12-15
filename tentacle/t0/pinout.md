# <i class="fas fa-microchip"></i> Pinout

## Microcontroller side

| Pin # | Signal | Description                               | min   | max    | Remarks                   |
|---------------:|:------------------------------------------|:------|:-------|---------------------------|
| 1     | VIN    | Supply voltage for the power isolator     | VSIG  | 5.5 V  | Can be separate from VSIG |
| 2     | VSIG   | Supply voltage for the signal isolator    | 3.3 V | 5.5 V  | Can be separate from VIN  |
| 3     | GND    | Ground                                    | -     | -      |                           |
| 4     | EN     | Enable/disable isolator. Active high GPIO | 2.0 V | 5.5 V  | do not leave floating     |
| 5     | SDA    | I2C Data line                             | VSIG  | 5.5 V  | no on-board pull-up       |
| 6     | SCL    | I2C Clock                                 | VSIG  | 5.5 V  | no on-board pull-up       |

## Isolated side

| Pin # | Signal | Description               | min   | max    | Remarks                   |
|---------------:|:--------------------------|:------|:-------|---------------------------|
| 7     | VISO    | Isolated voltage output  | 3.8  | 4.0 V   | Can be used for power indication LED, max draw 5mA. Do not connect to microcontroller gpio. |
| 8     | GND_ISO | Isolated GND             | -    | -       | Can be used for power indication LED. Do not connect to any other GND.  |
| 9     | PRB_GND | Probe Ground             | -    | -       |                           |
| 10    | PRB     | Probe Coax Signal        | -    | -       | do not leave floating     |
| 11    | PRB_GND | Probe Ground             | -    | -       | no on-board pull-up       |
| 12    | NC      | not connected            | -    | -       | leave floating            |

### EZO

| Pin # | Signal  | Description              | min  | max    |
|----------------:|:-------------------------|:-----|:-----.-|
| EZO 1 | GND_ISO | Isolated voltage output  | -    | -      |
| EZO 2 | SDA_ISO | Isolated I2C Data line   | 3.8V | 4.0 V  |
| EZO 3 | SCL_ISO | Isolated Clock           | 3.8V | 4.0 V  |
| EZO 4 | VISO    | Isolated voltage output  | 3.8  | 4.0 V  |
| EZO 5 | PRB     | Probe Signal             | -    | -      |
| EZO 6 | PRB_GND | Probe Ground             | -    | -      |

The Whitebox T3 does not "occupy" any pin exclusively. The T3 is mostly transparent to other HATs - they can even be stacked on top and will work as usual.

![Whitebox T3](/_media/whitebox-t3-ports-4-5.jpg)


## Port 1 + 2
