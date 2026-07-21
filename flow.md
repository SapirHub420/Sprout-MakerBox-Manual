# [Component Name] Guide

The **[Component Name]** is an input component that detects [briefly describe what it measures/senses, e.g., user touches, light levels, tilt angle]. It allows your SprouT board to interact with and respond to the physical world.

<p align="center">
  <img src="../images/[Exact Image Filename].png" alt="[Component Name]" width="300">
</p>

---

## How It Works

* **Type:** Input Component ([Digital / Analog])
* **Function:** [Explain in simple 1-2 sentences how the component senses changes, e.g., "When pressed, it completes a circuit and sends a HIGH signal."]
* **Signal Output:** 
  * **[HIGH / LOW or Value Range]:** [What the signal means, e.g., "Returns HIGH (1) when activated, LOW (0) when idle."]

---

## Connection Setup

1. Take your **SprouT Base Board** and plug in your central controller microchip.
2. Connect one end of the modular cable to the **[Component Name]** module.
3. Plug the other end of the cable into **[Port Number / Pin Type, e.g., Port A or Digital Pin 2]** on your SprouT Base Board.
4. Plug the USB cable into your board and connect it to your computer.

> **Safety Tip:** Always plug in your hardware components before powering on your board via USB!

---

## PictoBlox Programming Guide

### 1. Board & Mode Setup
* Open **PictoBlox**.
* Set your board to **[Arduino Nano / ION32 / Micro:bit]** in the top toolbar.
* Select **Upload Mode** (or **Stage Mode** for real-time testing).

### 2. Required Code Blocks
Look for the following block in the **[Board / Sensor Extension]** palette:

* `[Insert Block Image / Representation, e.g., read digital pin ( )]`

### 3. Example Logic Script
Here is a simple logic script to read the sensor and perform an action:

1. Add the `When [Board] starts up` hat block.
2. Attach a `forever` loop.
3. Inside the loop, add an `if ... then ... else` condition:
   * **Condition:** If `read digital pin [Pin Number]` is equal to `1` (HIGH)
   * **Action:** Turn ON an LED or print a message.
   * **Else:** Turn OFF the LED.

---

## Troubleshooting

* **No Reading / Not Responding:** Double-check that the modular cable is firmly clicked into both the component and the base board port.
* **Inverted Signal:** If the sensor triggers backwards (e.g., ON when you expect OFF), switch your code condition from `1` (HIGH) to `0` (LOW).