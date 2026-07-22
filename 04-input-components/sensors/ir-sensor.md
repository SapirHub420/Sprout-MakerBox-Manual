# Infrared Sensor Guide

The **Infrared (IR) Sensor** is a digital input component that detects objects or obstacles in close proximity by emitting and sensing reflected infrared light.

<p align="center">
  <img src="../../images/PNG - TOP - SprouT - SENANG - Infrared Sensor.png" alt="Infrared Sensor" width="300">
</p>

---

## How It Works

* **Type:** Input Component (Digital)
* **Function:** Emits infrared light from an IR LED and measures light bounced back to an IR receiver photodiode when an object blocks its field of view.
* **Signal Output:** 
  * **LOW (0):** Triggered when an object reflects IR light back to the receiver.
  * **HIGH (1):** Idle state when no reflection or object is detected.

---

## Connection Setup

1. Take your **SprouT Base Board** and plug in your central controller microchip.
2. Connect one end of the modular cable to the **Infrared Sensor** module.
3. Plug the other end of the cable into a **Digital Port** (e.g., Digital Pin 3) on your SprouT Base Board.
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
Here is a simple logic script to detect obstacles:

1. Add the `When [Board] starts up` hat block.
2. Attach a `forever` loop.
3. Inside the loop, add an `if ... then ... else` condition:
   * **Condition:** If `read digital pin [Pin Number]` is equal to `0` (LOW)
   * **Action:** Stop motors or activate an obstacle alert.
   * **Else:** Continue normal operation.

---

## Troubleshooting

* **Sensor Always Active:** Adjust the small sensitivity potentiometer on the IR module using a small screwdriver until the indicator LED turns off when no object is present.
* **Ambient Light Interference:** Direct sunlight or bright incandescent lighting can interfere with infrared optical detection.