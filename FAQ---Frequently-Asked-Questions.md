# Software topics

# Hardware topics
## Generic
## HawkEye Deluxe TX
### What is the use of the "Serial" port on the bottom of the Deluxe Tx ? and how is it used ?
The serial port can be used for telemetry or for inputting serial RC protocol such as SBUS/SpektrumSAT/SUMD. In the case of a Taranis, you likely want to use PPM output and keep the serial port for serial passthrough.

### What is the use of the "I2C" port on the bottom of the Deluxe Tx ? and how is it used ?
This is currently unused, however in future updates this can be used to connect two channel analog joystick (directly) or a I2C sensor for headtracking purposes.

### Where is the schematics of the hawkeye hardware ?
The hawkeye schematics/board designs are not available via us, however the HawkEye deluxeTX is pretty much exactly same as the DTF-UHF deluxeTX https://github.com/DTFUHF/DTFUHF-1W-Deluxe

### Where is the ports and leds exhaustive description of their functions and meanings of the tx ?
[[See LED Information at the end of the Basic Functions page|Basic-functions-guide#led-information]]


### What it the corresponding emitting power (in watts) of the 0 to 7 levels that can be configured in the chrome configurator ?
This varies a bit but 5 = ~500mW, 6 = ~600mW,  7= ~800mW. It is not recommended to use power levels 0-4 as they may be unreliable on 1W modules.

### What is the advised way to power the Tx unit : is it sufficient to have the three "GND-BATT-PPM" wire connected to the Taranis external connector or not ?
Yes, Taranis is able to give adequate power to the unit. The unit has internal DCDC converter and may consume upto around 3W (telemetry off, max power). This is about 250mA at 12V.

## HawkEye 6ch RX
### What is the purpose of the provided jumper
The jumper is provided for convenience and may be used to to short ch1-ch2 to enable forced bind, or ch3-ch4 to enable 'spectrum analyzer mode'. By default it is plugged on two GND pins and may be left there or removed.

### What is the RSSI & PWM pin voltage and range ? Is it an analog signal or a PWM rssi ?
The CH3/RSSI pin can be configured to various modes
* PWM RSSI (8kHz 0-100% dutycycle) can be converted to 0-3.3V analog by enabling the onboard filter.
* LBEEP this is a special mode in which audible signal is output from the pin when packets are lost, this can be directly or via simple circuit be connected to FPV vTX
* normal channel output, any servo channel can be configured (RSSI as servo PWM can be achieved using the 'RSSI injection feature')

### Is the schematic available
Directly no, however it is based on DTFUHF 6ch https://github.com/DTFUHF/DTFUHF-6ch

## Hawkeye 9ch RX
### What is the RSSI & PWM pin voltage and range ? Is it an analog signal or a PWM rssi ?
See 6ch above.
### What is the PINs mapping of 3-pins rows on the receiver : signal, ground, Voltage ? (which row is what ?)
From board edge inwards: GND, +5(6)V, signal. [[Hardware Guide|Hardware-Guide]]
