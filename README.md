# Home Energy Usage Dashboard

## Overview

This project monitors the home’s energy usage in real time, stores historical data, and presents a dashboard to help the user understand and optimize power consumption. Users can set budgets, get alerts, and optionally automate load control.

---

## Features

- Real‑time power/current measurement  
- Visualization of recent and historical energy usage (hourly/daily/weekly)  
- Budget setting & alerting  
- Appliance‑level monitoring (if multiple sensors)  
- Comparison over time (today vs yesterday, week vs week etc.)  
- (Optional) Automation to turn off non‑critical loads when usage is high  

---

## Components

### Hardware

| Component | Quantity | Purpose |
|---|---|---|
| ESP32 (or WiFi microcontroller) | 1 | Reads sensors & transmits data |
| Current sensor (e.g. CT clamp, ACS712 etc.) | 1 or more | To measure current |
| (Optional) Voltage sensor or assume fixed mains voltage | 1 | For calculating real power |
| Power supply | ‑ | To power device |
| Wires, enclosure etc. | ‑ | For connections, mounting |

### Software

- Arduino / PlatformIO for firmware  
- MQTT or HTTP for communication  
- Backend: e.g. Node.js / Python / cloud‑based service  
- Database: time series DB (InfluxDB / TimescaleDB) or NoSQL / SQL  
- Frontend: HTML/JS or React/Vue with charting library (e.g. Chart.js, D3.js)  

---

## Wiring / Setup

Describe how to wire the current sensor: how to connect CT, burden resistor if needed, signal conditioning. Connect microcontroller to WiFi. Point out safety (isolated measurement, ensure correct handling of mains voltage).

---

## Usage

1. Clone the repository  
2. Modify configuration (WiFi SSID, broker address, etc.)  
3. Upload firmware to the device  
4. Setup backend to receive & store data  
5. Run frontend to visualize data  
6. Configure alerts / budgets  

---

## Calibration

- Calibrate sensor readings (test with known loads)  
- If using CT, ensure correct burden resistor and safety isolation  
- Validate power calculation  

---

## Project Structure (Suggested)

