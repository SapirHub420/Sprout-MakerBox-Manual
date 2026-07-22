# Relay Module Guide

The **Relay 1-Channel Module** is an electrically operated switch output component. It allows your low-voltage SprouT board to isolate and trigger higher-voltage or higher-current devices safely.

<p align="center">
  <img src="../images/PNG - TOP - SprouT - SENANG - Relay 1-Channel.png" alt="Relay Module" width="300">
</p>

---

## How It Works

* **Type:** Output Component (Switching Relay)
* **Function:** Uses an internal electromagnet to mechanically pull an internal contact switch, opening or closing an isolated secondary circuit.
* **Signal Input:** 
  * **HIGH (1):** Activates the internal coil, closing the Normally Open (NO) circuit contact.
  * **LOW (0):** Deactivates the coil, opening the circuit contact.

---

## Connection Setup

1. Take your **SprouT Base Board** and plug in your central controller microchip.
2. Connect one end of the modular cable to the **Relay Module**.
3. Plug the other end of the cable into a **Digital Port** (e.g., Digital Pin 7) on your SprouT Base Board.
4. Wire your external load across the Relay terminal blocks (Common and Normally Open).
5. Plug the USB cable into your board and connect it to your computer.

> **Safety Tip:** Always plug in your low-voltage hardware components before powering on your board. Never expose high-voltage AC connections without instructor supervision!

---

## PictoBlox Programming Guide

### 1. Board & Mode Setup
* Open **PictoBlox**.
* Set your board to **[Arduino Nano / ION32 / Micro:bit]** in the top toolbar.
* Select **Upload Mode** (or **Stage Mode** for real-time testing).

### 2. Required Code Blocks
Look for the following block in the **Pin / Board** palette:

* `set digital pin ( ) output (HIGH/LOW)`

### 3. Example Logic Script
Here is a simple logic script to toggle a relay switch:

1. Add the `When [Board] starts up` hat block.
2. Attach a `forever` loop.
3. Inside the loop:
   * `set digital pin 7 output HIGH` (Relay ON - Click sound heard)
   * `wait 2 seconds`
   * `set digital pin 7 output LOW` (Relay OFF)
   * `wait 2 seconds`

---

## Troubleshooting

* **No Audible Click Sound:** Verify that the digital control pin output is switching between HIGH and LOW in your code.
* **Connected Load Doesn't Power On:** Double-check that your secondary circuit wires are connected between the **COM** (Common) and **NO** (Normally Open) screw terminals.