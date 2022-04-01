# esp8266-homekit-light-ws2812
This is a native HomeKit light with D1 mini ESP8266 and ws2812 NeoPixel.

## Hardware
The following hardware is required:
```
- D1 mini (ESP8266)
- WS2812 module
```

Connection:
D1 mini -> ws2812
```
5V -> VCC
GND -> GND
D4 -> DIN
```
![alt text](https://github.com/datjan/esp8266-homekit-light-ws2812/blob/main/connection-schema.png?raw=true)

## Development
This sketch is for following development environment
```
Arduino
```

Following libraries are required
```
https://github.com/datjan/Arduino-HomeKit-ESP8266 (fork from Mixiaoxiao/Arduino-HomeKit-ESP8266:master)
https://github.com/adafruit/Adafruit_NeoPixel
```

## Setup
Setup esp8266-homekit-light-ws2812.ino:
```
#define NUMPIXELS       8   // count leds in ws2812
```

Setup my_accessory.c:
```
.password = "555-11-123"  // Homekit Code
```

Setup wifi_info.h
```
const char *ssid = "xxx"; // SETUP Wlan ssid
const char *password = "xxx"; // SETUP Wlan password
```

## Upload to device
Following files needs to be uploaded to the ESP8266 (D1 mini)
```
esp8266-homekit-light-ws2812.ino
my_accessory.c
wifi_info.h
```

## Add device to Homekit
The device can be added to homekit like every other homekit device.
