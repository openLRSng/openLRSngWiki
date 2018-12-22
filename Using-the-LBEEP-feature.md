## Description
LBEEP allows implementing link quality 'beeper' with no extra hardware by utilizing the audio channel of the FPV video link.  
Note that there are 2 output options on your module
* packet loss beeper / LBEEP: gives you a beep on packet loss as an early warning
* link loss indicator: lets you know when your link has been entirely lost

## Connection alternative 1 - no other audio
In this mode the audio is silent and beeps will be emitted when packets are lost.

Circuit:

![](https://raw.githubusercontent.com/openLRSng/openLRSngWiki/master/images/LBEEP%20circuit.jpg)

## connection alternative 2 - mixing to existing audio
The lbeep output can be connected using pair of diodes to allow normal audio to pass thru unaffected while the beep will 'take over' when needed.
(if you wonder, the circuit blocks DC current from crossing, and remove 0.7V from voltage crossing the diodes, preventing line level (1V) sound from leaking much into the openlrsng module, while the openlrsng module can send a higher voltage and have that flow to the line level audio connection)

Circuit:

![](https://raw.githubusercontent.com/openLRSng/openLRSngWiki/master/images/lbeep_mixer.png)