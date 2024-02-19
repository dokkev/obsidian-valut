## Powering the Optimo
Arduino inside the control box allows the Roboligent SDK to power the robot on.
Every time the Optimo computer is restarted, we have to send commands to Arduino over serial.

### Send Commands to Arduino


On Arduino IDE,  send `<r,s,0>` then `<r,s,1>` over the serial.



error while shared
sudo ldconfig /opt/

Don't ever change the firmware of Arduino


Every we restart the Optimo computer
Open Arduino IDE with Serial  Terminal
`<r,s,0>` then `<r,s,1>` over the serial;

ACM1 - Arduino
ACM0 - CAN transceiver
`ethercat0` to see ethercat status