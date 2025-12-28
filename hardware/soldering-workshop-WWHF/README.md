# WWHF 2026 soldering exercise

2 different circuits

through-hole, or surface-mount 1206 or 0603

## Simple circuit

2 LEDs light up whenever a battery is inserted

### part selection

2 LEDs of whichever colours you choose, for LED 1 and LED 2

- Red / Green / Yellow	1.8V..2.0V @ 20mA

- Blue / White	2.2V..2.4V @ 20mA


2 brightness-controlling resistors (one for each LED), for RES 1 and RES 2

- (V_battery - V_led) / I_led

 - e.g. (3 - 1.8(red)) / 0.02(bright) = 60 ohm

 - e.g. (3 - 2.4(white)) / 0.005(dim) = 30 ohm


1 battery holder

## more-complex circuit

555 timer astable multivibrator, alternates between 2 LEDs

### part selection

2 LEDs of whichever colours you choose, for LED 3 and LED 4

2 brightness-controlling resistors (one for each LED), for RES 3 and RES 4

1 555 timer IC

1 power-filtering capacitor, for CAP 12

- any value from 10nF up will be fine

1 timing-controlling capacitor, for CAP 11

- any value at all will work

2 timing-controlling resistors, for RES 11 and RES 12

- online calculator at https://allaboutcircuits.com/tools/555-timer-astable-circuit

- f = 1.44 / ((R_11 + 2 x R_12) x C_11)

- T_high = 0.694 x (R_11 + R_12) x C_11

- T_low = 0.694 x R_12 x C_11

 - e.g. f = 1.44 / ((100 + 2 x 900k) x 200n = 4 Hz, 50% duty

 - e.g. f = 1.44 / ((500k + 2 x 500k) x 100n = 9.6 Hz, 67% duty

1 battery holder, if your board does not yet have one

# identifying component values

## surface-mount resistors

Digits as read from the left give the value in ohms,
but the rightmost digit is the number of zeros to put onto the right.

- e.g. 104 = 10 0000 = 100 k ohms

- e.g. 562 = 56 00 = 5.6 k ohms

- e..g 470 = 47 ohms


## through-hole resistors

Colour bands from the left,
converted to digits, give the value in ohms,
but the rightmost band indicates the tolerance
and the second-rightmost band gives the number of zeros to put onto the right.

Ideally, there's a bigger gap between rightmost (tolerance) band and the others, to indicate orientation.
Or, the (left end of the) group of bands is closer to one end of the resistor body than the other.
But sometimes this can be hard to distinguish.
If you can't decide which of the colour bands is the right choice to start reading,
try reading it both ways. One way will give a "nonsense" value and the other way will be correct.

Or, just measure it with a multimeter - the official value will be whatever "preferred value" (see below) is closest to the measured value.

### [preferred values](https://en.wikipedia.org/wiki/E12_series)

Resistor values are only approximate (as indicated by their "tolerance"), and are only manufactured in a limited set of nominal values.
A "nonsense" value is any value that does not appear in that set - you will never find a standard resistor marked with a value outside that set.

| The "E12" series of values |
| --- |
| 1.0, 1.2, 1.5, 1.8, 2.2, 2.7, 3.3, 3.9, 4.7, 5.6, 6.8, 8.2 |

| The "E24" series of values |
| --- |
| 1.0, 1.1, 1.2, 1.3, 1.5, 1.6, 1.8, 2.0, 2.2, 2.4, 2.7, 3.0, 3.3, 3.6, 3.9, 4.3, 4.7, 5.1, 5.6, 6.2, 6.8, 7.5, 8.2, 9.1 |


### [colour code](https://en.wikipedia.org/wiki/Electronic_color_code)

Black = 0

Brown = 1

Red = 2

Orange = 3

Yellow = 4

Green = 5

Blue = 6

Violet or Purple = 7

Grey = 8

White = 9

Gold / Silver / Pink used for tolerance or obscure multiplier only

## examples

- e.g. Brown, Black, Yellow, tolerance... = 10 0000 = 100 k ohms

- e.g. Green, Blue, Red, tolerance... = 56 00 = 5.6 k ohms

- e..g Yello, Violet, Black, tolerance... = 47 ohms
