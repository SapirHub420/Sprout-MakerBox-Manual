# SprouT Base Board for Arduino Nano v3

<p align="center">
  <img src="../images/PNG - TOP - SprouT - SENANG - Base Board for Arduino Nano - Nano on Top.png" width="300">
</p>

The Arduino Nano v3 is a compact, breadboard-friendly, and highly versatile microcontroller board based on the ATmega328P chip. When paired with the **SprouT Base Board for Arduino Nano**, it transforms from a complex mess of loose wires into a safe, clean, and modular plug-and-play electronics experience for makers.

---

## Key Features & Specifications

### Arduino Nano v3 Core Specs
* **Microcontroller:** ATmega328P 
* **Operating Voltage:** 5V
* **Digital I/O Pins:** 14 (with 6 providing PWM output for smooth motor and light control)
* **Analog Input Pins:** 8 (allowing multiple sensor readings simultaneously)
* **Flash Memory:** 32 KB (plenty of room for creative PictoBlox logic)
* **Clock Speed:** 16 MHz

---

## SprouT Base Board Custom Features

The custom SprouT Base Board acts as the "motherboard" for your Nano, adding critical physical enhancements designed to make learning electronics foolproof and fast.

### 1. Plug-and-Play Module Capability
No loose jumper wires, no messy breadboards, and zero soldering required! The base board breaks out the Nano's pins into dedicated, keyed plug-and-play connectors. 
* **Mistake-Proof Wiring:** Sensors and outputs only plug in the correct way, eliminating the risk of accidental short circuits or backward connections.
* **Rapid Prototyping:** Students can swap components (like changing a button for a light sensor) in under two seconds.

### 2. Dedicated Servo Motor Pins
Standard microcontroller boards struggle to power servo motors directly, often leading to board resets or glitches. The SprouT Base Board resolves this with dedicated servo connection rows:
* **Direct Header Rows:** Standard 3-pin servo motor cables (Signal, Power, Ground) plug straight into the board rows without extra adapters.
* **Stable Power Delivery:** The tracks are optimized to handle the physical current spikes drawn by active moving servo motors.

### 3. Flexible Power Inputs (7-12V DC)
While the board can run straight from your computer via a USB cable during programming, it is also equipped to operate completely untethered for mobile projects like robots!
* **Wide Voltage Range:** Features an onboard DC barrel jack/power port that safely accepts external voltages between **7V to 12V DC**.
* **Onboard Voltage Regulation:** A built-in regulator safely steps down incoming battery pack or wall-adapter voltages to the steady 5V required by the Nano and your connected sensors.

---

## Safety Quick-Tip

> ### Power Handling Check
> When using the **7-12V DC external power input**, always make sure your power supply adapter polarity matches the board configuration, and never plug in a power supply higher than 12V to avoid damaging the regulator chip!