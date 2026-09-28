# BreathSentry

Contact-free respiratory-illness early-warning monitor for shared rooms (IoT course project, BITS Pilani Dubai).

**Live dashboard:** https://tanishhari.github.io/breathsentry/

## How it works

ESP32 + INMP441 mic + CCS811/HDC1080 + DHT22 + HLK-LD2410 -> MQTT over WiFi (Mosquitto broker on a Raspberry Pi) -> Python risk engine (CO2 ventilation estimate + Wells-Riley infection risk, MFCC cough/sneeze classifier) -> web dashboard.

## Software

- ESP32 firmware: Arduino C++ (PlatformIO)
- Broker: Eclipse Mosquitto (MQTT)
- Raspberry Pi: Python (paho-mqtt, librosa, scikit-learn)
- Dashboard: HTML + Chart.js, hosted on GitHub Pages

The dashboard currently replays a verified test session (simulated sensor data) until the hardware is wired up.
