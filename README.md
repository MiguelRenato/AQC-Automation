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
 
- 3- Goto https://github.com/tasmota/tasmotizer and download Tasmotizer and happy hack.

- In case you have doubts don't forget make a Googling, this is a very documented subject on the internet and that's why I won't go into detail.
After Tasmota is connected to your wifi and configured as "Sonoff TH" let's move on or next step.

#
- Third step we go to the tasmota console and create the following RULES.
<img src="./pictures/consola_tasmota.png">

- Rule 1 create a thermo switch automation with a setpoint of 24°C.

```
Rule1 ON DS18B20#Temperature<24 DO Power1 0 ENDON ON DS18B20#Temperature>24.5 DO Power1 1 ENDON
```
Save Rule1 
```
Rule1 5
```
