# Bidirectional ESP-NOW Wireless Communication Using ESP32 and DHT11

## Project Overview

This project demonstrates a bidirectional wireless communication system using two ESP32 development boards and the ESP-NOW protocol. Each ESP32 reads temperature and humidity data from a DHT11 sensor and exchanges the data directly with another ESP32 without requiring a Wi-Fi router or internet connection.

The received and transmitted sensor readings are displayed on an SSD1306 OLED display in real time.

---

## Features

- ESP-NOW peer-to-peer communication
- No Wi-Fi router required
- Real-time temperature monitoring
- Real-time humidity monitoring
- OLED display visualization
- Low-power wireless communication
- Two-way data exchange

---

## Hardware Components

| Component | Quantity |
|------------|------------|
| ESP32 DevKit V1 | 2 |
| DHT11 Sensor | 2 |
| SSD1306 OLED Display (128x64) | 2 |
| Breadboard | 2 |
| Jumper Wires | As Required |
| USB Cable | 2 |

---

## Circuit Connections

### DHT11 to ESP32

| DHT11 Pin | ESP32 Pin |
|------------|------------|
| VCC | 3.3V |
| GND | GND |
| DATA | GPIO 4 |

### OLED to ESP32

| OLED Pin | ESP32 Pin |
|------------|------------|
| VCC | 3.3V |
| GND | GND |
| SDA | GPIO 21 |
| SCL | GPIO 22 |

---

## Software Requirements

- Arduino IDE
- ESP32 Board Package
- Adafruit GFX Library
- Adafruit SSD1306 Library
- DHT Sensor Library
- WiFi Library
- ESP-NOW Library

---

## Installation

### Step 1: Install Arduino IDE

Download and install Arduino IDE.

### Step 2: Install ESP32 Board Package

Open:

Tools → Board → Boards Manager

Search:

ESP32

Install the latest version.

### Step 3: Install Required Libraries

Open:

Sketch → Include Library → Manage Libraries

Install:

- Adafruit GFX
- Adafruit SSD1306
- DHT Sensor Library

---

## Getting ESP32 MAC Address

Upload the following code:

```cpp
#include <WiFi.h>

void setup() {
  Serial.begin(115200);
  WiFi.mode(WIFI_STA);
  Serial.println(WiFi.macAddress());
}

void loop() {}
```

Copy the MAC address and place it in the peer ESP32 code.

---

## Working Principle

1. DHT11 measures temperature and humidity.
2. ESP32 reads sensor values.
3. ESP-NOW transmits the data wirelessly.
4. The second ESP32 receives the packet.
5. Received data is displayed on OLED.
6. Both ESP32 boards simultaneously send and receive data.

---

## OLED Output

### Node A

```text
NODE A

LOCAL
T: 28.5 C
H: 65 %

REMOTE
T: 30.2 C
H: 58 %
```

### Node B

```text
NODE B

LOCAL
T: 30.2 C
H: 58 %

REMOTE
T: 28.5 C
H: 65 %
```

---

## Applications

- Smart Agriculture
- Environmental Monitoring
- Industrial Automation
- Smart Home Systems
- Wireless Sensor Networks
- IoT Monitoring Systems

---

## Future Enhancements

- Cloud Data Logging
- Mobile App Integration
- Multiple ESP32 Nodes
- Battery Powered Deployment
- Alert Notification System

---

## Technologies Used

- Embedded Systems
- ESP32
- ESP-NOW Protocol
- IoT
- Arduino IDE
- DHT11 Sensor
- SSD1306 OLED Display

---

## Project Outcome

Successfully implemented a bidirectional wireless communication system using ESP32 and ESP-NOW protocol for real-time temperature and humidity monitoring without requiring internet connectivity.

---

## Author

BONALA KAVYA

Electronics and Communication Engineering (ECE)
