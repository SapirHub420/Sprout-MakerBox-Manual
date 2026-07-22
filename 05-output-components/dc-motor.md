# DC Motor Guide

The **DC Motor** is an electromechanical output component that converts electrical energy into rotational movement. It allows your SprouT board to power wheels, fans, and mechanical mechanisms.

<p align="center">
  <img src="../images/PNG - TOP - SprouT - SENANG - Motor Driver.png" alt="DC Motor" width="300">
</p>

---

## How It Works

* **Type:** Output Component (Actuator)
* **Function:** Uses electromagnetic fields to spin an internal shaft continuous in either clockwise or counter-clockwise directions.
* **Signal Control:** 
  * **Direction & Speed (PWM):** Controlled via motor driver signals regulating voltage level (speed) and polarity (direction).

---

## Connection Setup

1. Take your **SprouT Base Board** and plug in your central controller microchip.
2. Connect the **DC Motor** wires to the motor channel terminals on your SprouT board or Motor Driver extension module.
3. Plug the modular cable from the motor driver into the assigned **Motor Port / PWM Pins** on your SprouT Base Board.
4. Connect an external 7–12V DC power source if driving high-load motors.
5. Plug the USB cable into your board and connect it to your computer.

> **Safety Tip:** Always plug in your hardware components before powering on your board via USB! Never drive DC motors directly from microchip digital IO pins.

---

## PictoBlox Programming Guide

### 1. Board & Mode Setup
* Open **PictoBlox**.
* Set your board to **[Arduino Nano / ION32 / Micro:bit]** in the top toolbar.
* Select **Upload Mode** (or **Stage Mode** for real-time testing).

### 2. Required Code Blocks
Look for the following blocks in the **Actuators** palette:

* `run motor ( ) in direction ( ) at speed ( )%`
* `stop motor ( )`

### 3. Example Logic Script
Here is a simple logic script to drive a motor forward and backward:

1. Add the `When [Board] starts up` hat block.
2. Attach a `forever` loop.
3. Inside the loop:
   * Set `run motor 1 in direction [Forward] at speed [80]%`.
   * Add `wait (2) seconds`.
   * Set `run motor 1 in direction [Backward] at speed [80]%`.
   * Add `wait (2) seconds`.

---

## Troubleshooting

* **Motor Not Spinning / Humming:** Check if external power (7–12V DC) is connected. USB power alone is often insufficient to power DC motors.
* **Spinning Backwards:** Swap the two terminal wires of the DC motor connected to the motor output port.