# homebridge-ESP-HSV

This is a plugin for [homebridge](https://github.com/nfarina/homebridge) to control an LED strip connected to an ESP8266 chip. It allows adding the ESP8266 as a lightbulb to HomeKit and controlling it with Siri or the Home App on iOS.

## Requirements:

- [ESP8266](http://espressif.com/products/hardware/esp8266ex/overview/) chip (I'm using the ESP-12F, you can order them very cheap e.g. from eBay)
- programmable RGB-LED strip (e.g. WS2812B, also available cheap on eBay)
- working wifi network (make sure to set SSID and password in `parameters.h`)
- server to run `homebridge` on
- iOS device with HomeKit

## Setup

1. Connect your LED strip to the ESP8266. Have a look [here](https://github.com/christophhagen/ESP8266-LED) for more information.

2. Flash the ESP with the code from [here](https://github.com/christophhagen/ESP8266-LED) and check that it connects to your Wifi

3. Install homebridge on your server. A guide can be found on the [project homepage](https://github.com/nfarina/homebridge)

4. Download this repository and copy the files to your `node_modules` directory. For me that's `/usr/lib/node_modules`

5. Add your configuration to the `config.json`. An example is included as `config-sample.json`.

6. Configure homebridge to [run on system startup](https://github.com/nfarina/homebridge/wiki/Homebridge-autostart-at-boot-(init.d)-on-Ubuntu-(linux)) for convenience

7. Set up the HomeKit device on your iOS device. It should be automatically discovered if you are on the same network.

8. Control your light with Siri or the Home app.

