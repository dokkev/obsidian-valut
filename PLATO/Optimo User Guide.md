## Powering the Optimo



### Send Commands to Arduino

Note: Don't ever change the firmware of Arduino

The Arduino inside the control box allows the Roboligent SDK to power the robot on.
Every time the Optimo computer is restarted, we have to send commands to Arduino over serial. On Arduino IDE,  send `<r,s,0>` then `<r,s,1>` over the serial.

`usb/ACM1` - Arduino


error while shared
sudo ldconfig /opt/



## Communication
`ethercat0` to see ethercat status

Ether 1 is master0 on PC
master 1 is EtherCAT 2 on PC

## Calibration
`usb/ACM0` - CAN transceiver

Call Roboligent