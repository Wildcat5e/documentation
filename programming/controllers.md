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

## Using [Nicholas's Controller](https://github.com/Wildcat5e/2026-rebuilt-robot/blob/671255baf85ac57c4cc5b37cf3424e4658026970/src/main/java/frc/robot/controller/Controller.java)

### Basic Usage

Driving should already work assuming you're passing in a swerve drive drivetrain. Keybind will require you to go in and rename the abstract methods and implementing methods for each controller and set the keybind you want in the specific controller, and then update what those keybinds do in `bindingsSetup()`.

### Controller Axis

You should note that the axes are flipped within individual controller implementations to match the [WPILib coordinate system](https://docs.wpilib.org/en/stable/docs/software/basic-programming/coordinate-system.html).
