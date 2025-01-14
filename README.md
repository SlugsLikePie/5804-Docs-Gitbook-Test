# 5804-Troubleshooting-Docs
Documentation for troubleshooting issues with FRC robots

## Table of Contents
1. [Laptop Issues](#laptop-issues)
    1. [1.0 Randomly E-Stopping](#10-randomly-e-stopping)
    2. 
3. [Pathplanner Issues](#pathplanner-issues)
    1. [1.0 Bootlooping and Pathplanner Cannot Find Settings File](#10-bootlooping-and-pathplanner-cannot-find-settings-file)
    2. 
5. [CAN & Canivore Issues](#can-and-canivore-issues)
    1. [1.0 Don't know how to update Canivore firmware](#10-dont-know-how-to-update-canivore-firmware)
2. [Rio Logging](#rio-logging)
    1. [1.0 Want to view Rio connection and power logs](#10-view-rio-connection-and-power-logs)
2. [Swerve Drive](#swerve-drive)
    1. [1.0 Swerve randomly not setting zeroes correctly on robot startup](#10-swerve-randomly-not-setting-zeroes-correctly-on-robot-startup)


## Laptop Issues
### 1.0 Randomly E-Stopping
Spacebar can get jammed down
1. Press spacebar repeatedly to unstick it
2. Redeploy code/power cycle to restart the robot

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

## Rio Logging
### 1.0 View Rio connection and power logs
1. Click the gear icon next to the team number in FRC Driver Station
2. Click view log file

## Swerve Drive
### 1.0 Swerve randomly not setting zeroes correctly on robot startup
1. Call swerve.resetModuleToAbsolute() (or equivalent method) twice at the top of RobotContainer

