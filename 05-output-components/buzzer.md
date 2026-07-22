# Tone Buzzer Guide

The **Tone Buzzer** is an output component that produces sound frequencies and audio alerts. It allows your SprouT board to provide auditory feedback, play musical tones, or sound alarms.

<p align="center">
  <img src="../images/PNG - TOP - SprouT - SENANG - Tone Buzzer.png" alt="Tone Buzzer" width="300">
</p>

---

## How It Works

* **Type:** Output Component (Digital / PWM)
* **Function:** Uses a piezoelectric element that vibrates rapidly when receiving electrical signals, creating sound waves at specified frequencies.
* **Signal Input:** 
  * **HIGH / LOW or PWM Frequency:** Digital HIGH turns the buzzer ON. Sending PWM frequencies generates specific musical notes and tones.

---

## Connection Setup

1. Take your **SprouT Base Board** and plug in your central controller microchip.
2. Connect one end of the modular cable to the **Tone Buzzer** module.
3. Plug the other end of the cable into a **Digital / PWM Port** (e.g., Digital Pin 8) on your SprouT Base Board.
4. Plug the USB cable into your board and connect it to your computer.

> **Safety Tip:** Always plug in your hardware components before powering on your board via USB!

---

## PictoBlox Programming Guide

### 1. Board & Mode Setup
* Open **PictoBlox**.
* Set your board to **[Arduino Nano / ION32 / Micro:bit]** in the top toolbar.
* Select **Upload Mode** (or **Stage Mode** for real-time testing).

### 2. Required Code Blocks
Look for the following block in the **Actuators / Sound** palette:

* `play tone on pin ( ) note ( ) for ( ) beats`
* `set digital pin ( ) output (HIGH/LOW)`

### 3. Example Logic Script
Here is a simple logic script to play a tone notification:

1. Add the `When [Board] starts up` hat block.
2. Attach a `forever` loop.
3. Inside the loop:
   * Play note `C4` on pin `8` for `1` beat.
   * Add a `wait (1) seconds` block.

---

## Troubleshooting

* **No Sound Output:** Verify the modular cable is fully inserted and that the selected pin in your blocks matches the physical digital port.
* **Distorted Audio:** Ensure the volume level or frequency is supported by the buzzer module and is not driven beyond standard operating voltage.