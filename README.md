# blink-32 📺
a small ESP32-S3 and TFT-SPI display project to play whatever you're watching but on a cuter screen. 
the casing is a tiny pocket-sized retro TV (3D Printed) designed to recreate the look and feel of portable media players of the past. 
connects directly to your laptop/PC through USB-C.

there is **no** audio output. the device is intentionally focused on the visual experience and not being sensory overload for me. the same reason it has adjustable luminosity btw. i'd like to say i started this to combine several areas of special interest (embedded systems, electronics, old graphics and any retro tech really, so on) but i also mostly enjoy having a tiny fake tv on my desk that looks like the screens i played games on as a child. how convoluted the path of nostalgia can get.

## progress 🎯
- [x] get the esp32-s3 going
- [x] connect and control ILI9341 display
- [x] test physical button functionality
- [ ] add some pics
- [x] finish final code from arduino IDE
- [ ] upload final code from arduino IDE
- [ ] implement youtube integration
- [ ] maybe a crt-style rendering to experiment. and for my inner kid
- [ ] print final enclosure and upload the file for it
- [ ] add brightness control
- [ ] optimize power consumption

## hardware 🧰
component | why
--- | --- 
ESP32-S3 N16R8 | main microcontroller
ILI9341 2.8" TFT-SPI LCD | screen
3 pushbuttons | user controls
220Ω resistor | LED current limiting
5mm LED | ON status indicator
breadboard and jumpers | prototype assembly
USB cable | programming and power
n-channel MOSFET | electronic switching and PWM control of display/backlight. adjustable luminosity
slide switch | ON/OFF

i soldered everything with flux core wire

## the deets
**controls:**
for extremely serious engineering purposes, the three buttons are referred to in code as BUTT 1, BUTT 2, and BUTT 3 respectively.
one is for increasing luminosity. one for decreasing. one for good measure, to extend in the future with other ideas i have in mind.

## prototype rambling 🔌
testing included:
- ESP32-S3 firmware uploads
- GPIO testing for each one
- button input testing
- LED output testing
- SPI display communication
- ILI9341 graphics rendering
- performance testing

during testing, the display loop reached approx. 160–170 FPS, providing plenty of headroom for the intended visual effects.

## software 💻
the firmware is being developed using the Arduino ecosystem.
current/planned dependencies include: 
- Adafruit GFX
- Adafruit ILI9341
- ESP32 Arduino core

additional libraries may be introduced for:
- HTTP requests
- JSON parsing
- YouTube/API communication
- image downloading
- image decoding
- CRT rendering effects
