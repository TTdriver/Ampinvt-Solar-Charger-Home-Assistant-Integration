# Ampinvt-Solar-Charger-to-Home-Assistant

This project explains how to connect an **Ampinvt solar charge controller** to Home Assistant using an ESP32, ESPHome, and an RS485-to-TTL converter.

This setup has been tested with the following models:

* Ampinvt 60A solar charge controller
* Ampinvt 80A solar charge controller

## Setup Overview

The first step is configuring the ESP32 with ESPHome and adding the device to Home Assistant.

A working ESPHome YAML configuration file is included in this repository.

The second step is wiring the ESP32 to the RS485-to-TTL converter and connecting it to the solar charge controller using an Ethernet cable.

Lastly, a required ampinvt.h file is included in this repository. This file needs placed in your ESP home directory. 

## Hardware Used

* ESP32 development board, such as an ESP32-WROOM-32
* RS485-to-TTL converter
* Jumper wires
* USB cable and power source for the ESP32
* Ethernet cable

## Wiring

### ESP32 to RS485-to-TTL Converter

| ESP32    | RS485 Converter |
| -------- | --------------- |
| GPIO17   | TXD             |
| GPIO16   | RXD             |
| GND      | GND             |
| VIN / 5V | VCC             |

### RS485 Converter to Ethernet Cable

| RS485 Converter | Ethernet Cable Wire |
| --------------- | ------------------- |
| A+              | White/orange stripe |
| B-              | Orange              |
| GND             | Brown               |

> [!IMPORTANT]
> Ethernet cable wire colors can vary depending on how the cable was terminated. Verify the pinout and wire continuity before connecting it to the charge controller. This is based on T-568B.

## ESPHome Configuration

The working ESPHome YAML file is included in this repository.

Upload the YAML configuration to the ESP32 using ESPHome, then add the ESPHome device to Home Assistant.

## Installation Steps

1. Install ESPHome in Home Assistant.
2. Create a new ESPHome device for the ESP32.
3. Copy the provided YAML configuration into the ESPHome device configuration.
4. Update the Wi-Fi credentials and device settings as needed.
5. Compile and install the configuration on the ESP32.
6. Add the ESPHome integration to Home Assistant.
7. Connect the ESP32 to the RS485-to-TTL converter.
8. Connect the RS485 converter to the Ethernet cable.
9. Plug the Ethernet cable into the Ampinvt solar charge controller.
10. Confirm that the charger sensors appear in Home Assistant.

## Credits

This Home Assistant forum post helped me get the project started:

[Ampinvt Solar Controller to Home Assistant via ESPHome](https://community.home-assistant.io/t/modbus-help-needed-ampinvt-solar-controller-to-home-assistant-via-esphome/493128)

## Disclaimer

This project involves connecting electronics to solar charging equipment.

Disconnect power before modifying wiring. Verify all voltages, pinouts, and connections before attaching the ESP32 or RS485 converter.

Proceed at your own risk. Incorrect wiring may damage the ESP32, converter, or solar charge controller.

## Photos
<img width="3000" height="4000" alt="20260728_221753" src="https://github.com/user-attachments/assets/e3978a28-2ceb-4b40-9111-a1aee185dfb4" />
<img width="3000" height="4000" alt="20260728_221802" src="https://github.com/user-attachments/assets/09d1a9a6-9403-4360-a1cd-6b106c524d10" />
<img width="3000" height="4000" alt="20260728_221745" src="https://github.com/user-attachments/assets/a8778234-63a0-4a7a-bafb-77ff0f7b1e5a" />


