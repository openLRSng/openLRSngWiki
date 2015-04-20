#### NOTE: this feature is experimental and should be used with care

##### 1. Setting up modules the modules
<ul>
 <li> Install custom beta firmware from http://openlrsng.org/beta/ (grab the latest)</li>
 <li> Use RX configurator to enable SCL and SDA outputs (from pinconfig)</li>
 <li> Enable the "slave mode" flag on one of the two receivers (the one going to be the slave)</li>
</ul>

##### 2. Connecting master and slave
<ul>
 <li> Use a 4 pin cable to connect the master and slave receivers</li>
</ul>
 

```
 SDA-SDA
 SCL-SCL
 GND-GND
 VCC-VCC or 5V-5V
```
##### 3. Bind and configure the system normally. Notably the outputs on the slave are not currently usable.

NOTE: to remove the 'slave mode' flag you need to have the 'force bind' jumpper on the RX to allow it to bind. 
