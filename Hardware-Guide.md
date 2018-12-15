General information on hardware
===============================
The following hardware is compatible with openLRSng:

* Flytron M2/M3 TX / OrangeRX UHF TX
* Flytron RX v2 / OrangeRX UHF RX / HawkEye RX
* openLRSngTX (and its derivatives) / HawkEye TX
* DTFUHF 4ch RX
* DTFUHF DeluxeTX

(list incomplete, see [Table of supported hardware](supported-hardware---feature-table)).  
All TX/RXs above are compatible with each other as well.

Note that some RXs can also be used as TXs with some additional hardware setup.

General information on inputs / outputs
=======================================
Servo channel outputs
---------------------
Servo PWM outputs can be mapped to any port. The DTF UHF 4-channel receiver has 6 such ports and the Hobbyking/Flytron RX has 13 such ports. The "extra" ports are the TX/RX and SDA/SCL pins. RC channels can be reused: for example, you may have RC channel 1 output on two different pins at the same time.

Special outputs
---------------
Other port configurations can only be mapped to one pin. These outputs include: High-frequency RSSI and LBEEP; serial TX and RX; i2c signals (SDA and SCL); and PPM. Similarly, analogue inputs can only be enabled on specific pins.
Receivers
=========

DTF UHF 4-channel
-----------------
![4ch](https://raw.githubusercontent.com/openLRSng/openLRSngWiki/master/images/4ch.png)

Version 2 and newer RXs also have the RSSI filter onboard, to filter High-Frequency RSSI into 0-3.3V RSSI. Enable the filter by soldering these two pads together:

![solder jumper](https://raw.githubusercontent.com/openLRSng/openLRSngWiki/master/images/jumper.png)

Hawkeye / Hobbyking / Flytron 9-channel
-----------------------------
![Hawkeye RX](https://raw.githubusercontent.com/openLRSng/openLRSngWiki/master/images/Hawkeye9ch.png)

![HK rx](https://raw.githubusercontent.com/openLRSng/openLRSngWiki/master/images/hk.png)

Note on Hawkeye 6ch/9ch ICSP pins
---------------------------------
Hawkeye 6ch/9ch receivers have non-standard ICSP pinout.

![Hawkeye ICSP](https://raw.githubusercontent.com/openLRSng/openLRSngWiki/master/images/hawkeye-6ch-9ch-isp.jpg)