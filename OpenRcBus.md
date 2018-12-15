# OpenRcBus - work in progress

OpenRcBus is an open and expandable protocol to be used between Transmitter - radiomodule or recevier - flightcontroller.

It will interleave RC control and telemetry inside a single serial link.

## Physical layer

3v3 TTL level serial port at 1M bauds (tbd.)

Bidirectional link if needed, both directions use same frame types.

## High level frame format

    [HEADER]
    [DATA]
    [CRC16]

### Header

    [PREFIX]   single byte of value '0x??' tbd.
    [LENGTH]   length of data part in bytes [0..255], excludes HEADER and CRC16
    [DATATYPE] single byte identifying the format of the DATA

#### Datatype values
    0x01 12 bit RC channel data (2 channels per 3 bytes)
    0x02 Serial telemetry

### Data

#### Data (0x01)
RC data
    [FLAGS] - 0x01 -- set failsafe
    X * ( ch0bits_11_4 | ch0bits_3_0,ch1bits_11_8 | ch1bits_7_0  ) - Channel values (3 bytes per 2 channels)

    nominal 1..2ms channel is mapped to values 1024..3071

    when setting failsafe special values are used for special behavior
    0x000 - do not output channel in failsafe
    0x3ff - channel outputs last good value on failsafe

#### Serial telemetry (0x02)
Serial telemetry of one of following formats, first byte gives subtype.

    Subtype values:
    0x00 - passthru (transparent data)
    0x10 - frsky 'D' telemetry
    0x11 - frsky 'smaprtport' telemetry
    0x18 - HoTT
    0x20 - mavlink
    ...

### CRC16
CRC16 value over HEADER and DATA parts. Calculation details tbd.

## WIP
### mixer sync
Special frame to inform when new RC data is expected, sent out a fixed time interval e.g. 10ms? before new RC data is needed.