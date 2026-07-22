# Capacitive Touch Sensor Guide

The **Capacitive Touch Sensor** is a digital input component that detects direct human physical touch or close skin contact without requiring physical mechanical force.

<p align="center">
  <img src="../../images/PNG - TOP - SprouT - SENANG - Capacitive Sensor.png" alt="Capacitive Touch Sensor" width="300">
</p>

---

## How It Works

* **Type:** Input Component (Digital)
* **Function:** Detects subtle body electrical capacitance changes when a user touches the sensor pad.
* **Signal Output:** 
  * **HIGH (1):** Signal returned when skin touch is detected on the sensor pad.
  * **LOW (0):** Signal returned when the sensor pad is untouched.

---

## Connection Setup

1. Take your **SprouT Base Board** and plug in your central controller microchip.
2. Connect one end of the modular cable to the **Capacitive Touch Sensor** module.
3. Plug the other end of the cable into a **Digital Port** (e.g., Digital Pin 4) on your SprouT Base Board.
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
Here is a simple logic script to use the touch pad as a digital toggle:

1. Add the `When [Board] starts up` hat block.
2. Attach a `forever` loop.
3. Inside the loop, add an `if ... then ... else` condition:
   * **Condition:** If `read digital pin [Pin Number]` is equal to `1` (HIGH)
   * **Action:** Trigger an output state or play a sound tone.
   * **Else:** Turn off output.

---

## Troubleshooting

* **False Triggers:** Avoid touching uninsulated soldered connections on the back of the PCB module; touch only the designated touch pad surface.
* **Unresponsive:** Ensure hands are clean and dry, and verify the cable is clicked firmly into the digital header port.