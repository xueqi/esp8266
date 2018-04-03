# Setup ESP8266 
## Requirement:
ESP8266 board with 1M flash. (Do not use 512k one for learning)
## NodeMCU Board
[NodeMCU](https://github.com/nodemcu/nodemcu-firmware) is a firmware for ESP8266 WiFiSOC. It uses Lua language for development.
Currently this project does not use lua because of personal preference. MicroPython(http://micropython.org) is used for development.
### Install MicroPython
[MicroPython for ESP8266 Tutorial](http://docs.micropython.org/en/v1.9.2/esp8266/esp8266/tutorial/index.html)

Official site said only [esptool](https://github.com/espressif/esptool/) is supported to flash the firmware. 
* Download micropython firmware from [github](http://micropython.org/download#esp8266), use the latest version. 
