# Tilt Sensor Guide

The **Tilt Sensor** is a digital input component that detects changes in orientation or inclination. It allows your SprouT board to know if an object is upright or tilted past a specific angle.

<p align="center">
  <img src="../images/PNG - TOP - SprouT - SENANG - Tilt Sensor.png" alt="Tilt Sensor" width="300">
</p>

---

## How It Works

* **Type:** Input Component (Digital)
* **Function:** Contains an internal metallic contact sphere that rolls inside a cavity, completing or breaking an electrical connection based on physical orientation.
* **Signal Output:** 
  * **HIGH (1):** Signal sent when the sensor is held upright.
  * **LOW (0):** Signal sent when the sensor is tilted or turned upside down.

---

## Connection Setup

1. Take your **SprouT Base Board** and plug in your central controller microchip.
2. Connect one end of the modular cable to the **Tilt Sensor** module.
3. Plug the other end of the cable into a **Digital Port** (e.g., Digital Pin 5) on your SprouT Base Board.
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
Here is a simple logic script to detect an orientation tilt alarm:

1. Add the `When [Board] starts up` hat block.
2. Attach a `forever` loop.
3. Inside the loop, add an `if ... then ... else` condition:
   * **Condition:** If `read digital pin [Pin Number]` is equal to `0` (LOW)
   * **Action:** Sound an alarm indicator.
   * **Else:** Keep system in standby mode.

---

## Troubleshooting

* **Jittery Readings During Motion:** Sudden shaking can cause the internal ball to bounce. Add a short delay (e.g., `wait 0.1 seconds`) in your code loop to stabilize signals.
* **No State Change:** Ensure the component is physically rotated past 45 degrees to allow the internal rolling contact element to move.