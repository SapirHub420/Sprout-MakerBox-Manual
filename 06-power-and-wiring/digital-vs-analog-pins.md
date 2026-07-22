# Digital vs Analog Pins Guide

Understanding the functional difference between Digital and Analog pins is essential for properly wiring components to your SprouT Base Board and writing accurate control logic.

---

## Technical Overview

Microcontrollers interpret physical signals in two primary ways: discrete state signals (Digital) and continuous variable signals (Analog).

| Feature | Digital Pins | Analog Pins |
| :--- | :--- | :--- |
| **Signal Type** | Binary (Discrete) | Continuous (Variable) |
| **States / Values** | 2 States: HIGH (1) or LOW (0) | 1024 Values: Range from 0 to 1023 |
| **Voltage Level** | 0V or 5V (or 3.3V depending on microchip) | Variable voltage from 0V up to VCC (5V) |
| **Primary Use** | Buttons, switches, relays, standard LEDs | Potentiometers, light sensors, gas sensors |
| **Read/Write Capability** | Digital Read & Digital Write | Analog Read (and PWM Output on select pins) |

---

## Digital Pins

Digital pins process discrete binary logic. They can operate in two modes:

1. **Digital Input:** Reads binary states from external components.
   * **HIGH (1):** Signal voltage detected (e.g., button pressed).
   * **LOW (0):** Ground / no voltage detected (e.g., button released).
2. **Digital Output:** Delivers binary power states to external components.
   * **HIGH:** Supplies full operating voltage to power an output (e.g., turn LED ON).
   * **LOW:** Connects pin to 0V ground (e.g., turn LED OFF).

### Pulse Width Modulation (PWM)
Certain digital pins (indicated with a `~` symbol or marked PWM) can simulate an analog output using rapid square wave pulses. This allows control over LED brightness levels or motor rotation speeds by varying duty cycles from `0` (0% power) to `255` (100% power).

---

## Analog Pins

Analog pins measure smooth, continuous electrical changes from input sensors.

1. **Analog-to-Digital Converter (ADC):**
   * SprouT base boards feature an internal 10-bit Analog-to-Digital Converter (ADC).
   * The ADC maps measured input voltages between 0V and 5V into integer values from **0** to **1023**.
2. **Voltage Resolution:**
   * Each integer step represents approximately **4.88 mV** ($5\text{V} / 1024$).

> **Important Usage Rule:** Analog input pins can be used as standard Digital input/output pins if needed, but Digital pins cannot perform true continuous Analog input readings.

---

## Selection Matrix

Use this quick guide to choose the correct pin type on your SprouT Base Board:

* **Use Digital Pins for:**
  * Push Buttons
  * Tactile switches
  * Infrared obstacle detectors
  * Vibration sensors
  * Single-color LEDs
  * Tone buzzers
  * Relays
* **Use Analog Pins for:**
  * Potentiometers / rotary knobs
  * LDR Light sensors
  * Gas and air quality sensors
  * Sound level sensors