
# IoT-Based Smart Energy Meter with Blynk Cloud

This project is a dual-channel energy meter using ESP32, designed to measure real-time voltage, current, and power, and send the data to the Blynk Cloud for remote monitoring. The system includes options for cloud-based access, LCD display, and offline monitoring.

Developed collaboratively as part of a hackathon, this project emphasizes teamwork, innovation, and real-world IoT applications.

---

## Project Directory

| File Name                         | Description                                      |
|----------------------------------|--------------------------------------------------|
| complete setup.jpeg              | Full prototype hardware image                    |
| with lcd.txt                     | Code version with LCD display                    |
| without cloud and lcd.txt        | Code for offline-only version                    |
| energy meter with bill generat...| Code with billing logic                          |
| energy meter using iot(2).docx   | Project documentation/report                     |
| esp32.jpeg                       | ESP32 microcontroller image                      |
| layout of energy meter .jpeg     | Wiring layout and component positioning          |
| voltage sensor.jpeg              | Voltage sensor module image (ZMPT101B)           |
| README.md                        | This project documentation file                  |

---

## Project Features

- Dual channel monitoring (Voltage and Current for two loads)
- Real-time power calculation
- ESP32 microcontroller with Wi-Fi support
- Remote monitoring through Blynk Cloud
- Mobile dashboard for real-time data visualization
- Optional features: LCD display, offline version, bill generation

---

## Hardware Overview

| Component         | Description                          |
|------------------|--------------------------------------|
| ESP32            | Wi-Fi-enabled microcontroller        |
| ZMPT101B         | AC voltage sensor                    |
| ACS712/SCT013    | AC current sensor                    |
| Blynk App        | Remote dashboard (iOS/Android)       |
| LCD Display      | Local monitoring (optional)          |
| Breadboard/Wires | Circuit prototyping and connections  |
| Bulbs with Holders| Load testing elements               |

---

## How the System Works

1. Voltage and current are sensed using ZMPT101B and ACS712/SCT sensors.
2. ESP32 reads the analog values using ADC pins.
3. Power is calculated using the formula: `Power = Voltage × Current`.
4. Data is pushed to Blynk Cloud using virtual pins.
5. Users monitor the data on the Blynk mobile dashboard.

---

## Blynk Integration

- Setup a Blynk IoT project and obtain the Auth Token.
- Use the following virtual pins:

| Parameter      | Virtual Pin |
|----------------|-------------|
| Voltage 1      | V0          |
| Voltage 2      | V1          |
| Current 1      | V2          |
| Current 2      | V3          |
| Power 1        | V4          |
| Power 2        | V5          |

Example code snippet:
```cpp
Blynk.virtualWrite(V0, voltage1);
Blynk.virtualWrite(V1, voltage2);
Blynk.virtualWrite(V2, current1);
Blynk.virtualWrite(V3, current2);
Blynk.virtualWrite(V4, power1);
Blynk.virtualWrite(V5, power2);
```

---

## Running the Project

1. Clone or download the repository.
2. Open `with lcd.txt` or `without cloud and lcd.txt` in the Arduino IDE.
3. Replace the Wi-Fi SSID, password, and Blynk Auth Token.
4. Upload the code to the ESP32 board.
5. Open the Blynk mobile app and start monitoring.

---

## Learning Outcomes

- Integration of analog sensors with microcontrollers
- Real-time power monitoring using ESP32
- Remote data visualization using Blynk Cloud
- Team-based collaborative hardware development
- Versioning with and without cloud or LCD

---

## Team Members

| Name           | Responsibility                      |
|----------------|--------------------------------------|
| Your Name      | Embedded programming and integration |
| Teammate 1     | Hardware circuit setup               |
| Teammate 2     | Blynk and cloud integration          |
| Teammate 3     | Documentation and testing            |

---

## Image Previews

| Full Setup                 | Layout                        | ESP32 Board            | Voltage Sensor        |
|---------------------------|-------------------------------|------------------------|------------------------|
| ![](./complete%20setup.jpeg) | ![](./layout%20of%20energy%20meter%20.jpeg) | ![](./esp32.jpeg) | ![](./voltage%20sensor.jpeg) |

---

## Documentation

For detailed explanation and circuit logic, refer to:

- `energy meter using iot(2).docx`

---

## License

This project is developed for educational purposes. Contributions and improvements are welcome.

---

## Contact

- Email: your.email@example.com
- GitHub: [yourusername](https://github.com/yourusername)
