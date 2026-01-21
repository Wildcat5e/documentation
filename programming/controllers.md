# Controllers

## Joystick Deadzones
Nicholas suggests using a scaled radial deadzone as done in the 2026-rebuilt-robot code and documented in these two resources:
<https://github.com/Minimuino/thumbstick-deadzones>
<https://joshsutphin.com/blog/doing-thumbstick-dead-zones-right.html>

## Scaled Input (Non-Linear Input)
A simple way to do this is to take the input value and raise it to the power of 3.
```java
Math.pow(rawInput, 3);
```
