# Light Sensor (LDR) Guide

The **Light Sensor (LDR)** is an analog input component that measures surrounding light levels. It allows your SprouT board to respond to environmental brightness, darkness, or shadows.

<p align="center">
  <img src="../../images/PNG - TOP - SprouT - SENANG - Light Sensor.png" alt="Light Sensor" width="300">
</p>

---

## How It Works

* **Type:** Input Component (Analog)
* **Function:** Uses a Light Dependent Resistor (LDR) whose electrical resistance decreases as ambient light intensity increases.
* **Signal Output:** 
  * **Analog Value (0 - 1023):** Returns higher analog values in bright light environments and lower values in dark conditions.

---

## Connection Setup

1. Take your **SprouT Base Board** and plug in your central controller microchip.
2. Connect one end of the modular cable to the **Light Sensor** module.
3. Plug the other end of the cable into an **Analog Port** (e.g., Analog Pin A1) on your SprouT Base Board.
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
Here is a simple logic script for an automatic night light system:

1. Add the `When [Board] starts up` hat block.
2. Attach a `forever` loop.
3. Inside the loop, add an `if ... then ... else` condition:
   * **Condition:** If `read analog pin [A1]` is less than `300` (Dark)
   * **Action:** Turn ON an LED component.
   * **Else:** Turn OFF the LED component.

---

## Troubleshooting

* **No Sensitivity to Light Changes:** Ensure the sensor is plugged into an **Analog** pin (A0–A7), as digital pins cannot process variable voltage signals.
* **Inverted Values:** Depending on circuit configuration, cover the LDR to verify if your values decrease or increase, then update your logic threshold accordingly.