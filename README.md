# TinyBasicPlus for ATmega644xx (MightyCore Port)

TinyBasicPlus is a lightweight BASIC interpreter tailored for microcontroller applications. This repository provides a dedicated port of TinyBasicPlus for the ATmega644xx series, leveraging the capabilities of the MightyCore platform. This project is aimed at hobbyists and developers seeking to integrate an interactive BASIC environment on their ATmega-based systems.

## Version

Current Release: **0.15.1**

This version introduces some OEM commands and functions that enhance usability and provide extended capabilities for user programs.
This sketch is pre-configured with:
- SD/MMC Card support (CS = 4)
- EEPROM support (ROM size auto detecting)
- TWI/I2C support (Included Wire.h)

## Key Features

Designed specifically for **ATmega644xx series** using **MightyCore Bootloader**.

Compact and efficient, ideal for low-resource environments.

Supports interactive BASIC programming with essential control and arithmetic functionality.

Expanded with custom commands tailored for versatile hardware operations.

## What's New in 0.15.1

This release introduces the following new commands and functions:

## Commands

Screen Utils:
- CLS: Clear the terminal screen for better readability.

TWI/I2C utils:
- BTWC: Begin TWI transmission with decimal address from 0 to 127.
Usage: BTWC <addr>

- TWW: Write data into TWI bus.
Usage: TWW <data>

- ETWC: End the TWI transmission and get status code.
No arguments, prints nothing on success

- RTWD: Request total count of bytes from TWI bus.
Usage: RTWD <addr> <count>

Functions:
- TWR(): Read value from TWI bus.
BUG: Doesn't work if you dont add a unneccesary value into the function!

## Installation

Prerequisites:
- Arduino IDE (Version 1.8 or later recommended).
- Install MightyCore in your Arduino IDE.
- An ATmega644xx microcontroller.

Steps:

1. Clone or download the repository.
git clone https://github.com/Saveriokarol/tinybasicplus-m644-port.git

2. Open the .ino file in the Arduino IDE.
Configure the board settings for MightyCore (Ext. 16MHz, 5V).

3. Upload the program to your ATmega644xx microcontroller.

## Usage

Once installed, connect to the microcontroller using a serial terminal (e.g., Arduino Serial Monitor or PuTTY). The interpreter is ready to execute BASIC commands interactively. Try the new commands and explore hardware interaction with ease.

## Contributing

Contributions to improve this port or add new functionality are welcome! Please submit an issue or pull request to collaborate.

## License

This project is open-source and available under the MIT License. See the [LICENSE](./LICENSE) file for details.

## Acknowledgments

Special thanks to:
[MightyCore](https://github.com/MCUdude/MightyCore) for providing robust ATmega support.
The original creators of [TinyBasicPlus](https://github.com/BleuLlama/TinyBasicPlus) for their inspiring work.

