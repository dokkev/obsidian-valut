## Problem Definition
Dynamics of a manipulator are represented by a nonlinear differential equation. However, linear control systems with approximations are widely used in industrial robot manipulators. 

## Summary of the methodology presented: algorithm, input-output
The methodology involves modeling a robotic manipulator with actuators which can produce torque at each joint and sensors using feedback control with second-order linear system. The controllers take desired trajectory and state (configuration) of the robot and outputs motion.

## Applicability / Problems solved 
This method is applicable to trajectory following in disturbance while ensuring the stability of the system. 

## Assumptions and limitations
It assumes that a robotic manipulator's nonlinear system can be approximated to a linear system.
Transmissions are modeled as a singular actuator at a joint. This method will experience instability in complex dynamic systems including 