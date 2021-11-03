# VAware-System-Logic
## About the Board
We used an off the shelf ESP32 Microcontroller that had the following capabilities:
- Bluetooth Low Energy
- Wifi
- Arduino IDE support
- Micropython support

## Using the Board
- Download the Arduino IDE
- Go to Preferences and enter the following link in 'Additional Boards Manager URLs:'
    - https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json
- Then under 'Tools' set the following.
    - 'Board' -> 'Boards Manager...'
        - Type in ESP32 in the search bar and download the latest Version from ESPRIFF SYSTEMS.
    - When you hover over 'Board' you should now see ESP32 Options.
        - Select the 'ESP32 Dev Module' option.
- You are now ready to flash the code on to the board!

## About the Code
- The Code was written in .ino in the Arduino IDE.
- It utilizes several Bluetooth libraries that work as one cohesive unit.
- During the initialization stages of the code the Arduino creates a BLE GATT Server that advertises itself as 'VAware'
- Once the connection between the client (instructor handheld device) and server (Arduino) is established, the server awaits commands.
- This is a high level over view of how the code functions feel free to look at the code (its commented) :)

## Challenges
- The Pins on the ESP32 do not behave the same way in several aspects.
    - A lot of trial and error had to be done inorder to ensure proper function.
    - The most significant was different performance of pins based on power delivery
        - When powered by USB port
        - When powered through 5V in VCC
- Behaviour of switches and learning which methods of input output would best work for our use case took a lot of trial and error.
- Learning BLE and GATT principals took a lot of time.
- Also make sure that you have a Data transfer Micro-USB cable instead of a Power only USB cable.



