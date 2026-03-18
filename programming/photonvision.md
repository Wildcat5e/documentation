# PhotonVision

## Re-Image the Coprocessor

Every year at the start of the season, you should flash the latest stable image to your vision coprocessor.

You can then offline update using the provided jar files for later updates with the same year. (`v2025.3.1` re-image to `v2026.1.1`, `v2026.1.1` offline update with jar to `v2026.3.2`.)

## Field

Make sure to set the correct field (especially if running last year's PhotonVision). You need to set it in the PhotonVision WebUI even if you already did it in the robot code.

`CoprocMultiTag` relies on the field provided in the PhotonVision WebUI while other methods that run on the RIO rely on the one specified in the robot code.