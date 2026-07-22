# Light Emitter (LED) Guide

The **Light Emitter (LED)** is a basic visual output component that emits light when powered. It allows your SprouT board to display visual indicators, warning lights, or status signals.

<p align="center">
  <img src="../images/PNG - TOP - SprouT - SENANG - Light Emitter - Red.png" alt="Light Emitter LED" width="300">
</p>

---

## How It Works

* **Type:** Output Component (Digital / PWM)
* **Function:** A semiconductor light source that illuminates when an electrical current flows through it in the forward direction.
* **Signal Input:** 
  * **HIGH (1):** Illuminates the LED.
  * **LOW (0):** Turns the LED off.
  * **PWM (0 - 255):** Controls the brightness level of the LED.

---

## Connection Setup

1. Take your **SprouT Base Board** and plug in your central controller microchip.
2. Connect one end of the modular cable to the **Light Emitter** module.
3. Plug the other end of the cable into a **Digital / PWM Port** (e.g., Digital Pin 13) on your SprouT Base Board.
4. Plug the USB cable into your board and connect it to your computer.

> **Safety Tip:** Always plug in your hardware components before powering on your board via USB!

---

## PictoBlox Programming Guide

### 1. Board & Mode Setup
* Open **PictoBlox**.
* Set your board to **[Arduino Nano / ION32 / Micro:bit]** in the top toolbar.
* Select **Upload Mode** (or **Stage Mode** for real-time testing).

### 2. Required Code Blocks
Look for the following blocks in the **Pin / Board** palette:

* `set digital pin ( ) output (HIGH/LOW)`
* `set PWM pin ( ) output ( )`

### 3. Example Logic Script
Here is a simple logic script to blink the LED:

1. Add the `When [Board] starts up` hat block.
2. Attach a `forever` loop.
3. Inside the loop:
   * `set digital pin 13 output HIGH`
   * `wait 1 seconds`
   * `set digital pin 13 output LOW`
   * `wait 1 seconds`

---

## Troubleshooting

* **LED Does Not Light Up:** Check that the modular cable is fully seated in the board port and verify the pin number matches your code.
* **Dim Lighting:** Ensure the pin is configured for standard output and not receiving an unexpectedly low PWM value.