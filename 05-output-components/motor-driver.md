# Motor Driver Guide

The **Motor Driver** is an output power interface component that enables microcontrollers to safely control speed and rotation direction for DC motors without overloading the board's circuit.

<p align="center">
  <img src="../images/PNG - TOP - SprouT - SENANG - Motor Driver.png" alt="Motor Driver" width="300">
</p>

---

## How It Works

* **Type:** Power Driver / Output Actuator
* **Function:** Uses an H-bridge circuit topology to switch high-current power supplies to motors using low-power control signals from the SprouT board.
* **Signal Input:** 
  * **Direction Control (IN1/IN2):** Determines forward or reverse rotation.
  * **Speed Control (PWM):** Regulates motor speed via pulse-width modulation signals.

---

## Connection Setup

1. Take your **SprouT Base Board** and plug in your central controller microchip.
2. Connect your DC motors to the terminal outputs of the **Motor Driver** module.
3. Plug the control cable from the motor driver into the assigned **Motor / PWM Port** on your SprouT Base Board.
4. Connect an external 7–12V DC power source to power the motors safely.
5. Plug the USB cable into your board and connect it to your computer.

> **Safety Tip:** Always connect external power to the driver board when operating heavy DC motor loads!

---

## PictoBlox Programming Guide

### 1. Board & Mode Setup
* Open **PictoBlox**.
* Set your board to **[Arduino Nano / ION32 / Micro:bit]** in the top toolbar.
* Select **Upload Mode** (or **Stage Mode** for real-time testing).

### 2. Required Code Blocks
Look for the following blocks in the **Actuators** palette:

* `set motor ( ) direction ( ) speed ( )`
* `stop motor ( )`

### 3. Example Logic Script
Here is a simple logic script to control a motor via driver:

1. Add the `When [Board] starts up` hat block.
2. Attach a `forever` loop.
3. Inside the loop:
   * Set motor `1` direction `Clockwise` at speed `100%`.
   * `wait 3 seconds`.
   * Set motor `1` direction `Counter-Clockwise` at speed `50%`.
   * `wait 3 seconds`.

---

## Troubleshooting

* **Board Resets When Motor Starts:** Your motors are drawing too much current from the microcontroller. Attach an external 7–12V DC power supply to the SprouT base board power input.
* **One Motor Not Moving:** Verify that output terminal screw contacts are clamped down tightly on the bare wire leads.