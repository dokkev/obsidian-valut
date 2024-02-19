TODO: add plato guideline as well
## Powering the Optimo and PC

There are two E-stops for Optimo (TODO: add photos)
- E-stop for the robot
- E-stop for the Power supply attached to the control box

1. Deactivate the Power supply E-stop, then the power supply will start running.
2. Turn on the Optimo computer. The password is `optimo`

## Powering off the Optimo

1. Activate the Robot E-stop
2. Turn off the computer. 
3. Activate the Power E-stop. Make sure to do this after the computer is completely off

## Launching Optimo

### Send Commands to Arduino

Warning: DO NOT FLASH

The Arduino inside the control box allows the Roboligent SDK to power the robot on.
Every time the Optimo computer is restarted, we have to send commands to Arduino over serial. On Arduino IDE, send `<r,s,0>` then `<r,s,1>` over the serial.

`/dev/usb/ACM1` - Arduino

### Build and Run (Default mode)
The default directory for Roboligent SDK is `optimo_controller`
1. `cd ~/CODE/linkdyn_sdk/optimo_controller`
2. Run  `./dev.sh -c -a -r ./bin/optimo_controller` to build SDK and run Optimo Controller with GUI (optional) or Run `./dev.sh -r ./bin/optimo_controller` to run without build
	> `-c` : cmake
	> `-a` : all
	> `-r`: run

3. On GUI, click `start hardware`. This will take about a minute.
4. Once the hardware starts running. Click `enable`. This will release the mechanical brakes on joints.

## Optimo Examples
There are other ways to launch the robot with ROS 2 features. Refer to:
https://roboligent.bitbucket.io/examples/index.html


## Communication

### EtherCAT
Run `ethercat0 master` to see EtherCAT status

Optimo computer has two Ethernet ports. Run `ethercat0 master`  to see EtherCAT status
- `EtherCAT1` is `master0` on PC.
- `master1` is `EtherCAT2` on PC.

### CAN
CAN is initiated with Optimo Controller with 500 kbps on `can0`. Run `candump can0` to see CAN messages

`/dev/usb/ACM0` - USB CAN transceiver

## Calibration

Call Roboligent