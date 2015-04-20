### Hardware 

They JR module can be fit in the back of a JR compatible radio like the Taranis.
Currently (on the Taranis) only the PPM mode can be used to communicate between radio and module.
It is possible to have PPM setup on your TX unit and output a serial format (SBUS/Spektrum/SUMD) on the RX unit.

### HawkEye / DTF UHF 1W JR 

This module has 3 internal jumpers which can be accessed when the case is opened.

<b>Invert TX:ON|OFF (Default ON)</b><br>
This controls if the serial TX line is inverted or not. Should be set to "ON" for Frsky Taranis to allow telemetry operation. May need to be set depending on Telemetry mods on your TX unit.

<b>INVERT RX:ON|OFF (Default ON)</b><br>
This controls if the serial RX line is inverted. May need to be set depending on Telemetry mods on your TX unit.

<b>PPM Type:PPM|SERIAL (Default PPM)</b><br>
This controls where the 'pin 1' from the TX is connected to. For transmitters outputting PPM set to PPM. For SUMD/SBUS/Spektrum serial formats set to SERIAL, notably INVERT RX should be set too (SBUS:ON, SUMD/Spektrum OFF).

![JRDTX](https://raw.githubusercontent.com/openLRSng/openLRSngWiki/master/images/Hawkeye_JRDTX.jpg)
