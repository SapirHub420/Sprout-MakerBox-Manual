# Potentiometer Guide

The **Potentiometer** is a variable analog input component that measures rotational movement. By turning its knob, you manually adjust electrical resistance to send smooth, continuous value ranges to your SprouT board.

<p align="center">
  <img src="../images/sprout_makerbox_input_potentiometer.png" alt="Potentiometer" width="300">
</p>

---

## How It Works

* **Type:** Input Component (Analog)
* **Function:** Uses a rotating wiper across a resistive track to change output voltage proportionally to the knob's position.
* **Signal Output:** 
  * **Analog Value (0 - 1023):** Returns continuous values ranging from 0 (fully turned counter-clockwise) to 1023 (fully turned clockwise).

---

## Connection Setup

1. Take your **SprouT Base Board** and plug in your central controller microchip.
2. Connect one end of the modular cable to the **Potentiometer** module.
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
Here is a simple logic script to read the potentiometer value and continuously check its position:

1. Add the `When [Board] starts up` hat block.
2. Attach a `forever` loop.
3. Inside the loop, add your variable or conditional mapping:
   * **Action:** Read `read analog pin [A0]` and print or map the returned value (0–1023) to control motor speed, LED brightness, or servo angles.

---

## Troubleshooting

* **Value Jumps Erratically:** Verify that the cable connection to the analog input port is secure and free of dust or movement.
* **No Value Change:** Ensure the cable is plugged into an **Analog** pin (A0–A7), as digital pins cannot measure variable resistance ranges.