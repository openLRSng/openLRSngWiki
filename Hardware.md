### General information
All TX/RXs are compatible with each other. Some RXs can also be used as TXs.

All receivers support 2 x analog input / I2C / telemetry serial port / up to 16ch PPM.

####Servo channel outputs
Servo PWM outputs can be mapped to any port. The DTF UHF 4-channel receiver has 6 such ports and the Hobbyking/Flytron RX has 13 such ports. The "extra" ports are the TX/RX and SDA/SCL pins. RC channels can be reused: for example, you may have RC channel 1 output on two different pins at the same time.

####Special outputs
Other port configurations can only be mapped to one pin. These outputs include: High-frequency RSSI and LBEEP; serial TX and RX; i2c signals (SDA and SCL); and PPM. Similarly, analogue inputs can only be enabled on specific pins.

### Transmitter hardware
| Name | Hardware type(no) | PPM input by timer | output power (unmodified) | integrated RF lowpass filter | integrated USB | link |
| ---- | ------------------| ------------------ | ------------------------- | ---------------------------- | -------------- | ---- |
| Hawkeye openLRSng (JR/Futaba) | 4 | yes | 400-800mW | - | no | [link](http://www.hobbiesfly.com/transmitter-receiver/hawkeye-openlrs-uhf-system-jr-turnigy-taranis-compatible.html) 
| Hawkeye DTFUHF deluxe JR | 4 | yes | 400-800mW | 490MHZ | yes | [link](http://www.hobbiesfly.com/transmitter-receiver/dtf-uhf-deluxetx-taranis-jr-turnigy-compatible.html)
|Hawkeye/DTFUHF deluxe TX | 6 | yes | 400-800mW | 490MHz | yes | [link](http://www.hobbiesfly.com/transmitter-receiver/dtf-uhf-deluxetx-transmitter.html)
|Flytron M1 (100mW) | 0 | no | 1.2-100mW | - | no | N/A
|OrangeRX openLRS / Flytron M2 (100mW) | 2 | no | 1.2-100mW | - | no | [link](https://www.hobbyking.com/hobbyking/store/__27095__OrangeRx_Open_LRS_433MHz_TX_Module_JR_Turnigy_compatible_.html)
|OrangeRX openLRS / Flytron M3 (1W) | 2 | no | 250-500mW | - | no | [link](https://www.hobbyking.com/hobbyking/store/__40031__OrangeRX_Open_LRS_433MHz_Transmitter_1W_compatible_with_Futaba_radio_.html)
|OrangeRX/Flytron 9ch RX | 3 | yes | 1.2-100mW | - | no | [link](https://www.hobbyking.com/hobbyking/store/__27096__OrangeRx_Open_LRS_433MHz_9Ch_Receiver.html)
|Hawkeye 9ch RX (blue) | 3 | yes | 1.2-100mW | - | no | [link](http://www.hobbiesfly.com/transmitter-receiver/hawkeye-9-channel-receiver.html)
|Hawkeye 9ch RX (black) | 3 | yes | 1.2-100mW | 490MHz | no | [link](http://www.hobbiesfly.com/transmitter-receiver/hawkeye-9-channel-long-range-receiver.html)
|Hawkeye/DTFUHF 6(/4)ch | 5 | yes | 1.2-100mW | 490MHz | no | [link](http://www.hobbiesfly.com/transmitter-receiver/dtf-uhf-6-channel-long-range-receiver.html)

### Receiver hardware
| Name | Hardware type(no) | output power (unmodified) | integrated RF lowpass filter | max PWM outputs | improved power filtering | USB | size | link |
| ---- | ----------------- | ------------------------- | ---------------------------- | --------------- | ------------------------ | --- | ---- | ---- |
|OrangeRX 9ch RX | 3 | 1.2-100mW | - | 13 | no | - | 51x28x16mm 10.0g | [link](https://www.hobbyking.com/hobbyking/store/__27096__OrangeRx_Open_LRS_433MHz_9Ch_Receiver.html)
|Flytron 9ch RX | 3 | 1.2-100mW | - | 13 | no | - | 57x27x12mm 8.4g
|Hawkeye 9ch RX (blue) | 3 | 1.2-100mW | - | 13 | yes | - | XxXxXmm 9.6g |  [link](http://www.hobbiesfly.com/transmitter-receiver/hawkeye-9-channel-receiver.html)
|Hawkeye 9ch RX (black) | 3 | 1.2-100mW | 490MHz | 13 | yes | - | XxXxXmm 9.6g | [link](http://www.hobbiesfly.com/transmitter-receiver/hawkeye-9-channel-long-range-receiver.html)
|Hawkeye/DTFUHF 6(/4)ch | 5 | 1.2-100mW | 490MHz | 8 | yes | - | 55x20x8mm 7.0g | [link](http://www.hobbiesfly.com/transmitter-receiver/dtf-uhf-6-channel-long-range-receiver.html)
|Hawkeye/DTFUHF miniRX | 5 | 1.2-100mW | 490MHz | 8 | yes | yes | 57x25x8mm 9.7g | [link](http://www.hobbiesfly.com/transmitter-receiver/dtf-uhf-minirx-long-range-receiver.html)
|Hawkeye/DTFUHF 1W RX | 5 | ~800mW | 490MHz | 8 | yes | yes | 57x28x8mm 15g | [link](http://www.hobbiesfly.com/transmitter-receiver/dtf-uhf-1watt-long-range-receiver.html)
|Brotronics PowerTowerRX | 7 | 100mW | 490MHz | tbd | yes | yes | tbd | [link](http://www.multirotorsuperstore.com/radio/radio-receivers/brotronics-powertowerrx-for-openlrsng.html)
|OpenLRSng MicroRX | 8 | 100mW | 490MHz | 5 | yes | - | 22x22x8mm 5g
|Brotronics BroversityRX | 9 | 100mW | 490MHz | tbd | yes | yes | tbd | [link](http://www.hobbiesfly.com/transmitter-receiver/brotronics-openlrsng-broversityrx.html)
|Brotronics 4ch remix | 5 | 100mW | 490MHz | tbd | yes | - | 31x17x8 5g | [link](http://www.hobbiesfly.com/transmitter-receiver/brotronics-4ch-remix-long-range-receiver.html)
|OrangeRX/Flytron TX 100mW/1W| 2 | 1-100mW / 400mW | - | 7 | ? | - | tbd. | [link](https://www.hobbyking.com/hobbyking/store/__40031__OrangeRX_Open_LRS_433MHz_Transmitter_1W_compatible_with_Futaba_radio_.html)

#### Hardware Notes

##### DTF UHF 4-channel
![4ch](https://raw.githubusercontent.com/openLRSng/openLRSngWiki/master/images/4ch.png)

Version 2 and newer RXs also have the RSSI filter onboard, to filter High-Frequency RSSI into 0-3.3V RSSI. Enable the filter by soldering these two pads together:

![solder jumper](https://raw.githubusercontent.com/openLRSng/openLRSngWiki/master/images/jumper.png)

##### Hawkeye / Hobbyking / Flytron 9-channel
![Hawkeye RX](https://raw.githubusercontent.com/openLRSng/openLRSngWiki/master/images/Hawkeye9ch.png)

![HK rx](https://raw.githubusercontent.com/openLRSng/openLRSngWiki/master/images/hk.png)

Note on Hawkeye 6ch/9ch ICSP pins
---------------------------------
Hawkeye 6ch/9ch receivers have non-standard ICSP pinout.

![Hawkeye ICSP](https://raw.githubusercontent.com/openLRSng/openLRSngWiki/master/images/hawkeye-6ch-9ch-isp.jpg)
