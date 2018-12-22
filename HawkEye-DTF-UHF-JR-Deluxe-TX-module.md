# Hardware 

They JR module can be fit in the back of a JR compatible radio like the Taranis.
Currently (on the Taranis) only the PPM mode can be used to communicate between radio and module.
It is possible to have PPM setup on your TX unit and output a serial format (SBUS/Spektrum/SUMD) on the RX unit.

**Works out of the box for Taranis X9D**: I ordered this module in 2015/07, and all the jumpers were set so that it just worked with a Taranis (including RSSI telemetry). So there was no need to open it or adjust any jumpers -- merlin

# Interference with Taranis Electronics
Be advised that sending 800mW through some antennas like a dipole or a moxon, **will send enough RF back to your transmitter to confuse some analog channels. As a result, you will see S1, S2, and S3 values jump inexplicably**.
You can try covering your Taranis with aluminum foil shielding, or use a small antenna extension to move the antenna farther away from your Taranis.

# Internal jumper settings
![JRDTX](https://raw.githubusercontent.com/openLRSng/openLRSngWiki/master/images/Hawkeye_JRDTX.jpg)
## Invert TX:ON|OFF (Default ON)
This controls if the serial TX line is inverted or not. Should be set to "ON" for Frsky Taranis to allow telemetry operation. May need to be set depending on Telemetry mods on your TX unit.

## INVERT RX:ON|OFF (Default ON)
This controls if the serial RX line is inverted. May need to be set depending on Telemetry mods on your TX unit.

## PPM Type:PPM|SERIAL (Default PPM)
This controls where the 'pin 1' from the TX is connected to. For transmitters outputting PPM set to PPM. For SUMD/SBUS/Spektrum serial formats set to SERIAL, notably INVERT RX should be set too (SBUS:ON, SUMD/Spektrum OFF).