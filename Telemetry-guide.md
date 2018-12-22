This page is incomplete. Please have a look at these pages for more details:
* http://flyingforfun.weebly.com/open-lrs.html
* https://hackpad.com/ep/pad/static/zpJZqq8H2Qq
* http://diydrones.com/forum/topics/mavlink-ardupilot-opentx-extension
* http://www.rcgroups.com/forums/showthread.php?t=1913501
* If you care about mavlink on openlrs, you can also look at UltimateLRS (Orange only as of 2015/12): http://www.itluxembourg.lu/site/ https://vimeo.com/133086385 https://vimeo.com/137746307

# Notes
## Asymmetric linkpower (1W TX vs 100mW RX)
When 1W TX module is used with 100mW RXs the range for telemetry is limited by the 100mW power of the RX. As TX side has more power (5 - 10 times) there is fairly large window where control is not affected while telemetry is totally lost.

## Serial protocols using the same serial port
**You cannot use SBUS, Spektrum or SUMD and use serial telemetry at the same time**:  
When SBUS, Spektrum or SUMD is assigned as a pin output, the serial port (RX pinout) used for receiving telemetry data will be set to the baudrate of the serial protocol that is used. For Spektrum and SUMD this is 115200 baud and for SBUS this is 100000 baud. 
This effectively means that the FrSky D and Smartport with a baud rate of 9600 and 57600 respectively will affect serial passthrough (but basic telemetry for RSSI and passing on analog A1/A2 will work with both FrSky D and Smartport).

# Telemetry modes

## Passthru
In this mode data inputted on the serial port on TX is outputted on RX and vice versa. It should be noted that the amount of data passed thru is limited by the radiolink, if the radiolink capacity is exceeded data will be silently dropped. Approximate speed that data can be passed thru can be caluculated from refresh rate as it is possible to pass 8 bytes of data in each telemetry packet from RX to TX, TX->RX rate is half of that since every other packet is used by servo values.

## Smartport
This mode is compatible with FrSky Taranis, currently it only supports RSSI and two analog sensors from RX (setup one port as SDA, one as SCL and they will be your 2 analog values you can input on the line wire. Be careful not to exceed 3.3V (or 5V depending on your module)).  
It should be noted that FrSky uses inverted serial levels and thus a inverter may be needed between openLRSng module and Taranis (not true with "DTF UHF 1-watt Deluxe TX JR Module" which is already inverted by default, and just works).   Kha also says at http://www.rcgroups.com/forums/showpost.php?p=33375743&postcount=1732 that "Smartport is not that complete for now" (2015/12). Try the FrSky protocol instead if you don't need Smartport.  
Selecting 2 output ports as ANALOG does send their value to A1 and A2 in the Frsky telemetry page (but this doesn't work on a Broversity RX module where SDA and SCL ought to be usable as analog input)

## FrSky
In this mode openLRSng emulates the behaviour of FrSky two way system (DxR-x). It should be noted that FrSky uses inverted serial levels and thus inverters may be needed to convert the serial signal (again "DTF UHF 1-watt Deluxe TX JR Module" is already inverted by default, and just works).  
Frsky supports serial telemetry passthrough and external sensors (sensor hub), so it can pass more data than Smartport support  
To learn the basics on Frsky D telemetry, see: https://www.youtube.com/watch?v=mkHSORoEcAM  
Selecting 2 output ports as ANALOG does send their value to A1 and A2 in the Frsky telemetry page (but this doesn't work on a Broversity RX module where SDA and SCL ought to be usable as analog input)

## Mavlink
Development work on Mavlink telementry has been made availible in the [gitsly branch](https://github.com/openLRSng/openLRSng/tree/gitsly). Sadly since the openlrsng code now seems frozen in time (2017), it does not look like this branch will ever be merged, but hopefully it should work on its own.

# Connections

New JR modules like  [HawkEye Deluxe TX](https://github.com/openLRSng/openLRSngWiki/wiki/HawkEye-JR-Deluxe-TX-module) have a build in inverter both on RX and TX which can be set by jumpers on the board (by default the JR Hawkeye TX module just works, no need to change the jumpers).
  
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
## [Modifying DTF UHF deluxe TX for Taranis](https://www.dropbox.com/s/zl753t5qce8xgt9/DTFUHF_dTX_for_Taranis.pdf) (note, this is for the standalone TX, not the JR TX module which does not need to be modified)
## [Modifying OrangeRX UHF TX for Taranis](https://www.dropbox.com/s/aw3g0rder8kgcqp/OrangeRX_UHF_TX_Taranis.pdf)
## [Modifying OrangeRX UHF 1W TX for Taranis](http://www.rcgroups.com/forums/showpost.php?p=26953006&postcount=2802)
## [Modifying HawkEye 1W for Taranis](https://www.dropbox.com/s/n7oi1bhu5ek2ndv/HawkEye_for_Taranis.pdf)