An overview of openLRSng functions that do not require being connected to a computer.

Binding
-------
Hold down the bind button while connecting power to the transmitter. Once the transmitter beeps once, release
the bind button. The transmitter will begin to beep 5 times per second and the red LED will flash. The transmitter is now in bind mode, using the stored bind information.

Connect your receiver to power. After a moment, both the red and green LEDs should stay lit constantly and
the transmitter will stop beeping. The receiver is now bound and all binding and transmitter information has been sent to the receiver. To bind additional receivers without restarting the transmitter, press the bind button momentarily and the transmitter will begin to beep again.

There are three bind modes:
<dl>
<dt>Release button after 1st beep ( hold for &lt; 5 seconds )</dt>
<dd>Regular bind mode.</dd>

<dt>Release button while beeping rapidly ( hold for 5 - 10 seconds )</dt>
<dd>Randomize the TX unique code and hop channels. This makes your TX unique but keeps settings related to telemetry etc.</dd>

<dt>Release button while TX is emitting solid tone ( hold for 10+ seconds )</dt>
<dd>Switches the active profile. There are four profile slots and the active profile is indicated by the short beeps on startup.</dd>
</dl>

Randomizing
-----------
Hold down the bind button while connecting power to the transmitter. Continue holding down the bind button
for about 5 seconds until the transmitter begins to beep slowly, then release the bind button. The transmitter will begin to beep 5 times per second and the red LED will flash. The transmitter is now in bind mode, and has randomized the binding data, making your transmitter’s ID unique. Bind your receivers as normal. All receivers previously bound with this transmitter will have to be re-bound.

Setting failsafe
----------------
Failsafe information is stored in the eeprom of each receiver. If failsafe information has not been set, the
receiver’s behaviour is to keep outputting the last information it received. If the RX stops getting information from the TX for a set duration the failsafe servo positions are loaded.

To set failsafe controls to a specific position, turn on a bound transmitter and receiver pair, hold the controls in the failsafe position, and hold down the bind button until the transmitter beeps and the red LED flashes on both the receiver and transmitter. Failsafe information is now set. Always test failsafe operation BEFORE you need to rely on it.

OpenLRSng also supports per-channel failsafe settings (hold last value or set to a specific value) as well as stop-ppm and stop-pwm, that can be enabled after a specified delay i.e. in a staged failsafe setup. These are all set through the RX settings menu and are saved to the RX's memory.

Transmitter profiles
--------------------
The TX module has four separate 'slots' for settings which are completely isolated from each other and thus can have completely different setups. The profile can be swapped without any extra tools by keeping the 'bind' button down during TX startup more than ~10s. This can be used to have a profile with telemetry and another one without telemetry or to create a range testing mode with lower TX power.

LED information
---------------
<dl>
<dt>Transmitter</dt>
<dd>The green LED will flash constantly under normal operation. The red LED will illuminate to indicate a loss of signal from the controller, a lost packet from the receiver (if telemetry is enabled), a problem with the radio, or when failsafe information is set.</dd>
<dt>Receiver</dt>
<dd>The green LED will flash constantly under normal operation. The red LED will illuminate to indicate a loss of signal from the transmitter, a problem with the radio, or when failsafe information is set.</dd>
</dl>
