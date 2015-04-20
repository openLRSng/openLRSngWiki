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

### OrangeRX TX as receiver 
It is possible to use the 1W OrangeRX TX as receiver allowing ~500mW telemetry.

7 outputs are available (all can be used for servo PWM)

1. buzzer driver transistor 'B' (PPM)
2. PPM IN pin (LBEEP,RSSI)
3. RFOUT pin (LLIND)
4. SDA pin (ANALOG input)
5. SCL pin (ANALOG input)
6. RXD pin (serial RX)
7. TXD pin (serial TX, SUMD, SPEKSAT, SBUS)

![OrangeRX TX as RX](https://raw.githubusercontent.com/openLRSng/openLRSngWiki/master/images/orange_tx_ppmout.jpg)
