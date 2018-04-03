# Setup ESP8266 
## Requirement:
ESP8266 board with 1M flash. (Do not use 512k one for learning)
## NodeMCU Board
NodeMCU board is a development board.

[NodeMCU](https://github.com/nodemcu/nodemcu-firmware) is a firmware for ESP8266 WiFi SOC. It uses Lua language for development.
Currently this project does not use lua because of personal preference. [MicroPython](http://micropython.org) is used for development.
### Install MicroPython
[MicroPython for ESP8266 Tutorial](http://docs.micropython.org/en/v1.9.2/esp8266/esp8266/tutorial/index.html)

Official site said only [esptool](https://github.com/espressif/esptool/) is supported to flash the firmware. 
* install [esptool](https://github.com/espressif/esptool/), or just:
for Python 2
** pip install esptool
for Python 3
** pip3 install esptool
* Download micropython firmware from [github](http://micropython.org/download#esp8266), use the latest version. 
* NodeMCU board comes with USB micro B connection, so there is no need to wireup the flash circuit.
* Connect NodeMCU board with USB cable, identify the port. (On windows should be COM?, linux: /dev/tty??)
** if device is not recognized, install the usb to serial driver. The driver depends what the board use. Check the rectangular chip on board. Reads as CH340G or Cp2102 or CH341
* erase old firmware
** esptool.py --port COM4 erase_flash
* flash the firmware
** esptool.py --port COM4 --baud 115200 write_flash --flash_size=detect 0 esp8266-20171101-v1.9.3.bin

