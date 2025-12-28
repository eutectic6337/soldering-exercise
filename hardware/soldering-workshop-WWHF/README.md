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

- allaboutcircuits.com/tools/555-timer-astable-circuit

- f = 1.44 / ((R_11 + 2 x R_12) x C_11)

- T_high = 0.694 x (R_11 + R_12) x C_11

- T_low = 0.694 x R_12 x C_11

 - e.g. f = 1.44 / ((100 + 2 x 900k) x 200n = 4 Hz, 50% duty

 - e.g. f = 1.44 / ((500k + 2 x 500k) x 100n = 9.6 Hz, 67% duty

1 battery holder, if your board does not yet have one
