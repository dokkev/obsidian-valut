## Powering the Optimo

There are two E-stops
- E-stop for the robot
- E-stop for the Power supply attached to the control box

Deactive the E-stop

## Powering off the Optimo

Activate the E-




### Send Commands to Arduino

Note: Don't ever change the firmware of Arduino

The Arduino inside the control box allows the Roboligent SDK to power the robot on.
Every time the Optimo computer is restarted, we have to send commands to Arduino over serial. On Arduino IDE, send `<r,s,0>` then `<r,s,1>` over the serial.


`usb/ACM1` - Arduino

## Communication

### EtherCAT

Run `ethercat0` to see EtherCAT status

EtherCAT 1 is master0 on PC.
master 1 is EtherCAT 2 on PC.
`ethercat0` to see EtherCAT status

### CAN

## Calibration
`usb/ACM0` - CAN transceiver


## How to luanch

Call Roboligent