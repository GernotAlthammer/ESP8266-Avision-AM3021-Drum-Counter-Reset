# ESP8266 Avision AM3021 Drum-Counter Reset
Drum-Counter Reset for Avision AM3021 Laser Printer with ESP8266 ESPHome 

With der YAML code in the folder <a href="https://github.com/GernotAlthammer/ESP8266-Avision-AM3021-Drum-Counter-Reset/tree/main/ESPHome" rel="nofollow">ESPHome</a> for ES8266 the EEPROM chip HT24LC02 of the Drum-Unit can be re-programmed.
This sets the counter back to the state of health level of 100%. - like a brand new Drum-Unit :-)

The ESPHome code:
- works on any ESP8266 (NodeMCU, Wemos D1 mini, etc.)
- uses D1 = SCL and D2 = SDA (the usual ESPHome defaults)
- adds a button in Home Assistant to trigger the erase
- logs progress in ESPHome logs
- writes in 8‑byte pages (fastest + correct for 24LC02)

Required hardware:
- ESP8266 D1 mini (or equivalent board)
- connecting wires

Required software:
- ESPHome

<img src="https://github.com/GernotAlthammer/ESP8266-Avision-AM3021-Drum-Counter-Reset/blob/main/Pictures/ESP8266 HT24LC02 Wire Diagram.jpg" style="width: 50%;">

Note: I have
- soldered the wires for 3.3V/VCC and GND/VSS driectly to the chip pins (VSS Pin 4, VCC Pin 8).
- plugged the wires into the golden metal contact springs TP3 for SDA and TP4 for SCL 

<img src="https://github.com/GernotAlthammer/ESP8266-Avision-AM3021-Drum-Counter-Reset/blob/main/Pictures/Avision DR321-Chip.jpg" style="width: 25%;">

Info: the same counter is used in Lexmark TN-1070 toner unit

:-) 
