# Air Quality Sensor Guide

The **Air Quality Sensor (Gas Sensor MP-135)** is an analog input component that detects ambient gas concentrations in the surrounding environment. It allows your SprouT board to monitor air pollution levels, smoke, and combustible gases.

<p align="center">
  <img src="../images/PNG - TOP - SprouT - SENANG - Gas Sensor MP-135 (Air Quality).png" alt="Air Quality Sensor" width="300">
</p>

---

## How It Works

* **Type:** Input Component (Analog)
* **Function:** Measures gas concentrations by detecting changes in resistance across its internal sensing layer when gas molecules bind to it.
* **Signal Output:** 
  * **Analog Value (0 - 1023):** Returns a continuous voltage signal proportional to the concentration of detected target gases in the air.

---

## Connection Setup

1. Take your **SprouT Base Board** and plug in your central controller microchip.
2. Connect one end of the modular cable to the **Air Quality Sensor** module.
3. Plug the other end of the cable into an **Analog Port** (e.g., Analog Pin A0) on your SprouT Base Board.
4. Plug the USB cable into your board and connect it to your computer.

> **Safety Tip:** Always plug in your hardware components before powering on your board via USB!

---

## PictoBlox Programming Guide

### 1. Board & Mode Setup
* Open **PictoBlox**.
* Set your board to **[Arduino Nano / ION32 / Micro:bit]** in the top toolbar.
* Select **Upload Mode** (or **Stage Mode** for real-time testing).

### 2. Required Code Blocks
Look for the following block in the **Pin / Board** palette:

* `read analog pin ( )`

### 3. Example Logic Script
Here is a simple logic script to read air quality readings continuously:

1. Add the `When [Board] starts up` hat block.
2. Attach a `forever` loop.
3. Inside the loop, add an `if ... then ... else` condition:
   * **Condition:** If `read analog pin [A0]` is greater than threshold value (e.g., `400`)
   * **Action:** Trigger an alarm or turn ON a warning indicator.
   * **Else:** Keep status indicators normal.

---

## Troubleshooting

* **Inaccurate Initial Readings:** Gas sensors require a brief warm-up period (30–60 seconds) after powering on before readings stabilize.
* **No Value Change:** Ensure the cable is plugged into an **Analog** pin (A0–A7), as digital ports cannot process variable gas concentration levels.