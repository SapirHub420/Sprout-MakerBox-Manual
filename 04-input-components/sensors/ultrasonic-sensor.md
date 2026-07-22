# Ultrasonic Distance Sensor Guide

The **Ultrasonic Sensor** is an input component that measures distance to an object by projecting high-frequency sound waves and timing their echo reflections.

<p align="center">
  <img src="../images/PNG - TOP - SprouT - SENANG - Ultrasonic Sensor.png" alt="Ultrasonic Sensor" width="300">
</p>

---

## How It Works

* **Type:** Input Component (Distance Sensor)
* **Function:** Emits an ultrasonic burst from a transmitter transducer and measures time elapsed for the signal to bounce off a target surface and return to the receiver transducer.
* **Signal Output:** 
  * **Distance Value (cm):** Calculated numerical distance based on sound wave flight time.

---

## Connection Setup

1. Take your **SprouT Base Board** and plug in your central controller microchip.
2. Connect one end of the modular cable to the **Ultrasonic Sensor** module.
3. Plug the other end of the cable into the designated **Ultrasonic Sensor Port** (or configured Trigger/Echo Digital Pins) on your SprouT Base Board.
4. Plug the USB cable into your board and connect it to your computer.

> **Safety Tip:** Always plug in your hardware components before powering on your board via USB!

---

## PictoBlox Programming Guide

### 1. Board & Mode Setup
* Open **PictoBlox**.
* Set your board to **[Arduino Nano / ION32 / Micro:bit]** in the top toolbar.
* Select **Upload Mode** (or **Stage Mode** for real-time testing).

### 2. Required Code Blocks
Look for the following block in the **Sensor Extension** palette:

* `read ultrasonic sensor trig ( ) echo ( ) distance in cm`

### 3. Example Logic Script
Here is a simple logic script to detect obstacle distance:

1. Add the `When [Board] starts up` hat block.
2. Attach a `forever` loop.
3. Inside the loop, add an `if ... then ... else` condition:
   * **Condition:** If `read ultrasonic distance in cm` is less than `15`
   * **Action:** Stop movement or trigger a distance warning.
   * **Else:** Proceed with clear pathway routines.

---

## Troubleshooting

* **Distance Returns Zero or 400+ cm:** Verify Trigger and Echo pin assignments in your block settings match the physical board connection.
* **Soft Target Surface Issues:** Soft materials (e.g., cloth, foam) absorb sound waves instead of reflecting them, leading to false distance readings.