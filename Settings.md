How to get into the transmitter settings menu
---------------------------------------------

1. Start the Google Chrome configurator. [(download it here)](http://goo.gl/iX7dJx)

2. Connect your transmitter to the computer as shown in the ["Connecting to a computer guide"](Connecting-to-a-computer).

3. The configurator should auto-connect to the transmitter and open the settings page.

How to get into the receiver settings menu
------------------------------------------

Note that RX settings are done wirelessly. Your receiver does not need to be connected to the computer to adjust settings. No PWM or PPM will be output by the RX while in configuration mode.

1. Connect to the transmitter as above and ensure you are in the transmitter settings tab.

2. Click on the RX settings tab. Apply power to the RX during the timeout period. This can be done by applying power as normal to the airplane or helicopter.

3. The configurator should auto-connect to the receiver and open the settings page.

Transmitter settings
--------------------
These settings are set on the transmitter and sent to the receiver during bind. You must rebind after changing any of these settings.
<dl>
<dt>RFM Type</dt>
<dd>Select the frequency of the RF module on your device. Most units are 433.</dd>
<dt>Operating frequency</dt>
<dd>The lowest frequency of the frequency range you are transmitting.</dd>
<dt>RF Power</dt>
<dd>The output power setting of the transmitter. 0 is the lowest and 7 is the highest. The receiver will use the same power setting if telemetry is enabled. 1W hardware should not be set to a value lower than 5. Power output does not change linearly with this setting.</dd>
<dt>Channel spacing</dt>
<dd>The amount of frequency between each channel.</dd>
<dt>Serial baudrate</dt>
<dd>The connection speed of the serial link if you are using the transparent serial link. This is only the connection speed, which will depend on the devices that you are connecting to. The rate that data can be sent will probably be much lower.</dd>
<dt>Data rate</dt>
<dd>The rate that data is sent between the transmitter and receiver. Lower numbers mean slightly improved range at the cost of servo refresh rate.</dd>
<dt>Enable telemetry</dt>
<dd>Enable the telemetry link from the receiver. The transmitter will beep if the receiver experiences packet loss. Also, the transparent serial bridge will be available. The FrSky option will enable FrSky telemetry output on the transmitter for connection to OpenTX or FLD-02.</dd>

<dt>Bind code</dt>
<dd>The randomly-generated ID of your transmitter. If this reads DEADFEED, you need to randomize the information on your transmitter. Valid characters are hexadecimal (0-9, A-F)</dd>
<dt>RC output configuration (channels)</dt>
<dd>Select the number of channels that will be sent to the receiver. This is also the number of channels that will appear on the receiver’s PPM output. Additional channels sent to the transmitter will be ignored. Example: if the transmitter is set to 8 channels, and you controller is set to 12 channels, only the first 8 channels will be sent to the receiver. The “Switch” channels are channels with very low resolution - only 4 positions; however they take 1/5th of the time to transmit, increasing the number of useful channels for a certain refresh rate.</dd>
<dt>Number of hop channels</dt>
<dd>This will allow you to set the number of hopping channels.</dd>
<dt>Maximum desired frequency</dt>
<dd>Set the maximum frequency you want to transmit on. All the hopping channels will be placed below this frequency.</dd>
</dl>

Receiver Settings
-----------------
These settings are set on each individual RX and stored in the RX's memory. The RX will keep these settings until they are changed or erased during a software update.

PPM output is available on one pin. It can be enabled by setting the correct port to output PPM. High-frequency RSSI / LBEEP is also available on one pin and is enabled the same way. See the [Hardware Guide](Hardware-Guide) to find the correct port for your receiver.

<dl>
<dt>Minimum PPM sync time</dt>
<dd>The minimum time between PPM frames on the PPM output. The default value works fine for many systems but fickle systems such as Ardupilot require a longer sync time.</dd>
<dt>Inject RSSI on servo channel</dt>
<dd>The RSSI signal is turned into an output that can drive a servo and injected into the PPM stream, replacing the RC channel of your choice. This channel can then be mapped to an output port.</dd>
<dt>Always bind on startup</dt>
<dd>By default, the receiver always listens for a bind message for a moment when power is applied. If this feature is disabled, you must jumper ports 1 and 2 to force the RX into bind mode on startup.</dd>
<dt>Limit PPM out to 8 channels</dt>
<dd>Some devices that accept PPM are also picky about the number of PPM channels that are in a PPM frame. This option is used to only output the first 8 channels in the PPM stream regardless of the number of channels sent to the receiver.<dd>
<dt>Enable slave mode</dt>
<dd>This option is for a future multi-RX diversity mode. Don't use it for now.</dd>
<dt>Failsafe delay</dt>
<dd>The amount of time after the last packet is received before the receiver will load failsafe values. This can be used to “fly through failsafes” and can be adjusted to your liking. This value is in 1/10ths of a second.</dd>
<dt>Stop PWM on failsafe</dt>
<dd>Completely disable PWM outputs on failsafe.</dd>
<dt>Stop PPM on failsafe</dt>
<dd>Completely disable PPM outputs on failsafe.</dd>
<dt>Beacon frequency</dt>
<dd>If this option is enabled a tone is transmitted on the selected frequency that can be picked up using a common FRS, PMR or amateur radio walkie-talkie to aid finding a lost airplane or helicopter. Five tones are sent of descending transmit power to help you zero in on its location. The beacon is sent after failsafe has been activated.</dd>
<dt>Beacon interval</dt>
<dd>The amount of time the beacon will idle between transmit sequences.</dd>
<dt>Beacon deadtime</dt>
<dd>The amount of time after failsafe has been enabled before the beacon starts.</dd>
<dt>Channel Output</dt>
<dd>Set the outputs for each port in this menu.</dd>
</dl>

RSSI modes
----------
There are four different RSSI modes available in openLRSng. That's a lot!
### High-frequency RSSI pulse
An 8kHz PWM signal is available on one pin. It is varied between 0-100% duty cycle to indicate RSSI.
### Analogue RSSI 0-3.3 volts
The high-frequency signal above can be filtered to produce an analogue signal. On DTF UHF 4-channel receivers V2 and newer, the filter is on-board and can be enabled by soldering a jumper as seen in the Hardware Guide. An external filter can be made with a capacitor and resistor.

![Analogue RSSI filter circuit](https://raw.githubusercontent.com/openLRSng/openLRSngWiki/master/images/AnalogueRSSIfilter.jpg)
### LBEEP Audio Beep mode
This will output a beep on a lost radio packet that continues until a valid packet is received. This output can be connected directly to the audio input of a video transmitter. Thus, instant audio feedback of the radio link quality is enabled.
[Using LBEEP (link loss beep over FPV audio)](wiki/Using-the-LBEEP-feature)
### RSSI Injection
A RC servo channel can be replaced with RSSI information, and set to an output port to drive a servo or OSD with 50Hz servo-pwm. Note that this injection will replace that servo channel, or you can map this to an additional RC channel when in 8- or 12-channel mode, so RSSI will be on channel 9 or 13 and not overwrite a PPM channel you are using.
