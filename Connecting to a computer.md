Always attach an antenna
========================
Never power on any receiver or transmitter for any reason without a suitable antenna attached. This includes
when you are connecting it to a computer for software updates. All receivers are also capable of transmitting.

Connecting a device with on-board USB (DeluxeTX)
------------------------------------------------
Simply plug in the USB port to your computer and ensure the correct drivers have been installed. :)

Connecting a device that requires a USB-Serial adapter
------------------------------------------------------
**5 volt warning:** The radio modules on all 100mW models are not 5 volt tolerant. If you connect 5 volt power to the programming headers, you may damage the radio module. Only connect a programming cable that provides 3.3 volt power. Fortunately, the other components on the receivers and transmitters are tolerant of 5 volts, and the radio module is replaceable if you damage it.

**Also:** some USB-serial adapters are actually 5 volt when they claim to be 3.3 volt. Sneaky, eh? Verify that the power connection (Vcc) is actually 3.3 volts and not 5 volts _with a voltmeter_ if you are not absolutely sure. 

Connect your USB-Serial adapter to the computer and ensure the drivers have installed. Driver installation for USB-serial adapters is outside the scope of this manual but links to drivers for the most popular adapters are at the bottom of this document.

The following connections must be made between the device and USB-Serial adapter:
* Ground
* TX
* RX

If you are flashing the device, an additional pin is required: (optional if simply changing settings)
* DTR

The device will also require a power connection. Transmitters may be powered by the radio as normal, and receiver may be powered by a BEC on the servo pins as normal. If your USB-serial adapter provides 3.3 volts, you may connect that to the power pin on the programming header instead. (Note that Hawkeye transmitters must be powered by the radio)

Drivers
-------

**_DeluxeTX:_** This device requires drivers for Arduino Leonardo. The simplest way to install these drivers on Windows is to install the latest version of Arduino which is found [here](http://arduino.cc/en/Main/Software#toc3). Download and install the release appropriate for your platform. At the time of writing, version 1.5.5 Beta is the latest release.

**_CP2102:_** [Manufacturer's driver download page](http://www.silabs.com/products/mcu/pages/usbtouartbridgevcpdrivers.aspx)

_**FTDI:**_ [Manufacturer's driver download page](http://www.ftdichip.com/Drivers/VCP.htm)

### Note: JR and Futaba modules (Non-Deluxe)

These transmitters need to be powered by your radio, as the power supplies on board don't like being powered with your USB-Serial adapter. These modules should be plugged into your radio and the radio switched on in order to program them. For OrangeRX modules it's common to cut a hole in the outer plate exposing the programming pins, so you don't have to unscrew the plate every time.
