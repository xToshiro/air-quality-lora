
# ESP32 LoRa Web Chat

This project provides a robust C++ code for the Heltec ESP32 LoRa V3 (433-510 MHz) with OLED Display. 
The goal is to create a bidirectional communication system between two ESP32 LoRa devices through a local web server. 
This project enables the ESP32 to host a Wi-Fi network, allowing a mobile device to connect and send/receive messages.

## Project Overview

- **Device**: Heltec ESP32 LoRa V3 (433-510 MHz)
- **Frequency**: 450.5 MHz (adjustable)
- **Communication**: LoRa + Local Wi-Fi network
- **Web Interface**: 
  - A simple webpage hosted on ESP32 with two boxes: 
    - One for typing messages to send via LoRa
    - One displaying received messages
- **OLED Display**: Displays IP, Wi-Fi credentials, and message status (sent/received).

## How It Works

1. Two ESP32 LoRa devices run the same code.
2. Each device creates a Wi-Fi network (SSID and password are configurable).
3. A mobile device can connect to this network and access the web interface at the provided IP.
4. Messages can be sent via the webpage and transmitted over LoRa.
5. Received messages are displayed on the OLED and updated on the web interface.

## Hardware Requirements

- Heltec ESP32 LoRa V3 (with OLED and LoRa antenna)
- USB cable for programming
- Antenna for LoRa (to avoid hardware damage)

## Software Requirements

- Arduino IDE
- Heltec ESP32 board support (install via board manager)
- Radiolib library (for LoRa communication)

## Installation

1. Clone this repository.
2. Open the `.ino` file in Arduino IDE.
3. Select "Heltec ESP32" as the board.
4. Install required libraries: 
   ```
   Heltec ESP32 board package
   RadioLib
   WiFi
   WebServer
   ```
5. Upload the code to two Heltec ESP32 LoRa devices.
6. Monitor the Serial Output to check for IP addresses and successful initialization.

## How to Use

1. Power up both devices.
2. The OLED displays the Wi-Fi SSID and IP address.
3. Connect to the ESP32 Wi-Fi network using a mobile phone or laptop.
4. Open a web browser and enter the IP address (displayed on the OLED screen).
5. Use the web interface to send messages.
6. The received messages will appear in real-time on the same page.

## License

This project is licensed under the GNU GENERAL PUBLIC LICENSE Version 3, 29 June 2007.  
For more details, see [LICENSE](https://www.gnu.org/licenses/gpl-3.0.en.html).

## About

This project is part of the **Trama (Transport and Environment) Laboratory** at the **Federal University of Ceará (UFC)**.
