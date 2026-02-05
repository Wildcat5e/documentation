# Controllers

## Field Centric Alliance Color Direction

Phoenix Tuner's Drivetrain will set the direction that the Field Centric control faces based on Alliance while the Driver Station is disabled. Be careful when simulating that you don't get all confused.

## Joystick Deadzones

Nicholas suggests using a scaled radial deadzone as done in the 2026-rebuilt-robot code and documented in these two resources:
<https://github.com/Minimuino/thumbstick-deadzones>
<https://joshsutphin.com/blog/doing-thumbstick-dead-zones-right.html>

## Scaled Input (Non-Linear Input)

A simple way to do this is to take the input value and raise it to the power of 3.

```java
Math.pow(rawInput, 3);
```
