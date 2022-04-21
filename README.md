# M2_WiFi-Based-RTV-IR-Remote-Range-Extender
The aim for this project was to design and develop a device which can be used to extend range of IR communication between RTV remote and RTV device using WiFi. It was latter extended to provide the functionality of controlling RTV devices with a PC or smartphone connected trough WiFi to the device (a web application is presented on the screen).
The device consists of two cooperating parts in client-server architecture:
client part that receives IR code from RTV remote (with IR receiver) and sends it trough WiFi (with ESP8266) to another part,
server part that receives code trough WiFi (with ESP8266) and sends it trough IR (with IR LED + amplifier) to RTV device.
Each part consists of IR element (LED or receiver with demodulation IC), AVR ATmega 328P uC programmed using Arduino libraries and an ESP8266 WiFi module running NodeMCU firmware.
To decode and encode IR codes I used IRremote library.
PC/smartphone can also be a client and connect to a server part.
ESP8266 module can act as an access point and a client at the same time, so there is an option to connect the server part to router and control the device from PC/smartphone connected to the same LAN network - configurable in webapp.
