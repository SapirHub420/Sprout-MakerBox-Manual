# Sound Sensor Guide

The **Sound Sensor** is an input component that uses an onboard microphone to detect sound signals, ambient noise levels, and sudden audio spikes like claps or shouts.

<p align="center">
  <img src="../../images/PNG - TOP - SprouT - SENANG - Sound Sensor.png" alt="Sound Sensor" width="300">
</p>

---

## How It Works

* **Type:** Input Component (Digital / Analog)
* **Function:** Converts acoustic sound waves into electrical signals via an electret microphone element and onboard signal amplifier.
* **Signal Output:** 
  * **Analog Value (0 - 1023):** Represents relative volume/sound intensity levels.
  * **HIGH (1) / LOW (0):** Digital trigger signal when sound volume exceeds a set threshold.

---

## Connection Setup

1. Take your **SprouT Base Board** and plug in your central controller microchip.
2. Connect one end of the modular cable to the **Sound Sensor** module.
3. Plug the other end of the cable into an **Analog Port** (e.g., Analog Pin A2) or **Digital Port** on your SprouT Base Board.
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

* `read analog pin ( )` or `read digital pin ( )`

### 3. Example Logic Script
Here is a simple logic script to detect sound spikes (such as a hand clap):

1. Add the `When [Board] starts up` hat block.
2. Attach a `forever` loop.
3. Inside the loop, add an `if ... then ... else` condition:
   * **Condition:** If `read analog pin [A2]` is greater than `500`
   * **Action:** Toggle a light or buzzer output.
   * **Else:** Keep default state.

---

## Troubleshooting

* **Too Sensitive / Not Triggering:** Adjust the sensitivity potentiometer on the sensor module board using a small screwdriver.
* **Constant High Signal:** Background room noise may be too high; increase your code's comparative threshold level.