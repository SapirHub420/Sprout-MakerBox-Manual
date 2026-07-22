# Humidity and Temperature Sensor (DHT11) Guide

The **DHT11 Sensor** is a digital input component that measures environmental ambient temperature and relative humidity simultaneously. It allows your SprouT board to monitor local climate conditions.

<p align="center">
  <img src="../images/PNG - TOP - SprouT - SENANG - Humidity Sensor DHT11.png" alt="DHT11 Sensor" width="300">
</p>

---

## How It Works

* **Type:** Input Component (Digital / Protocol)
* **Function:** Uses a capacitive humidity sensor and a thermistor to measure surrounding air conditions and outputs data via a single-wire digital protocol.
* **Signal Output:** 
  * **Digital Serial Data:** Outputs digital data packets containing temperature (°C) and humidity (%) readings.

---

## Connection Setup

1. Take your **SprouT Base Board** and plug in your central controller microchip.
2. Connect one end of the modular cable to the **DHT11 Sensor** module.
3. Plug the other end of the cable into a **Digital Port** (e.g., Digital Pin 2) on your SprouT Base Board.
4. Plug the USB cable into your board and connect it to your computer.

> **Safety Tip:** Always plug in your hardware components before powering on your board via USB!

---

## PictoBlox Programming Guide

### 1. Board & Mode Setup
* Open **PictoBlox**.
* Set your board to **[Arduino Nano / ION32 / Micro:bit]** in the top toolbar.
* Select **Upload Mode** (or **Stage Mode** for real-time testing).

### 2. Required Code Blocks
Look for the following blocks in the **Sensor Extension** palette:

* `read temperature (°C) on pin ( )`
* `read humidity (%) on pin ( )`

### 3. Example Logic Script
Here is a simple logic script to monitor environment conditions:

1. Add the `When [Board] starts up` hat block.
2. Attach a `forever` loop.
3. Add a `wait (2) seconds` block (the DHT11 requires at least 1–2 seconds between readings).
4. Store or display `read temperature (°C) on pin [Pin Number]` and `read humidity (%) on pin [Pin Number]`.

---

## Troubleshooting

* **Readings Return Zero/NaN:** Check that the correct digital pin number is selected in your blocks and that the modular cable is securely seated.
* **Data Refresh Delay:** The DHT11 sensor updates once every 1–2 seconds; reading it faster may result in stale or missing data.