---
icon: blender-phone
---

# 5804-Docs

Documentation for troubleshooting issues with FRC robots

## Table of Contents

1. [Hardware Info](./#hardware-info)
   1. [Common Cables](./#10-common-cables)
2. [Laptop Issues](./#laptop-issues)
   1. [1.0 Randomly E-Stopping](./#10-randomly-e-stopping)
   2. [2.0 Phoenix Tuner X cannot communicate with devices](./#20-phoenix-tuner-x-cannot-communicate-with-devices)
   3. [3.0 WPILib Updates](./#30-wpilib-updates)
3. [Pathplanner Issues](./#pathplanner-issues)
   1. [1.0 Bootlooping and Pathplanner cannot find settings sile](./#10-bootlooping-and-pathplanner-cannot-find-settings-file)
4. [CAN & CANivore Issues](./#can-and-canivore-issues)
   1. [1.0 Update CANivore firmware](./#10-update-canivore-firmware)
5. [Rio Logging](./#roborio)
   1. [1.0 Flashing roboRIO 2.0 firmware](./#10-flashing-roborio-20-firmware)
   2. [2.0 View RIO connection and power logs](./#20-view-roborio-connection-and-power-logs)
   3. [3.0 Delete roboRIO logs to create disk space](./#30-delete-roborio-logs-to-create-disk-space)
6. [Swerve Drive](./#swerve-drive)
   1. [1.0 Swerve randomly not setting zeroes correctly on robot startup](./#10-base-talon-fx-swerve-randomly-not-setting-zeroes-correctly-on-robot-startup)
7. [Vision](./#vision)
   1. [1.0 Coprocessor networking configuration](./#10-coprocessor-networking-configuration-for-photonvision)
   2. [2.0 PhotonVision camera calibration](./#20-photonvision-camera-calibration)
   3. [3.0 Exporting pipeline settings](./#30-exporting-pipeline-settings)
   4. [4.0 PhotonVision debugging](./#40-photonvision-debugging)

## Hardware Info

### 1.0 Common Cables

<details>

<summary>USB</summary>

[![USB 2.0 and 3.0 connectors.svg](https://upload.wikimedia.org/wikipedia/commons/8/82/USB_2.0_and_3.0_connectors.svg)](https://commons.wikimedia.org/wiki/File:USB_2.0_and_3.0_connectors.svg#/media/File:USB_2.0_and_3.0_connectors.svg)\
By [Milos.bmx](https://commons.wikimedia.org/w/index.php?title=User:Milos.bmx\&action=edit\&redlink=1), [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0), [Link](https://commons.wikimedia.org/w/index.php?curid=30414864)

[![USB Type-C icon.svg](https://upload.wikimedia.org/wikipedia/commons/9/98/USB_Type-C_icon.svg)](https://commons.wikimedia.org/wiki/File:USB_Type-C_icon.svg#/media/File:USB_Type-C_icon.svg)\
By [Niridya](https://commons.wikimedia.org/wiki/User:Niridya) - Own work based on: [USB Type-C.svg](https://commons.wikimedia.org/wiki/File:USB_Type-C.svg) by [Pietz](https://commons.wikimedia.org/wiki/User:Pietz), [CC0](http://creativecommons.org/publicdomain/zero/1.0/deed.en), [Link](https://commons.wikimedia.org/w/index.php?curid=74081486)

</details>

<details>

<summary>DisplayPort</summary>

**DisplayPort**

[![DisplayPort Connector.svg](https://upload.wikimedia.org/wikipedia/commons/f/f1/DisplayPort_Connector.svg)](https://commons.wikimedia.org/wiki/File:DisplayPort_Connector.svg#/media/File:DisplayPort_Connector.svg)\
By [Abisys](https://commons.wikimedia.org/wiki/User:Abisys) - Own work, [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0), [Link](https://commons.wikimedia.org/w/index.php?curid=4415244)

**Mini DisplayPort**

[![Mini DisplayPort (connector).PNG](https://upload.wikimedia.org/wikipedia/commons/7/7f/Mini_DisplayPort_\(connector\).PNG)](https://commons.wikimedia.org/wiki/File:Mini_DisplayPort_\(connector\).PNG#/media/File:Mini_DisplayPort_\(connector\).PNG)\
By [Tosaka](https://commons.wikimedia.org/w/index.php?title=User:Tosaka\&action=edit\&redlink=1), [CC BY 3.0](https://creativecommons.org/licenses/by/3.0), [Link](https://commons.wikimedia.org/w/index.php?curid=5989283)

</details>

<details>

<summary>HDMI</summary>

[![HDMI Connector Types.png](https://upload.wikimedia.org/wikipedia/commons/4/42/HDMI_Connector_Types.png)](https://commons.wikimedia.org/wiki/File:HDMI_Connector_Types.png#/media/File:HDMI_Connector_Types.png)\
By [C0nanPayne](https://commons.wikimedia.org/wiki/User:C0nanPayne) - Based on File:HDMI Connector.jpg, [CC0](http://creativecommons.org/publicdomain/zero/1.0/deed.en), [Link](https://commons.wikimedia.org/w/index.php?curid=58368257)

</details>

## Laptop Issues

### 1.0 Randomly E-Stopping

Spacebar can get jammed down

1. Press spacebar repeatedly to unstick it
2. Redeploy code/power cycle to restart the robot

### 2.0 [Phoenix Tuner X](https://v6.docs.ctr-electronics.com/en/2024/docs/tuner/index.html) cannot communicate with devices

1. Click the menu button in the top left of Phoenix tuner
2. Select driver station
3. If devices are still not detected, return to the devices section and run temporary diagnostics

### 3.0 WPILib Updates

1. In WPILib, press ctrl + shift + p.
2. Search "check for WPILib updates (online)." (Make sure you are on internet.)

## [Pathplanner](https://pathplanner.dev/home.html) Issues

### 1.0 Bootlooping and Pathplanner cannot find settings file

1. Open the Pathplanner app
2. Change a robot config in the Pathplanner settings
3. Redeploy code

## CAN and [CANIvore](https://v6.docs.ctr-electronics.com/en/2024/docs/canivore/canivore-intro.html#canivore-intro) Issues

### 1.0 Update CANivore firmware

1. Click the menu button in the top left of Phoenix tuner
2. Click into the CANivores tab
3. Update the CANivore

## Motor Issues

### 1.0 [CTR Talon FX Motors](https://v6.docs.ctr-electronics.com/en/2024/docs/hardware-reference/talonfx/index.html) will not spin

1. Check stator current limit in Phoenix tuner
2. Change it to 120 amps if it is really small (\~0.1)
3. Test to see if the motor spins now using Phoenix tuner
4. Redeploy code and check in Phoenix tuner if the motor's stator current limit has been set back to a small value
5. If the value has been reset, find the line of code that is applying that value as a constant and change it to 120 amps (or whatever current limit it should be)

## roboRIO

### 1.0 Flashing [roboRIO 2.0](https://www.ni.com/docs/en-US/bundle/roborio-20-umanual/page/umanual.html) firmware

1. Find either a USB-A to MicroSD adapter or a SD to MicroSD adapter
2. Take the MicroSD Card from the roboRIO
3.
4. Read [FRC Official docs](https://docs.wpilib.org/en/stable/docs/zero-to-robot/step-3/roborio2-imaging.html) if more thourough documentation is needed

### 2.0 View roboRIO connection and power logs

1. Click the gear icon next to the team number in FRC Driver Station
2. Click view log file

### 3.0 Delete roboRIO logs to create disk space

1. Navigate to the log extractor tool in the tools tab of Phoenix Tuner X
2. Press connect while connected to the robot
3. Select any logs that need to be downloaded or deleted

## Swerve Drive

### 1.0 [Base Talon FX Swerve](https://github.com/dirtbikerxz/BaseTalonFXSwerve) randomly not setting zeroes correctly on robot startup

1. Call swerve.resetModuleToAbsolute() (or equivalent method) twice at the top of RobotContainer

## Vision

### 1.0 Coprocessor networking configuration for [PhotonVision](https://docs.photonvision.org/en/latest/)

Note: Step order is very important

1. Set the static IP in the networking tab of Photonvision to 10.TE.AM.11 (for team #5804: 10.58.04.11)
2. Set the static IP for the RoboRIO to the default static IP
3. Power cycle the robot
4. Access the camera configuration settings at 10.TE.AM.11:5800 (for team #5804: 10.58.04.11:5800)
5. Read the [PhotonVision docs](https://docs.photonvision.org/en/latest/docs/quick-start/networking.html#networking) if more thourough documentation is needed

### 2.0 PhotonVision camera calibration

Note: Remember to change the camera lense focus by twisting the physical lense of the ArduCam. Do not use auto-exposure.

1. The maximum distance that an AprilTag can be detected at improves with higher resolution; however, increasing resolution has the negative side effect of lowering the framerate
2. When calibrating the camera, the chessboard/charuco must be held close to the camera in order for it to be detected at lower resolutions

### 3.0 Exporting pipeline settings

1. There is currently not possible to export only pipeline settings
2. Using the export settings button in the settings tab includes the ip address, and the cameras will not work share ip addresses

### 4.0 PhotonVision debugging

1. If the ip addresses for the cameras are inadvertantly overwritten, perform a software factory reset in the settings tab of the PhotobnVision software. Afterwards, the static ip must be reconfigured
2. Cameras must all be on the same version of the PhotonVision
