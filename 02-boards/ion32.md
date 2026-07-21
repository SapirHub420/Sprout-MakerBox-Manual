# SprouT Base Board for ION32

The ION32 is a powerful processing board designed for high-speed execution and advanced robotics projects. When paired with the SprouT Base Board for ION32, it provides a robust, plug-and-play platform for modular prototyping.

<p align="center">
  <img src="../images/PNG - TOP - SprouT - SENANG - Base Board for ION32 - SprouT ION32 on Top.png" alt="SprouT Base Board for ION32" width="300">
</p>

---

## Technical Specifications

### Microcontroller Specifications
* Microcontroller: ION32 Architecture
* Operating Voltage: 3.3V / 5V dual-rail logic
* Digital I/O Pins: Multi-function configurable pins
* Port 22 Capabilities: Switchable between I2C communication and standard Digital I/O

---

## Base Board Custom Features

### 1. Plug-and-Play Module Ports
* Connects sensors and outputs using keyed, modular cables to prevent miswiring.
* Eliminates the need for breadboards and jumper wires.

### 2. Dedicated 5V Servo Pins
* Integrated 3-pin headers (Signal, 5V Power, Ground) for direct connection of servo motors.
* Delivers a stable 5V output supply across all servo headers.

### 3. Port 22 Pinmode Switch (I2C / I/O Mode)
* Features a physical toggle switch designated for Port 22.
* Allows quick toggling between I2C protocol communication (for screens/sensors) and standard Digital I/O pin functionality without altering hardware wiring.

### 4. Dual Power Terminal Blocks
* **7-12V DC Input Terminal Block:** Accepts external power inputs between 7V and 12V DC to drive heavy power configurations.
* **5V Input/Output Terminal Block:** Provides dual functionality; it can act as a direct 5V regulated input source or output a 5V supply to power auxiliary external hardware.

---

## Safety Guidelines

Ensure external power feeds are connected to the correct terminal block. Do not connect higher voltage sources (e.g., 7-12V) into the dedicated 5V terminal block to avoid permanent damage to the board logic.