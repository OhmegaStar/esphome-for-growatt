# ESPhome for Growatt by ohmegastar (still under development)
ESPhome configuration for monitoring and control of Growatt inverters in Home Assistant.
This include all addresses i could see relevant from the inverter, and then some.

forked from https://github.com/klatremis/esphome-for-growatt

* For DIY generic esp32 hardware, I use ESP32-S3-WROOM N16R8 Board with a TTL to RS485 Board with Auto Flow Control and the wiring below

## Supported devices
### SPH inverters
* SPH10000TL3-BH-UP (confirmed), use the growatt-sph-10k-tl3-bh-up.yaml
* SPH3600 (assumed) (was supported in the original klatremis code)

### MIC inverters
* (not confirmed)

### MOD inverters
* MOD10000TL3-X (confirmed), use the growatt-mod-10k-tl3-x.yaml

### MID inverters
* (not confirmed)

### MAX inverters
* (not confirmed)

## Requirements
* ESP32-S3-WROOM N16R8
* TTL To RS485 Module with automatic flow control

## Installation
1. Create your esp32 in esphome in home assistant
2. Upload the your basis config via. usb from pc.
3. Test wireless upload
4. Copy all content (make sure you have your wifi ssid&password, esphome ota and api keys in the secrets)
5. Edit the sensors in the config if you like
6. Upload wireless

## Wiring of generic esp32 & TTL module
RX / TX between esp and ttl converter may have to be swapped. This seems to be a little different from espboard to espboard.
If it dosent communicate(RX/TX led both blinking) Try swap rx/tx on the esp.
 ![image](https://github.com/klatremis/esphome-for-bms/blob/main/wiring.jpg)
