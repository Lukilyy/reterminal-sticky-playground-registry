# Bus ETA

Bus ETA turns reTerminal Sticky into a live bus arrival display. It supports Singapore and Hong Kong bus data, on-device station setup, WiFi setup, and automatic low-power sleep.

## Setup

After flashing, open the WiFi page to connect the device to a network. In Setup, select the city/provider and enter a station name or station ID. A station refresh interval is optional and can be saved independently. The Bus page shows the station name, local time and available arrivals.

The firmware uses WiFi to retrieve public bus arrival data and NTP time. It writes synchronized time to the onboard RTC when available. After one hour without a hardware button press, it displays a simple sleep screen and enters low-power sleep. Press the refresh/AI button to wake and refresh the Bus page.

## Firmware package

- Version: `1.0.0`
- Source project: [Clair2929/reterminal-sticky-bus-eta](https://github.com/Clair2929/reterminal-sticky-bus-eta)
- Build toolchain: ESP-IDF v5.4, target ESP32-S3
- Package: the bootloader, partition table and application image are listed with their flash offsets and SHA-256 hashes in `firmware/1.0.0/manifest.json`.

## Hardware test

Tested on a reTerminal Sticky with ESP32-S3. The device booted, connected to WiFi, synchronized NTP time, read the RTC and battery gauge, and displayed live bus arrivals. The preview photo shows the firmware running on the device.
