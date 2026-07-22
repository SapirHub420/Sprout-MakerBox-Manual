# Power Supply Guide

Providing clean, stable voltage to your SprouT system prevents unexpected resets, guarantees proper sensor accuracy, and protects hardware components from overvoltage damage.

---

## Power Specifications Summary

| Source Option | Input Voltage Range | Recommended Operating Range | Primary Application |
| :--- | :--- | :--- | :--- |
| **USB Power Port** | 5V DC ($\pm0.25\text{V}$) | 5V DC | Code uploading, logic testing, low-power components |
| **DC Barrel Jack** | 7V – 12V DC | 9V DC | High-power applications, DC motors, servos, relays |
| **Onboard Rail VCC** | 5V DC (Regulated) | 5V DC | Standard modular sensors and input components |

---

## Primary Power Methods

### 1. USB Cable Power (5V DC)
* **Source:** Computer USB ports, powered USB hubs, or 5V USB wall adapters.
* **Supply Current:** Typically limited to **500 mA** (USB 2.0) or **900 mA** (USB 3.0).
* **Best Used For:** 
  * Programming and debugging code.
  * Running basic input sensors, single LEDs, and low-power displays.
* **Limitation:** Insufficient for running multiple high-torque DC motors or servos simultaneously.

### 2. External DC Power Jack (7–12V DC)
* **Source:** 9V DC power adapters or external battery packs connected to the onboard barrel jack.
* **Voltage Regulation:** Onboard linear voltage regulators reduce incoming 7–12V DC down to a steady regulated 5V DC for internal logic.
* **Best Used For:** 
  * Autonomous mobile robots.
  * Projects utilizing DC motors, motor drivers, buzzers, and relay modules.

---

## Powering Base Boards

### SprouT Base Board Specifications
All SprouT base boards feature built-in protection and distribution rails to simplify component wiring:

* **Arduino Nano v3 Base Board:** Accepts 7–12V DC via external power input or 5V DC via mini-USB.
* **ION32 Base Board:** Supports 7–12V DC external power input, with onboard regulation providing dual 5V and 3.3V logic rails.
* **Micro:bit Base Board:** Accepts 7–12V DC external board power or 3.3V/5V regulated edge connector supply.

---

## Power Safety Guidelines

To ensure safe operation and prevent damage to hardware:

1. **Observe Polarity:** Verify positive ($+$) and negative ($-$ / GND) orientation before connecting external battery terminals.
2. **Never Exceed 12V DC:** Applying voltages higher than 12V DC directly to the external DC power jack will cause onboard linear regulators to overheat and fail.
3. **Isolate High Loads:** Never connect high-current loads (like motors) directly to 5V logic output pins. Always route heavy motor loads through a Motor Driver powered by external supply rails.
4. **Disconnect Power During Wiring:** Always unplug USB cables and external battery supplies before connecting or changing modular wiring leads.