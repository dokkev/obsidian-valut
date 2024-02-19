## Powering the Optimo





### Send Commands to Arduino

Note: Don't ever change the firmware of Arduino

The Arduino inside the control box allows the Roboligent SDK to power the robot on.
Every time the Optimo computer is restarted, we have to send commands to Arduino over serial. On Arduino IDE,  send `<r,s,0>` then `<r,s,1>` over the serial.

`usb/ACM1` 


error while shared
sudo ldconfig /opt/



ACM1 - Arduino
ACM0 - CAN transceiver
`ethercat0` to see ethercat status