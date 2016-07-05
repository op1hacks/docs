# LFO Description

LFO types and their parameter values with:

 - Knob value type
 - Default value (based on latest official firmware 'op1_14203.op1')
 - Min value
 - Max value
 - The ^ symbol in the headers indicates the shift values (pressing shift and turning knob)


## Bend

 | Type       | Blue (1) | Green (2) | White (3) | Red (4) | ^Blue (5) | ^Green (6) | ^White  (7) | ^Red (8) |
 | ---        | ---      | ---       | ---       | ---     | ---       | ---        | ---         | ---      |
 | Default    |     7200 |      7100 |     32767 |       0 |         0 |          0 |           0 |     2048 |
 | Min        |     1024 |      1024 |    -32767 |    6208 |         0 |          0 |           0 |     1024 |
 | Max        |    15360 |      7168 |     32767 |    6208 |         0 |          0 |           0 |     3072 |

### Knobs

 - Blue (lfo knob dest)
 > 4 values: blue, green, white, red
 > min: 1024
 > max: 15360

 - Green (lfo engin dest)
 > 4 values: synth, envelope, fx, sound
 > min: 1024
 > max: 7168

 - White (lfo amount)
 > Scale: -100 - 100
 > min: -32767
 > max: 32767

 - Red (bend activation)
 > Value not clear
 > min: 6208
 > max: 6208

 - Shift Red (lfo direction)
 > 2 values: up, down
 > min: 1024
 > max: 3072


## Crank

 | ---        | Blue (1) | Green (2) | White (3) | Red (4) | ^Blue (5) | ^Green (6) | ^White  (7) | ^Red (8) |
 | ---        | ---      | ---       | ---       | ---     | ---       | ---        | ---         | ---      |
 | Defaults   |        0 |     16384 |      2000 |    2000 |         0 |          0 |           0 |        0 |
 | Min values |     -576 |         0 |      1024 |    1024 |      8512 |          0 |           0 |        0 |
 | Max values |     1280 |     32767 |      7168 |   15360 |     12992 |          0 |           0 |        0 |

### Knobs

 - Blue (crank speed)
 > Value not clear
 > min: -576
 > max: 1280

 - Green (lfo amount)
 > Scale 0 - 100
 > min: 0
 > max: 32767

 - White (lfo engin dest)
 > 4 values: synth, envelope, fx, sound
 > min: 1024
 > max: 7168

 - Red (lfo knob dest)
 > 4 values: blue, green, white, red
 > min: 1024
 > max: 15360


## Element

 | ---        | Blue (1) | Green (2) | White (3) | Red (4) | ^Blue (5) | ^Green (6) | ^White  (7) | ^Red (8) |
 | ---        | ---      | ---       | ---       | ---     | ---       | ---        | ---         | ---      |
 | Defaults   |     2000 |      4000 |      2000 |    2000 |         0 |          0 |           0 |        0 |
 | Min values |     1024 |    -32767 |      1024 |    1024 |         0 |          0 |           0 |        0 |
 | Max values |     7168 |     32767 |      7168 |   15360 |         0 |          0 |           0 |        0 |

### Knobs

 - Blue (source)
 > 4 values: g, mic, evelope, sigma (?)
 > min: 1024
 > max: 7168

 - Green (lfo amount)
 > Scale -100 - 100
 > min: -32767
 > max: 32767

 - White (lfo engin dest)
 > 4 values: synth, envelope, fx, sound
 > min: 1024
 > max: 7168

 - Red (lfo knob dest)
 > 4 values: blue, green, white, red
 > min: 1024
 > max: 15360


## Midi

TODO: check min & max values

 * Defaults: 2000, 2000, 2000, 2000, 2000, 2000, 2000, 2000

### Knobs

 - All Knobs (lfo knob dest)
 > 4 values: blue, green, white, red

 - All Knobs with Shift (lfo engine dest)
 > 4 values: synth, envelope, fx, sound


## Random

 | Type       | Blue (1) | Green (2) | White (3) | Red (4) | ^Blue (5) | ^Green (6) | ^White  (7) | ^Red (8) |
 | ---        | ---      | ---       | ---       | ---     | ---       | ---        | ---         | ---      |
 | Defaults   |     2000 |      4000 |      2000 |   24000 |         0 |          0 |           0 |        0 |
 | Min values |        0 |         0 |      1024 |       0 |         0 |          0 |           0 |        0 |
 | Max values |    32767 |     32767 |      5120 |   32767 |         0 |          0 |           0 |        0 |

### Knobs

 - Blue (lfo amount)
 > Scale: 0 - 100
 > min: 0
 > max: 32767

 - Green (lfo speed)
 > Scale: unclear (min to max is one knob revolution)
 > min: 0
 > max: 32767

 - White (lfo engine dest)
 > 4 values: synth, envelope, fx, sound
 > min: 1024
 > max: 5120

 - Red (lfo envelope)
 > Value not clear (min to max is six knob rotations, seems like a signed value)
 > min: 0
 > max: 32767


## Tremolo

 * Defaults:   ```16000,      0,      0, 16000, 0, 0, 0, 0
 * Min values: ```    0, -32767, -32767,     0, 0, 0, 0, 0
 * Max value:  ```32440,  32767,  32767, 32767, 0, 0, 0, 0

### Knobs

 - Blue (lfo speed)
 > Dual scale: 8 - 1 and dial with half a rotation
 > min: 0
 > max: 32440

 - Green (lfo pitch amount)
 > Scale: -100 - 100
 > min: -32767
 > max: 32767

 - White (lfo volume amount)
 > Scale: -100 - 100
 > min: -32767
 > max: 32767

 - Red (lfo envelope)
 > Value not clear (min to max is six knob rotations, seems like a signed value)
 > min: 0
 > max: 32767


## Value

TODO: Add all missing values

### Knobs

 - Blue (lfo speed)
 > Dual scale: 8 - 1 and dial with half a rotation

 - Green (lfo amount)
 > Scale: -100 - 100

 - White (lfo engine dest)
 > 4 values: synth, envelope, fx, sound

 - Red (lfo envelope)
 > Value not clear (min to max is six knob rotations, seems like a signed value)





