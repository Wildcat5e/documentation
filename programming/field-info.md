# Field Information

## Welded vs. AndyMark

While both the Welded and AndyMark field layouts are approved for official play, slight dimensional variances exist between the two builds, which shift the exact coordinates of certain field elements and their corresponding AprilTags. This directly impacts the accuracy of global pose estimation and vision systems. Since different real-world fields utilize different field layouts, you must verify which layout will be in use at any event and [configure your software](#changing-the-field-layout) with the matching AprilTag layout map.

> As seen [in the Game Manual](https://firstfrc.blob.core.windows.net/frc2026/Manual/2026GameManual.pdf#page=20), the Peachtree District tyically uses the Welded layout.

## Changing the Field Layout

>— The field layout **must** be changed on the roboRIO. <br>
>— If using PhotonVision on a coprocessor, the field layout must **also** be changed through the PhotonVision UI.

### Changing the roboRIO's Field Layout

The field layout must be changed in the [Constants.java](https://github.com/Wildcat5e/2026-rebuilt-robot/blob/main/src/main/java/frc/robot/Constants.java) file:

```java
import edu.wpi.first.apriltag.AprilTagFieldLayout;
import edu.wpi.first.apriltag.AprilTagFields;

// Using the Welded layout
AprilTagFieldLayout FIELD_LAYOUT = AprilTagFieldLayout.loadField(AprilTagFields.k2026RebuiltWelded);

// Using the AndyMark layout
AprilTagFieldLayout FIELD_LAYOUT = AprilTagFieldLayout.loadField(AprilTagFields.k2026RebuiltAndymark);
```

### Changing the PhotonVision Coprocessor's Field Layout

The field layout must be changed through the PhotonVision UI. <br>
Follow these steps:

#### Download New Field Layout

1. Navigate to WPILib's [list of field layouts](https://github.com/wpilibsuite/allwpilib/tree/main/apriltag/src/main/native/resources/edu/wpi/first/apriltag).
2. Download the JSON file for the field layout you wish to import. For the 2026 season, we downloaded `2026-rebuilt-welded.json`.
3. Save the JSON file somewhere accessible on your computer.

#### Upload New Field Layout

1. Connect to the robot with the PhotonVision system active.
2. On the laptop connected to the robot, navigate to <http://photonvision.local:5800/> in a browser.
3. Using the left sidebar, navigate to the `Settings` panel.
4. Scoll down to the `AprilTag Field Layout` section to check which AprilTags have been loaded. It should be apparent from the number of AprilTags whether or not the correct layout is loaded (e.g. the 2025 layout has 22 AprilTags, the 2026 layout has 32).
5. Remaining in the `Settings` panel, scroll up and click on `Import Settings`.
6. Choose `Apriltag Layout` in the "Type" dropdown menu.
7. Upload the JSON file you saved to your computer earlier.
8. Go back to the `AprilTag Field Layout` section to ensure that the correct number of AprilTags have been loaded.
