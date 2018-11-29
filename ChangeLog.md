# Changelog

All notable changes to this project will be documented in this file.

# [v0.4.4] - 2018-11-29

## Added

- Script FinchCalibration: class FinchCalibration:
     - public static void LoadStep(int stepId) - New function to load certain calibration step.

## Remove

- Script DashCalibrationStep: class DashCalibrationStep:
     - public float TimeToCalibrate.

- Script FinchScanner: enum FinchScannerType
     - Field AB.

- Script FinchScanner: class FinchScanner
     - Field public int ThressholdRssi.

- Script FinchControllerVisual: class FinchControllerVisual
     - Field: public float MaxAngleRotation.
     - Field: public float TouchPadRadius.
     - Field: public float TouchPointRadius.
     - Field: public float ScaleTimer.

## Fix
- Fix crash on PC

# [v0.4.3] - 2018-11-15

## Added

- Add Finch Unity SDK version in Finch script.

# [v0.4.2] - 2018-11-15

## Changed

- Skipping a step in the calibration for Shift controllers is done with a press, and for Dash controllers for a long press.

## Fix

- Fixed broken reconnect caused by scanning stops.

# [v0.4.1] - 2018-11-15

## Fix

- Fixed scanner behaviour: scanner re-launched before it had a chance to pair controllers.

# [v0.4.0] - 2018-11-14

## Added

- Script FinchCalibration: class FinchCalibration:
    - public TutorialStep IncorrectSet - New tutorial step added in case of nodes disconnection.

- Script PlayableSet: class PlayableSet - New class added for tracking the nodes disconnection.

- Script DashHandednessChooser: class DashHandednessChooser - New class added for defining chirality in case when only one dash is connected.

## Changed

- Calibration button binding changed inside calibration module: ThumbButton -> HomeButton.

# [v0.3.0] - 2018-11-07

## Added

- Dcript FinchControllerVisual: class BatteryLevel - New class added to pass battery level to the indication sprite.

- Prefab FinchDash - includes 2 Finch Dash controller objects, Dash calibration objects and a camera. Finch script is assigned to the FinchDash object.

- Prefab FinchShift - includes 2 Finch Shift controller objects, Shift calibration objects and a camera. Finch script is assigned to the FinchShift object.

- Script Finch: enum CalibrationType - calibration type enumerator.

- Script FinchCalibration: class FinchCalibration
    - public TutorialStep[] FastCalibration - fast calibration tutorial steps.

## Remove

- Script FinchScanner: class FinchScanner.

## Change

- Prefab Dash -> DashController.

- Prefab Shift -> ShiftController.

- Script FinchCalibration: class FinchCalibration Steps -> FullCalibration.

- Script FinchControllerVisual: class FinchControllerVisual public Sprite[] BatteryMaterials -> public BatteryLevel[] BatteryLevels.

- Script Finch to script ScannerStep (enum FinchIOScanner -> enum FinchScannerType).
