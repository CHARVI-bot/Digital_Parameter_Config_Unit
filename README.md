# Arduino UNO R4 \- SSD1306 OLED Project

## Project overview
Simple Arduino project that initializes a 128x64 SSD1306 OLED over I2C and displays text. Source is in `src/main.cpp`.

## IDE
- IDE: `CLion`
- Version: `CLion 2025.3.2`
- Platform: Windows

## Code
- Main source: `src/main.cpp`
- Behavior: Initializes I2C OLED (address `0x3C`), clears the display, sets text size/color, and prints three lines of text.

## Libraries
Install via Arduino Library Manager:
- `Adafruit_SSD1306`
- `Adafruit_GFX`
- `Wire` (part of Arduino core)
- `Arduino.h` (Arduino core)

## Dependencies
- Arduino board package that supports Arduino UNO R4 (install via Boards Manager)
- Arduino core headers and build toolchain (for CLion integration use Arduino CLI or a CMake toolchain that wraps Arduino)
- USB driver for the board (if required by Windows)

## Components and wiring (OLED)
- OLED module: 128x64 SSD1306 I2C (default address `0x3C`)
- Connections:
  - VCC \- connect to `3.3V` or `5V` depending on module specification
  - GND \- ground
  - SDA \- I2C data line
  - SCL \- I2C clock line
- Optional: pull\-up resistors (4.7k) if board/module does not include them
- Confirm correct I2C pins for your board variant before wiring

## Software requirements
- `CLion 2025.3.2`
- Arduino CLI or Arduino IDE (for board package installation and uploading)
- C++ toolchain compatible with Arduino board package (configured in CLion)
- Arduino Library Manager access (internet) to install required libraries

## Hardware requirements
- Arduino UNO R4 (or compatible board with SSD1306 I2C support)
- SSD1306 128x64 I2C OLED module (address `0x3C`)
- USB cable to connect board to PC
- Optional: breadboard and jumper wires

## How to build and upload (high level)
1. Install board package for UNO R4 and required libraries via Arduino Boards/Library Manager.
2. Configure CLion to use Arduino CLI or a CMake toolchain for Arduino.
3. Open project and build.
4. Upload using configured upload command (Arduino CLI / IDE).

## Author
- Author: `CHARVI-bot`
