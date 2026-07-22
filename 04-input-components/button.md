# Push Button Guide

The **Push Button** is a basic digital input component that detects physical tactile presses. It allows users to send manual trigger signals to your SprouT board to start actions, switch modes, or toggle components.

<p align="center">
  <img src="../images/sprout_makerbox_input_push_button.png" alt="Push Button" width="300">
</p>

---

## How It Works

* **Type:** Input Component (Digital)
* **Function:** Contains a physical tactile switch that completes or interrupts an electrical circuit when pressed by the user.
* **Signal Output:** 
  * **HIGH (1):** Signal sent when the button is actively pressed.
  * **LOW (0):** Signal sent when the button is released/idle.

---

## Connection Setup

1. Take your **SprouT Base Board** and plug in your central controller microchip.
2. Connect one end of the modular cable to the **Push Button** module.
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
Look for the following block in the **Pin / Board** palette:

* `read digital pin ( )`

### 3. Example Logic Script
Here is a simple logic script to read the button state and switch an output:

1. Add the `When [Board] starts up` hat block.
2. Attach a `forever` loop.
3. Inside the loop, add an `if ... then ... else` condition:
   * **Condition:** If `read digital pin [Pin Number]` is equal to `1` (HIGH)
   * **Action:** Set an output pin state to `HIGH`.
   * **Else:** Set output pin state to `LOW`.

---

## Troubleshooting

* **No Reading / Not Responding:** Double-check that the modular cable is firmly clicked into both the button module and the base board port.
* **Inverted Logic:** If the button triggers actions when not pressed, check if the module uses an inverted circuit and change your code condition from `1` (HIGH) to `0` (LOW).