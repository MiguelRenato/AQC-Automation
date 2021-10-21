IOTizar-AQC

This automation on top of Tasmota is to control a underfloor heating system with Home Assistant.
#
- Frist step we have to do a hardware hack on sonoff th16 to get dry contact.
<img src="./pictures/sonoff th16 conversion.jpg" width="600">

#
- Second step will be flashing Tasmota on Sonoff TH16.
- 1- Goto https://tasmota.github.io/docs/devices/Sonoff-TH/ and read.
- 2- Get a FTDI Module and make wire connections like this
- <img src="./pictures/ftdi_module.jpg" width="150"> 
- 3.3v <-------> 3.3v
- GND <--------> GND
- TX <---------> RX
- RX <---------> TX
- 
- 3- Goto https://github.com/tasmota/tasmotizer and download Tasmotizer and happy hack.
- 

