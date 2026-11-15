# Smart-Soil-Automatic-Irrigation
Arduino Based Smart Soil and Automatic Irrigation Controller System
An Arduino-based embedded system that checks soil moisture and waters plants automatically. It has a tank-empty safety feature and an adjustable dry limit.

## Features
- Automatic pump control from soil moisture
- Adjustable moisture limit with two buttons
- Tank-empty protection with buzzer alert
- Live moisture % and pump status on LCD
- Hysteresis to avoid pump flicker

## Why it is useful
Low-cost, easy to build, saves water, and needs no human attention. It can be developed into a commercial smart agriculture product for farms, gardens, and greenhouses.

## Hardware
See [docs/components.md](docs/components.md).

## Circuit
- Diagram: [circuit/circuit_diagram.svg](circuit/circuit_diagram.svg)
- Pin table and pump wiring: [circuit/wiring.md](circuit/wiring.md)

## Software setup
1. Install the Arduino IDE.
2. Install the **LiquidCrystal_I2C** library (Sketch > Include Library > Manage Libraries).
3. Run `code/sensor_test.ino` to calibrate the sensor.
4. Edit `DRY_VALUE` and `WET_VALUE` in `code/irrigation.ino`.
5. Upload `code/irrigation.ino` to the Arduino Uno.

## Folder structure
```
smart-irrigation-controller/
├── README.md
├── LICENSE
├── .gitignore
├── code/
│   ├── irrigation.ino
│   └── sensor_test.ino
├── circuit/
│   ├── circuit_diagram.svg
│   └── wiring.md
└── docs/
    ├── components.md
    └── how_it_works.md
```

## Future improvements
- Wi-Fi monitoring with ESP32 and a phone app
- Temperature and humidity sensor (DHT11)
- Scheduled watering using a real-time clock (RTC)
- Data logging to an SD card

