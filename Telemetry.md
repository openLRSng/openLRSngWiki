This page is incomplete (obviously)

# Notes
## Asymmetric linkpower (1W TX vs 100mW RX)
When 1W TX module is used with 100mW RXs the range for telemetry is limited by the 100mW power of the RX. As TX side has more power (5 - 10 times) there is fairly large window where control is not affected while telemetry is totally lost.

## Serial port
When SBUS, Spektrum or SUMD is assigned as a pin output, the serial port (RX pinout) which is normally used for receiving telemetry data will be set to the baudrate of the serial protocol instead. For Spektrum and SUMD this is 115200 baud and for SBUS this is 100000 baud. This effectively means that the FrSky D and Smartport telemetry data will not be received as the baud rate is different, 9600 and 57600 respectively.

# Telemetry modes

## Passthru
In this mode data inputted on the serial port on TX is outputted on RX and vice versa. It should be noted that the amount of data passed thru is limited by the radiolink, if the radiolink capacity is exceeded data will be silently dropped. Approximate speed that data can be passed thru can be caluculated from refresh rate as it is possible to pass 8 bytes of data in each telemetry packet from RX to TX, TX->RX rate is half of that since every other packet is used by servo values.

## Smartport
This mode is compatible with FrSky Taranis, currently it only supports RSSI and two analog sensors from RX. It should be noted that FrSky uses inverted serial levels and thus a invertter is needed between openLRSng module and Taranis.

## FrSky
In this mode openLRSng emulates the behaviour of FrSky two way system (DxR-x). It should be noted that FrSky uses inverted serial levels and thus invertters may be needed to convert the serial signal.

## Mavlink
Development work on Mavlink telementry has been made availible in the [gitsly branch](https://github.com/openLRSng/openLRSng/tree/gitsly). The code is currently being reviewed for merger into the main branch.

# Connections

New JR modules like  [HawkEye Deluxe TX](https://github.com/openLRSng/openLRSngWiki/wiki/HawkEye-JR-Deluxe-TX-module) have a build in inverter both on RX and TX which can be set by jumpers on the board.
They do not require any hardware extension or modifiction.
  
For other hardware a simple one transistor inverter can be used for converting FrSky & SmartPort signals between:
* hub/hubless sensors to openLRS RX
* openLRS TX to FLD02
* openLRS TX & Taranis
* etc.

![Telemetry inverter](https://github.com/openLRSng/openLRSngWiki/raw/master/images/smartport_inverter.jpg)

Transistor can be virtually any small signal NPN, e.g. BC547, 2n2222
 
# Modification instructions and adapters
## HawkEye deluxeTX Taranis adapter circuit (adapter wire)
![dTX to Taranis adapter cable schematic](https://github.com/openLRSng/openLRSngWiki/raw/master/images/dtx_taranis_adapter.png)
## [Modifying DTF UHF deluxe TX for Taranis](https://www.dropbox.com/s/zl753t5qce8xgt9/DTFUHF_dTX_for_Taranis.pdf)
## [Modifying OrangeRX UHF TX for Taranis](https://www.dropbox.com/s/aw3g0rder8kgcqp/OrangeRX_UHF_TX_Taranis.pdf)
## [Modifying OrangeRX UHF 1W TX for Taranis](http://www.rcgroups.com/forums/showpost.php?p=26953006&postcount=2802)
## [Modifying HawkEye 1W for Taranis](https://www.dropbox.com/s/n7oi1bhu5ek2ndv/HawkEye_for_Taranis.pdf)
