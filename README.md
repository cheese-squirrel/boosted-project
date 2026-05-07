# Boosted Project

A replication of the pairing protocol between a boosted board and remote using an ESP32. My current board version is v1.5.2 and remote is v2.3.3.

## Setup

In order to replicate this project, you need to acquire an [ESP32 MCU](https://www.espressif.com/en/products/socs/esp32).

To get started I recommend following these resources to get setup with ESP-IDF BLE library:
1. https://docs.espressif.com/projects/esp-idf/en/latest/esp32/get-started/
2. https://github.com/espressif/esp-idf

The code was last tested on an ESP32-S3-nano, installed with ESP-IDF v6.0.1.

To make it easier for myself, I set up my development environment through vscode:
https://docs.espressif.com/projects/esp-idf/en/v4.2.3/esp32/get-started/vscode-setup.html

You only need to work with the code in the `esp-ble-remote`. The rest is a bit of a mess and was for testing/dev purposes.
Look for the ESP_GATTS_WRITE_EVT and ESP_GATTS_CONF_EVT cases in the `gatts_profile_controls_event_handler` function (around line 780).
The indication data in there contains the data sent to the board with information about speed and button states.

## Readings

I recommend you read this [blog post](https://medium.com/@johnathanchiu1065/side-project-series-reverse-engineering-the-boosted-board-remote-ceda4c30a74a) I wrote for the exact details.

I also wrote down all the boosted board/remote services and characteristics on this doc: https://docs.google.com/document/d/1elPj-vNOmTOq7oeU73JZj5jzti-n7vpdX68a-TypZo0/edit?usp=sharing

## Additional

Feel free to reach out to me and contribute to this repository/carry forth this project!



