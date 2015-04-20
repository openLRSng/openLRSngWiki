## HawkEye Deluxe TX
<b>What is the use of the "Serial" port on the bottom of the Deluxe Tx ? and how is it used ?</b><br>
The serial port can be used for telemetry or for inputting serial RC protocol such as SBUS/SpektrumSAT/SUMD.

<b>What is the use of the "I2C" port on the bottom of the Deluxe Tx ? and how is it used ?</b><br>
This is cuurently unused, however in future updates this can be used to connect two channel analog joystick (directly) or a I2C sensor for headtracking purposes.

<b>Where is the schematics of the hamkeye hardware ?</b><br>
The hawkeye schematics/board designs are not available via us, however the HawkEye deluxeTX is pretty much exactly same as the DTF-UHF deluxeTX https://github.com/DTFUHF/DTFUHF-1W-Deluxe

<b>Where is the ports and leds exhaustive description of their functions and meanings of the tx ?</b><br>
LEDs https://github.com/openLRSng/openLRSng/wiki/Basic-functions-guide#led-information
Ports, see above.

<b>What it the corresponding emitting power (in watts) of the 0 to 7 levels that can be configured in the chrome configurator ?</b><br>
This varies a bit but 5 = ~500mW, 6 = ~600mW,  7= ~800mW. It is not recommended to use powerlevels 0-4 as they may be unreliable on 1W modules.

<b>What is the advised way to power the Tx unit : is it sufficient to have the three "GND-BATT-PPM" wire connected to the Taranis external connector or not ?</b><br>
Yes, Taranis is able to give adequate power to the unit. The unit has internal DCDC converter and may consume upto around 3W (telemetry off, max power). This is about 250mA at 12V.

## HawkEye 6ch RX
<b>What is the purpose of the provided jumper</b><br>
The jumper is provided for convinience and may be used to to short ch1-ch2 to enable forced bind, or ch3-ch4 to enable 'spectrum analyzer mode'. By default it is plugged on two GND pins and may be left there or removed.

<b>What is the RSSI & PWM pin voltage and range ? Is it an analog signal or a PWM rssi ?</b><br>
The CH3/RSSI pin can be configured to various modes
* PWM RSSI (8kHz 0-100% dutycycle) can be converted to 0-3.3V analog by enabling the onboard filter.
* LBEEP this is a special mode in which audible signal is output from the pin when packets are lost, this can be directly or via simple circuit be connected to FPV vTX
* normal channel output, any servo channel can be configured (RSSI as servo PWM can be achieved using the 'RSSI injection feaature')

<b>Is the schematic available</b><br>
Directly no, however it is based on DTFUHF 6ch https://github.com/DTFUHF/DTFUHF-6ch

## Hawkeye 9ch RX
<b>What is the RSSI & PWM pin voltage and range ? Is it an analog signal or a PWM rssi ?</b><br>
See 6ch above.

<b>What is the PINs mapping of 3-pins rows on the receiver : signal, ground, Voltage ? (which row is what ?)
From board edge inwards: GND, +5(6)V, signal. https://github.com/openLRSng/openLRSng/wiki/Hardware-Guide
