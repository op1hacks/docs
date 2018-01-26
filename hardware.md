# OP-1 Hardware

NOTE: This document is incomplete.


## Overview

The OP-1 is made up of the following parts:

- Aluminium Chassis
- Speaker
- UI Board
- Display
- DSP Board
- Battery
- IO Board
- Keyboard
- Ribbon cable (connects all PCB:s together)


## Display

The display size is listed as 320x160 pixels. In reality it's a lot bigger
vertically as part of it is hidden under the keyboard. The actual size is
320x240. In addition to this mismatch the actual visible portion of the
display is actually closer to 150px high.

 - Part Number: 74-X000045
 - Width: 68mm
 - Height: 49mm
 - Resolution: 320x240 px
 - Usable resolution: ~ 320x150 px


## Battery

The OP-1 battery is a 3.7V li-polymer battery rated at 1800 mAh.

 - Width: 70mm
 - Height: 50mm
 - Depth: 7mm
(Source: iFixit)[https://www.ifixit.com/Guide/Teenage+Engineering+OP-1+Battery+Replacement/65563]

The model number is 055070 and the connector type is *probably* a JST ACH.
(Source: operator-1.com)[https://www.operator-1.com/index.php?p=/discussion/comment/41372/#Comment_41372]
The connector on the PCB looks like BM02B-ACHSS-GAN-TF(LF)(SN) and the connector
on the battery looks like ACHR-02V-S.

TODO: Verify connector type and exact part number.


## DSP Board

- Main processor: ADSP-BF524C2

Additional info:

(Source: @Punji at operator-1.com)[https://www.operator-1.com/index.php?p=/discussion/comment/34440/#Comment_34440]

    The three S9C are Analog Devices ADG884 audio switches.
    The 23017 is an I/O expander.
    The 3576 is a power management IC with USB OTG support.
    The 5810D is an OLED power source.
    The 345B is an accelerometer IC.
    The LFKQ is a LTC2941 battery gas gauge monitor.

