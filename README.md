# ESP8266 Avision AM3021 Drum-Counter / Toner-Counter Reset

Read and Reset for Avision AM3021 Laser Printer with ESP8266 ESPHome
- for the DR321 Drum-Counter
- for the TN321 Toner-Counter 

With der YAML code in the folder <a href="https://github.com/GernotAlthammer/ESP8266-Avision-AM3021-Drum-Counter-Reset/tree/main/ESPHome" rel="nofollow">ESPHome</a> for ES8266 the EEPROM chip HT24LC02 of the Drum-Unit or the Toner-Unit can be re-programmed.
This sets the counter back to the state of health level of 100%. - like a brand new part :-)

The ESPHome code:
- works on any ESP8266 (NodeMCU, Wemos D1 mini, etc.)
- uses D1 = SCL and D2 = SDA (the usual ESPHome defaults)
- adds buttons in Home Assistant to trigger the read or erase
- reads EEPROM of DR321 from address 0x50 and EEPROM of TN321 from address 0x52
- writes 0x00 in 8‑byte pages (fastest + correct for 24LC02)
- logs progress in ESPHome logs

Required hardware:
- ESP8266 D1 mini (or equivalent board)
- connecting wires

Required software:
- ESPHome

<img src="https://github.com/GernotAlthammer/ESP8266-Avision-AM3021-Drum-Counter-Reset/blob/main/Pictures/ESP8266 HT24LC02 Wire Diagram.jpg" style="width: 50%;">

Note: For the DR321 Drum-Counter PCB i have
- soldered the wires for 3.3V/VCC and GND/VSS directly to the chip pins (VSS Pin 4, VCC Pin 8).
- plugged the wires into the golden metal contact springs TP3 for SDA and TP4 for SCL 

<img src="https://github.com/GernotAlthammer/ESP8266-Avision-AM3021-Drum-Counter-Reset/blob/main/Pictures/Avision DR321-Chip.jpg" style="width: 35%;">


Note: For the TN321 Toner-Counter PCB i have connected the wires directly to the PCB contact pads
- GND/VSS to Pad TP1
- 3.3V/VCC to Pad TP2
- SDA to Pad TP3
- SCL to Pad TP4 

<img src="https://github.com/GernotAlthammer/ESP8266-Avision-AM3021-Drum-Counter-Reset/blob/main/Pictures/Avision TN321-Chip.jpg" style="width: 35%;">


:-) 
