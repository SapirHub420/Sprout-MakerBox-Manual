# Vibration Sensor Guide

The **Vibration Sensor** is a digital input component that detects mechanical impacts, movement, shocks, or sudden vibrations.

<p align="center">
  <img src="../../images/PNG - TOP - SprouT - SENANG - Vibration Sensor.png" alt="Vibration Sensor" width="300">
</p>

---

## How It Works

* **Type:** Input Component (Digital)
* **Function:** Contains a flexible conductive spring and central contact pin that briefly touch during mechanical vibration, momentarily closing an electrical circuit.
* **Signal Output:** 
  * **LOW (0):** Short momentary state returned when physical vibration/impact is sensed.
  * **HIGH (1):** Idle baseline state when stationary.

---

## Connection Setup

1. Take your **SprouT Base Board** and plug in your central controller microchip.
2. Connect one end of the modular cable to the **Vibration Sensor** module.
3. Plug the other end of the cable into a **Digital Port** (e.g., Digital Pin 6) on your SprouT Base Board.
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

* `read digital pin ( )`

### 3. Example Logic Script
Here is a simple logic script to log impact events:

1. Add the `When [Board] starts up` hat block.
2. Attach a `forever` loop.
3. Inside the loop, add an `if ... then` condition:
   * **Condition:** If `read digital pin [Pin Number]` is equal to `0` (LOW)
   * **Action:** Increment an impact counter or turn ON an indicator.

---

## Troubleshooting

* **Missed Impacts:** Because vibration contact pulses are extremely fast, avoid using long `wait` blocks inside your code loop so the signal is not missed.
* **Continuous False Pulses:** Ensure the component module is securely mounted and not subject to motor vibrations on the same chassis.