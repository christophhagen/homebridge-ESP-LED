# homebridge-ESP-HSV

This is a plugin for [homebridge](https://github.com/nfarina/homebridge) to control an LED strip connected to an ESP8266 chip. It allows adding the ESP8266 as a lightbulb to HomeKit and controlling it with Siri or the Home App on iOS.

## Requirements:

- An ESP8266 setup with my [URL/UDP API](https://github.com/christophhagen/ESP8266-LED)
- working wifi network for the ESP to receive commands
- server to run `homebridge` on
- iOS device with HomeKit

## Setup

1. Connect your LED strip to the ESP8266 and flash the device. Have a look [here](https://github.com/christophhagen/ESP8266-LED) for more information.

2. Check that the ESP connects to your Wifi.

3. Install `homebridge` on your server. A guide can be found on the [project homepage](https://github.com/nfarina/homebridge)

4. Download this repository and copy the files to a separate folder `homebridge-ESP-LED` in your `node_modules` directory. For me that's `/usr/lib/node_modules`

5. Run `npm install` in the `node_modules` directory to download the dependencies.

6. Add your configuration to the `config.json`. An example is included as `config-sample.json`. Make sure that the `id` and `ip` of the device you want to control matches your ESP8266-LED configuration.

7. Optionally: Configure homebridge to [run on system startup](https://github.com/nfarina/homebridge/wiki/Homebridge-autostart-at-boot-(init.d%29-on-Ubuntu-(linux%29) for convenience

7. Set up the HomeKit device on your iOS device. It should be automatically discovered if you are on the same network.

8. Control your light with Siri or the Home app.
