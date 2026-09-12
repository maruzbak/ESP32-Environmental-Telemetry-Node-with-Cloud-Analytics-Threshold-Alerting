# ESP32-Environmental-Telemetry-Node-with-Cloud-Analytics-Threshold-Alerting
An end-to-end IoT edge monitoring system built on an ESP32 microcontroller, featuring real-time local display feedback, continuous cloud telemetry logging, and automated event-driven alerts.

## Key Features
- **Edge Sensing:** Interfaced DHT22 digital sensor for ambient temperature and humidity tracking.
- **Local Visualization:** Integrated a 128x64 SSD1306 OLED display via I2C (`Wire.h`) for on-site monitoring and status feedback.
- **Cloud Telemetry:** Formatted payloads pushed over Wi-Fi to a ThingSpeak channel via REST API at 15-second intervals.
- **Automated Alerting:** Implemented ThingSpeak React rules to trigger automated email dispatches upon high-temperature threshold breaches.

## Hardware Circuit Setup
| Component | ESP32 Pin | Interface Protocol |
| :--- | :--- | :--- |
| DHT22 Data | GPIO 15 | Digital One-Wire |
| SSD1306 SDA | GPIO 21 | I2C Data |
| SSD1306 SCL | GPIO 22 | I2C Clock |
| VCC / GND | 3V3 / GND | Power |

## Tech Stack
- **Embedded C++** (ESP32 Board Support Package)
- **Libraries:** `DHTesp`, `Adafruit_SSD1306`, `Adafruit_GFX`, `ThingSpeak`, `WiFi`
- **Cloud Infrastructure:** ThingSpeak Analytics & React Apps
