# 5804-Docs
Documentation for troubleshooting issues with FRC robots

## Table of Contents
1. [Hardware Info](#hardware-info)
    1. [USB](#usb)
3. [Laptop Issues](#laptop-issues)
    1. [1.0 Randomly E-Stopping](#10-randomly-e-stopping)
    2. 
4. [Pathplanner Issues](#pathplanner-issues)
    1. [1.0 Bootlooping and Pathplanner Cannot Find Settings File](#10-bootlooping-and-pathplanner-cannot-find-settings-file)
    2. 
5. [CAN & Canivore Issues](#can-and-canivore-issues)
    1. [1.0 Don't know how to update Canivore firmware](#10-dont-know-how-to-update-canivore-firmware)
6. [Rio Logging](#rio-logging)
    1. [1.0 Flashing roboRIO 2.0](#10-flashing-roborio-20)
    2. [1.0 Want to view Rio connection and power logs](#10-view-roborio-connection-and-power-logs)
7. [Swerve Drive](#swerve-drive)
    1. [1.0 Swerve randomly not setting zeroes correctly on robot startup](#10-swerve-randomly-not-setting-zeroes-correctly-on-robot-startup)
8. [Vision](#vision)
    1. [1.0 Camera Setup Issues](#10-camera-setup-issues)

## Hardware Info
### What cable is this?
#### [USB](https://en.wikipedia.org/wiki/USB_hardware) (Universal Serial Bus)
<p><a href="https://commons.wikimedia.org/wiki/File:USB_2.0_and_3.0_connectors.svg#/media/File:USB_2.0_and_3.0_connectors.svg"><img src="https://upload.wikimedia.org/wikipedia/commons/8/82/USB_2.0_and_3.0_connectors.svg" alt="USB 2.0 and 3.0 connectors.svg" height="476" width="640"></a><br>By <a href="//commons.wikimedia.org/w/index.php?title=User:Milos.bmx&amp;action=edit&amp;redlink=1" class="new" title="User:Milos.bmx (page does not exist)">Milos.bmx</a>, <a href="https://creativecommons.org/licenses/by-sa/3.0" title="Creative Commons Attribution-Share Alike 3.0">CC BY-SA 3.0</a>, <a href="https://commons.wikimedia.org/w/index.php?curid=30414864">Link</a></p>

## Laptop Issues
### 1.0 Randomly E-Stopping
Spacebar can get jammed down
1. Press spacebar repeatedly to unstick it
2. Redeploy code/power cycle to restart the robot

### 2.0 Phoenix Tuner X cannot communicate with devices
1. Click the menu button in the top left of Phoenix tuner
2. Select driver station
3. If devices are still not detected, return to the devices section and run temporary diagnostics

## Pathplanner Issues
### 1.0 Bootlooping and Pathplanner Cannot Find Settings File
1. Open the Pathplanner app
2. Change a robot config in the Pathplanner settings
3. Redeploy code

## CAN and Canivore Issues
### 1.0 Don't know how to update Canivore firmware
1. Click the menu button in the top left of Phoenix tuner
2. Click into the Canivores tab
3. Update the Canivore

## Motor Issues
### 1.0 Motors will not spin
1. Check stator current limit in Phoenix tuner
2. Change it to 120 amps if it is really small (~0.1)
3. Test to see if the motor spins now using Phoenix tuner
4. Redeploy code and check in Phoenix tuner if the motor's stator current limit has been set back to a small value
5. If the value has been reset, find the line of code that is applying that value as a constant and change it to 120 amps (or whatever current limit it should be)

## roboRIO
### 1.0 Flashing roboRIO 2.0
1. Find either a USB-A to MicroSD adapter or a SD to MicroSD adapter
2. 
3. Read [FRC Official docs](https://docs.wpilib.org/en/stable/docs/zero-to-robot/step-3/roborio2-imaging.html) for more thourough documentation
### 1.0 View roboRIO connection and power logs
1. Click the gear icon next to the team number in FRC Driver Station
2. Click view log file

## Swerve Drive
### 1.0 Swerve randomly not setting zeroes correctly on robot startup
1. Call swerve.resetModuleToAbsolute() (or equivalent method) twice at the top of RobotContainer

## Vision
### 1.0 Camera setup
1. Set the static IP in the networking tab of Photonvision
2. THEN Set the static IP for the RoboRIO
3. Power cycle the robot
4. Access the camera configuration settings at the new static IP


