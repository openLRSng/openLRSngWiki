1. Connect your device to the computer as shown in the ["Connecting to a computer guide"](Connecting-to-a-computer). Find the COM-port associated with the device.

2. Open cTn's configurator for Google Chrome [(download it here)](http://goo.gl/iX7dJx) and select the COM-port from the menu. If you plugged in your USB-serial adapter after starting the configurator, click refresh to update the list of detected COM-ports, or click Disconnect if the configurator has auto-connected. Don’t click on Connect. Click on Start Firmware Flasher.

3. Select the hardware you are flashing. Note that some receivers can also be flashed with transmitter firmware, allowing them to be used as transmitters with some additional components.

4. Select whether or not to erase eeprom. It is always recommended to leave this enabled unless you know what
you’re doing.

5. Click the Flash Firmware button. If the flashing was unsuccessful, check to make sure the correct COM-port is selected, the pins have been connected properly (you may have to swap TX and RX, depending on your USB-serial adapter), the LEDs on the receiver are off for the duration of the flashing (indicating that the device is indeed being flashed), and that the device being flashed is being powered properly. Some 1-watt transmitters draw more power than a USB port can give; in this case the transmitter must be powered by a battery while flashing.

## Hardware specific notes
### Hawkeye 1W JR/Futaba modules
Easiest method to flash these units is to use 3v3 CP2102/FTDI adapter connected to the (1x6) serial header with following procedure.

1. Plug the module into the radio and connect the serial to it but have it off USB

2. Turn radio on

3. plug in USB to PC

4. unplug the module from the Radio

5. Flash using the configurator

Same procedure can be used when connecing it for configuration.
For convinience cut a hole on the backside of the module box so that the serial header can be accessed without opening the module.