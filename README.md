# Smart Alarm System with Firebase Integration and RTC

## Overview

This project involves a smart alarm system that integrates Firebase, RTC (Real-Time Clock), and the DFPlayer Mini for an interactive and automated experience. The system allows users to set alarms, control connected devices, and manage the alarm schedules through Firebase. Additionally, it retrieves real-time data from a DS3231 RTC and displays the date and time via serial communication.

### Key Features:
- **RTC Integration**: Uses a DS3231 RTC to keep track of the current time and set alarms.
- **Firebase Integration**: Syncs alarm settings, medicine schedules, and other configurations from Firebase.
- **DFPlayer Mini Integration**: Plays audio through the DFPlayer Mini when certain events occur, like setting alarms or when no network is detected.
- **WiFi Connectivity**: The device connects to a WiFi network and retrieves configuration data from Firebase.
- **EEPROM Storage**: Saves alarm settings and medicine schedules in EEPROM to retain values between reboots.

## Hardware Requirements

- **ESP32/ESP8266**: The project is compatible with ESP32 and ESP8266 boards.
- **DFPlayer Mini MP3 Module**: Used to play audio files stored on an SD card.
- **DS3231 RTC Module**: Real-time clock for keeping track of the current time.
- **WiFi Connection**: Connect to a WiFi network to access Firebase.
- **LEDs**: Used to show various statuses (alarm notifications, no network detected, etc.).

## Software Libraries

- `Wire.h`: I2C library to communicate with the RTC module.
- `RtcDS3231.h`: Library for DS3231 RTC.
- `WiFi.h`/`ESP8266WiFi.h`: WiFi library for ESP32/ESP8266.
- `FirebaseESP32.h`/`FirebaseESP8266.h`: Firebase libraries for ESP32/ESP8266.
- `DFRobotDFPlayerMini.h`: Library to interact with the DFPlayer Mini.

## Wi-Fi and Firebase Configuration

To use this system, you need to set up Wi-Fi and Firebase. Replace the following placeholders with your actual data:

```cpp
#define WIFI_SSID "your_wifi_ssid"
#define WIFI_PASSWORD "your_wifi_password"
#define API_KEY "your_firebase_api_key"
#define DATABASE_URL "your_firebase_database_url"
