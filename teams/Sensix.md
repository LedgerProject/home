# Sensix

We build modular power quality measurement equipment that is affordable, easy to install, and open source. It measures all the generic electric meter parameters: Voltage, Current, Power, Energy, Power Factor, but its real value stands in accurately measuring Harmonic Distortions, up to 40th order.

Our mission is to automate electric energy audits with our analytics platform so that our clients can better maintain their electric grid and reduce energy costs by 30%.
All this while using energy responsibly and reducing climate change impact.

By providing affordable and open power quality measurement equipment, we hope to increase adoption also among households - choosing a freemium community account from [Sensix](https://sensix.io/). You benefit from accurate and permanent electric power tracking. In exchange, you contribute to an open, anonymized, and aggregated power quality map so that people can spot electric grid issues and held utilities responsible for keeping an optimal infrastructure for everybody to use.


## Technology

We use an ESP32 RTOS, for each DIN module (each phase) that connects to our AFE - ADE9153a, so that we collect the current and voltage waves @ 4ksps to compute all the electric parameters.

#### Interfaces

* MQTT (with SSL) over WiFi, to send/receive binary payloads - suitable for `cloud computing.
* Modbus RTU over RS485, to send/receive - suitable for `edge computing`.

#### Parameters

We maintain all parameters and registers [in one place](https://docs.google.com/spreadsheets/d/1-8I-vsCFemheWAyDiTNe6QQz5eJ-0ca78oh8UrcBhMo/edit#gid=329540371), for different systems.

- 1P - Single-phase
- 1P+N - Single-phase and Neutral
- 3P - Three-phase
- 3P+N - Three-phase and Neutral

#### Documentation

https://powermonitor.org/

We commit to maintain and update the docs constantly during the project.


## Repos

### Frontend

[Sensix PowerMap Frontend Repo](https://github.com/LedgerProject/sensix-power-map-frontend)

- Built with React Web
- Displays aggregated and anonymized power quality heat map


### Backend

[Sensix PowerMap Backend Repo](https://github.com/LedgerProject/sensix-power-map-backend)

- Built with Django / DRF / Python3
- Subscribes to Sensix MQTT Broker (or any other)
- Aggregates clean JSON payloads
- Exposes a REST API to integrate with the PowerMap Frontend.


### Firmware and Hardware

[Sensix PowerMonitor Repo](https://github.com/LedgerProject/sensix-power-monitor)

#### Hardware designs

- Designed to fit into a 2 DIN Module SPD base enclosure
- Instead of Ethernet and 24V AC power the controller has a USB transceiver chip to ease the development
- Powered by USB 5V DC
- Breakout headers for internal SPI bus to experiment with external RAM
- Breakout headers for I2C bus to add ST NFC module for configuration loading
- Shunt mounted directly on the SPD spade plugs

#### Firmware

- Built with ESP-IDF
- Properly unit tested
- Used and modified other 3rd party open-source software
