# Bluetooth Module Guide

The **Bluetooth Module** is a wireless communication input/output component that allows your SprouT board to send and receive data wirelessly over short distances using Bluetooth protocols. It enables remote control via smartphones, tablets, or computers.

<p align="center">
  <img src="../images/PNG - TOP - SprouT - SENANG - Bluetooth Transceiver MLT-BT05.png" alt="Bluetooth Module" width="300">
</p>

---

## How It Works

* **Type:** Wireless Communication Module (Serial Input/Output)
* **Function:** Transmits and receives data using Universal Asynchronous Receiver-Transmitter (UART) communication to enable wireless control and telemetry.
* **Signal Output:** 
  * **TX / RX Serial Streams:** Transmits incoming wireless characters/commands as serial data bytes to the microcontroller board.

---

## Connection Setup

1. Take your **SprouT Base Board** and plug in your central controller microchip.
2. Connect one end of the modular cable to the **Bluetooth Module**.
3. Plug the other end of the cable into the designated **Serial / TX-RX Communication Port** on your SprouT Base Board.
4. Plug the USB cable into your board and connect it to your computer.

> **Safety Tip:** Always plug in your hardware components before powering on your board via USB!

---

## PictoBlox Programming Guide

### 1. Board & Mode Setup
* Open **PictoBlox**.
* Set your board to **[Arduino Nano / ION32 / Micro:bit]** in the top toolbar.
* Select **Upload Mode** (or **Stage Mode** for real-time testing).

### 2. Required Code Blocks
Look for the following block in the **Dabble / Bluetooth Extension** palette:

* `get data from Bluetooth`
* `read Bluetooth data`

### 3. Example Logic Script
Here is a simple logic script to process incoming wireless commands:

1. Add the `When [Board] starts up` hat block.
2. Add the `initialize Bluetooth at baud rate [9600]` block.
3. Attach a `forever` loop.
4. Inside the loop, add an `if ... then` condition:
   * **Condition:** If `Bluetooth data available`
   * **Action:** Perform specific hardware actions based on received command values.

---

## Troubleshooting

* **Pairing Failed:** Ensure your mobile device's Bluetooth is enabled and the module's status LED is blinking (indicating it is ready to pair).
* **No Serial Connection:** Verify that TX and RX lines are connected correctly (TX to RX, RX to TX) and that the baud rate matches your code settings.