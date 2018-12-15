OpenLRSng can output RSSI in a few different forms

* RSSI
  Pure signal strength, notably this will show zero during packetloss

* Qualilty
  Pure signal quality, basically success/fail ratio over 15 last packets. For example losing a single packet in air will result in a 6% drop for duration of 15 packets.

* Composite
  Composite signal is a mix of RSSI and Quality.
  If quality is maxed (100%) the composite signal is RSSI mapped to 50-100% range. If quality is not 100% the composite output is quality values mapped to 0-50% range.

When RSSI is injected into PWM/PPM/SUMD/SBUS etc. it is also possible to get RSSI and Quality as separate channels, this is the best option if your OSD supports that.

If you can only show one value it is recommended to use the Composite (default) mode as that will give both RSSI and quality information as singe value.

It is recommended to familiarize oneself to the RSSI behavior by testing behavior with dummy load etc. 
