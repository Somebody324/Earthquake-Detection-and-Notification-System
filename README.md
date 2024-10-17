# Earthquake Detection and Notification System

## Overview
This project implements an earthquake detection and notification system using an ESP32 microcontroller, an ADXL335 accelerometer, and a DFPlayer Mini for audio alerts. The system continuously monitors seismic activity and sends notifications via Telegram in case of detected earthquakes. It also displays real-time acceleration data on an OLED screen.

## Features
- **Real-time Seismograph**: Displays acceleration data for the X, Y, and Z axes on a 128x64 OLED display.
- **Earthquake Detection**: Utilizes accelerometer data to determine if an earthquake has occurred based on defined thresholds.
- **Audio Alerts**: Plays a sound alert when an earthquake is detected using the DFPlayer Mini.
- **Telegram Notifications**: Sends urgent messages to specified Telegram chat IDs to alert users of detected earthquakes.
- **User Interaction**: Includes a button to stop the audio alert and reset the earthquake state.
- **Loading Animation**: Displays a sequence of images during startup to indicate loading status.

## Components Required
- ESP32 Microcontroller
- ADXL335 Accelerometer
- DFPlayer Mini MP3 Player Module
- 128x64 OLED Display
- Push Button
- Miscellaneous components (resistors, jumper wires, breadboard)

## Libraries Used
- **Adafruit_GFX**: Graphics library for the OLED display.
- **Adafruit_SSD1306**: OLED display driver.
- **DFRobotDFPlayerMini**: Library for controlling the DFPlayer Mini.
- **WiFi**: Library for WiFi connectivity.
- **HTTPClient**: Library for sending HTTP requests.
- **UniversalTelegramBot**: Library for interacting with the Telegram Bot API.

## How to Use

### Setup
1. Connect the components as per the circuit schematic.
2. Update the WiFi credentials and Telegram Bot Token in the code.

### Upload the Code
- Upload the code to the ESP32 using the Arduino IDE.

### Run the Program
1. Open the Serial Monitor to view debug messages.
2. The system will display loading images during startup, then show the seismic activity graph.

### Earthquake Detection
- The system continuously monitors accelerometer data. When an earthquake is detected, it will play an audio alert and send a notification to the Telegram chat IDs specified in the code.

### Stop the Alert
- Press the button to stop the audio alert and reset the earthquake state.

## Notes
- Ensure that the accelerometer is properly calibrated for accurate readings.
- Adjust the earthquake detection thresholds as needed based on the expected sensitivity and environment.
