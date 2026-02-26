# ESP8266 Avision AM3021 Drum-Counter Reset
Drum-Counter Reset for Avision AM3021 Laser Printer with ESP8266 ESPHome 

With der ESPHome code for ES8266 the EEPROM chip HT24LC02 of the Drum-Unit can be re-programmed.
This sets the counter back to the state of health level of 100%.

Required hardware:
- ESP8266 D1 mini (or equivalent board)
- connecting wires

Required software:
- ESPHome

Note: I have
- soldered the wires for 3.3V/VCC and GND/VSS driectly to the chip pins (VSS Pin 4, VCC Pin 8).
- plugged the wires for SCL and SDA into the golden metal contact springs 

:-) 
