# LCD Screen (I2C 1602) Guide

The **LCD Screen (1602 with I2C)** is a text display output component capable of showing up to 32 characters (16 characters across 2 lines). It allows your SprouT board to display sensor values, system states, and text messages.

<p align="center">
  <img src="../images/PNG - TOP - SprouT - SENANG - LCD I2C 1602 - Front.png" alt="LCD Screen I2C 1602" width="300">
</p>

---

## How It Works

* **Type:** Output Component (I2C Display)
* **Function:** Uses Liquid Crystal Display technology combined with an I2C backpack module to display text using only two communication lines (SDA and SCL).
* **Signal Interface:** 
  * **I2C Protocol:** Transmits display coordinates, ASCII text, and backlight commands over the I2C bus.

---

## Connection Setup

1. Take your **SprouT Base Board** and plug in your central controller microchip.
2. Connect one end of the modular cable to the **LCD Module**.
3. Plug the other end of the cable into the designated **I2C Port** (SDA/SCL) on your SprouT Base Board.
4. Plug the USB cable into your board and connect it to your computer.

> **Safety Tip:** Always plug in your hardware components before powering on your board via USB!

---

## PictoBlox Programming Guide

### 1. Board & Mode Setup
* Open **PictoBlox**.
* Set your board to **[Arduino Nano / ION32 / Micro:bit]** in the top toolbar.
* Add the **Display / LCD** extension from the Extension Library.
* Select **Upload Mode** (or **Stage Mode** for real-time testing).

### 2. Required Code Blocks
Look for the following blocks in the **LCD Extension** palette:

* `initialize LCD at address (0x27 or 0x3F)`
* `print ( ) on LCD line ( ) position ( )`
* `clear LCD`

### 3. Example Logic Script
Here is a simple logic script to initialize and display text:

1. Add the `When [Board] starts up` hat block.
2. Add `initialize LCD at address 0x27`.
3. Add `clear LCD`.
4. Add `print [Hello SprouT!] on LCD line 1 position 1`.

---

## Troubleshooting

* **Screen Displays Blank / White Blocks:** Adjust the small blue contrast potentiometer on the back of the I2C board using a screwdriver until characters become visible.
* **No Text Appearing:** Verify if the I2C address in your code matches your module (usually `0x27` or `0x3F`).