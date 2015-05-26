# ESP8266
The [ESP8266](https://github.com/mattwind/ESP8266/blob/master/docs/ESP8266_Specifications_English.pdf) WiFi Module is a self contained SOC with integrated TCP/IP protocol stack that can give any microcontroller access to your WiFi network.

<img src="https://github.com/mattwind/ESP8266/blob/master/images/esp8266_pinout.png">

**Wiring**

I only use the TX/RX and a common ground on my FTDI chip. I supply a dedicated 3.3 volts to the ESP8266 module VCC and CH_PD pins. Connect GPIO0 to Ground when updating the ESP module.

**Updating the Firmware**

```
AT+GMR
00200.9.5(b1)
compiled @ Dec 25 2014 21:40:28
AI-THINKER Dec 25 2014
````

Unzip the the content of the ZIP file https://github.com/mattwind/ESP8266/archive/master.zip

Close Putty and/or any other application that is using the COM port to access the ESP8266.

1. Power down the ESP8266 module.
2. Connect GPIO0 to GND.
3. Power on the ESP8266 module.
4. Run esp8266_flasher.exe as an administrator (right-click, then Run as administrator...)
5. Click on the button labeled as Bin to select the BIN file, select AI-v0.9.5.0_AT_Firmware.bin
6. Enter the COM port your ESP8266 is connected to. In my case it was COM5.
7. Click Download, then wait.
8. Leaving, failed to leave flash mode. (This is okay!)
9. If it doesn't finish, click download again. I had to do it a few times.

Power down the ESP8266 module.
Disconnect GPIO0 from GND
Power on the ESP8266 module.

***Other Resources***
* [ESP8266 Datasheet](https://github.com/mattwind/ESP8266/blob/master/docs/ESP8266_Specifications_English.pdf)
* [ESP8266 AT Command Reference](https://github.com/mattwind/ESP8266/wiki/AT-Command-Reference)
* http://www.esp8266.com
* http://www.electrodragon.com/w/ESP8266
* http://www.xess.com/blog/esp8266-reflash
* https://github.com/esp8266/Arduino
* http://www.electrodragon.com/w/ESP8266_Firmware


