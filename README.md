# Wearable Heat Stroke Early Warning System

**Graduation Project – Computer Engineering**

**Hardware Development & Prototype Integration**  
**Contributor:** Tiba Khalid

---

## 1. Project Overview

The Wearable Heat Stroke Early Warning System is a smart wearable device designed to monitor environmental and physiological parameters and estimate potential heat-related health risks.

The system uses multiple sensors connected to an ESP32-C3 microcontroller to collect real-time measurements. These measurements will later be processed using a Machine Learning model and communicated to an Android application through Bluetooth Low Energy (BLE).

The main objective is to develop a wearable prototype capable of monitoring relevant conditions and providing early risk alerts.

> This project is an experimental monitoring prototype, not a certified medical diagnostic device.

## 2. Hardware Components

| Component | Function |
|---|---|
| ESP32-C3 Super Mini | Main microcontroller |
| MAX30102 | Heart rate and SpO2 monitoring |
| MLX90614 | Non-contact skin surface temperature measurement |
| SHT41 | Ambient temperature and humidity measurement |
| MPU6050 | Motion and activity monitoring |
| OLED 0.96" SSD1306 | Displaying sensor readings |
| LiPo Battery 650mAh | Planned portable power source |
| Charging and Power Management Board | To be finalized |

## 3. Work Completed – Hardware Development

**Contributor: Tiba Khalid**

The following hardware development tasks have been completed or started:

### 3.1 ESP32-C3 Setup

- Prepared the ESP32-C3 Super Mini development board.
- Installed and configured Arduino IDE.
- Configured the ESP32 board support package.
- Connected the development board to the computer through USB.
- Successfully uploaded and executed test programs.

### 3.2 Sensor Preparation and Testing

- Prepared the required sensor modules.
- Installed the required Arduino libraries.
- Tested the MPU6050 motion sensor successfully.
- Prepared individual test programs for the other sensor modules.
- Worked on integrating the sensor modules into one hardware prototype.

### 3.3 Breadboard Circuit Assembly

- Started assembling the hardware prototype using two breadboards.
- Connected the ESP32-C3 to the breadboard.
- Established shared power and ground connections.
- Connected the I2C communication lines.
- Used GPIO4 as SDA and GPIO5 as SCL.
- Prepared the common I2C connection for the sensors and OLED display.

### 3.4 Software and Development Environment

The following Arduino libraries were prepared for sensor communication:

- Adafruit MPU6050
- Adafruit Unified Sensor
- Adafruit BusIO
- Adafruit SHT4x
- Adafruit MLX90614
- SparkFun MAX3010x Pulse and Proximity Sensor Library
- Adafruit SSD1306
- Adafruit GFX Library

### 3.5 Preliminary Wearable Design

A modular wrist-worn design is being considered, consisting of:

- Display Module: OLED screen on the upper surface.
- Core Module: ESP32-C3 and internal electronic components.
- Heart Rate Module: MAX30102 positioned on the underside of the device.
- Skin Temperature Module: MLX90614 with a separate infrared sensing opening.
- Environmental Sensor: SHT41 positioned near a ventilated side opening.
- Motion Sensor: MPU6050 fixed inside the main enclosure.

A 3D-printed enclosure and silicone wristband are planned for the next development stage.

---

## 4. I2C Communication

The prototype uses I2C communication to connect multiple sensor modules through shared data and clock lines.

| Device | Expected I2C Address |
|---|---|
| MPU6050 | 0x68 / 0x69 |
| SHT41 | 0x44 |
| MLX90614 | 0x5A |
| MAX30102 | 0x57 |
| OLED SSD1306 | 0x3C / 0x3D |

**ESP32-C3 I2C Pin Configuration:**

| Signal | GPIO |
|---|---|
| SDA | GPIO4 |
| SCL | GPIO5 |

*Note: These are commonly used addresses. Actual addresses must be confirmed using an I2C scanner on the assembled prototype.*

## 5. Current Development Status

| Task | Status |
|---|---|
| ESP32-C3 setup and configuration | Completed |
| Arduino IDE configuration | Completed |
| Sensor library installation | Completed |
| MPU6050 individual test | Successfully tested |
| Breadboard hardware assembly | In progress |
| Individual sensor testing | In progress |
| Combined sensor integration | In progress |
| OLED integration and testing | In progress |
| Battery and charging circuit selection | Pending |
| Power consumption testing | Pending |
| PCB / Perfboard assembly | Pending |
| 3D enclosure design and printing | Pending |
| Wearable prototype testing | Pending |

## 6. Planned Development

The next hardware development stages include:

1. Complete individual testing of all sensors.
2. Verify I2C addresses and electrical compatibility.
3. Complete the combined sensor integration.
4. Finalize the battery and power management circuit.
5. Test the device's power consumption and operating time.
6. Transfer the circuit from the breadboard to a more stable assembly.
7. Design and print the 3D wearable enclosure.
8. Position and secure the sensors for reliable measurements.
9. Test the complete wearable prototype.

## 7. Project Software Integration

The hardware will eventually communicate with the following software components:

- **Embedded Firmware:** ESP32-C3 sensor acquisition and BLE communication.
- **Machine Learning:** Logistic Regression model with TensorFlow Lite.
- **Mobile Application:** Android application developed using Kotlin.
- **Communication:** Bluetooth Low Energy (BLE).

## 8. Repository Structure

The repository is intended to contain the following files:

```text
Wearable-Heat-Stroke-Alert/
│
├── README.md
│
├── Hardware/
│   ├── Components/
│   ├── Circuit_Diagrams/
│   ├── Pin_Configuration/
│   └── Prototype_Images/
│
├── Arduino_Code/
│   ├── MPU6050_Test/
│   ├── SHT41_Test/
│   ├── MLX90614_Test/
│   ├── MAX30102_Test/
│   ├── OLED_Test/
│   └── Integrated_Code/
│
├── Machine_Learning/
│
├── Android_Application/
│
└── Documentation/
```

## 9. Team Contributions

| Team Member | Main Responsibility |
|---|---|
| Tiba Khalid | Hardware development, sensor connections, prototype assembly and physical design |
| Dina Mohammed | Embedded programming and ESP32 firmware |
| Saja khalid | Machine Learning and model development |
| Mohammed ali | Android application and BLE integration |

---

**Project Status:** Hardware Prototype – Under Development

**Developed as part of the Computer Engineering Graduation Project.**
