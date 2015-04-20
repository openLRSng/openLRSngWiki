As all openLRS receivers are capable of transmission they can be used as 100mW transmitters.

### Connections
9ch modules (Hawkeye/Flytron/OrangeRX)

    output1(rssi) - passive buzzer (~speaker, multi freq support)
    output2(ch1)  - unused
    output3(ch2)  - active buzzer (single freq)
    output4(ch3)  - bind button (between signal and ground)
    output5(ch4)  - PPM input
    output6(ch5)  - RED led (between signal and ground, duplicates onboard LED)
    output7(ch6)  - GREEN led (between signal and ground, duplicates onboard LED)
    output8(ch7)  - unused
    output9(ch8) - unused

4/6ch modules (DTF-UHF)

    output1 - PPM input
    output2 - bind button (between signal and ground)
    output3 - passive buzzer (~speaker, multi freq support)
    output4 - active buzzer (single freq)
    output5 - RED led (between signal and ground, duplicates onboard LED)
    output6 - GREEN led (between signal and ground, duplicates onboard LED)

## Power considerations
As the receivers have fairly small voltage regulator it is not recommended to power them with more than 6V or so. Use a BEC to preregulate voltage to 5/6V before feeding to RX module (via servo connectors)

## Bind button
A normal single contact non locking push button should be used, as pullup is provided internally the button goes between GND and signal pin.

## Connecting buzzers
As the outputs have resistors on them it is necessary to have a transistor driver to be able to drive buzzer/speaker.

## external LEDs
LED outputs are duplicated on IO pins to allow easily mount LEDs in visible location. There is 1kOhm resistors thus very limited current is provided so LEDs should be high efficiency ones (ultrabright).
