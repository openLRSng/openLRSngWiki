## Description
LBEEP allows implementing link quality 'beeper' with no extra hardware by utilizing the audio channel of the FPV video link.

## Connection alternative 1 - no other audio
In this mode the audio is silent and beeps will be emitted when packets are lost.

Circuit:

![](https://raw.githubusercontent.com/openLRSng/openLRSngWiki/master/images/LBEEP%20circuit.jpg)

## connection alternative 2 - mixing to existing audio
The lbeep output can be connected using pair of diodes to allow normal audio to pass thru unaffected while the beep will 'take over' when needed.

Circuit:

![](https://raw.githubusercontent.com/openLRSng/openLRSngWiki/master/images/lbeep_mixer.png)
