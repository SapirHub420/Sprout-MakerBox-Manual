# Program Arduino Board with PictoBlox

## Blink Arduino Pin 13 LED

### Description
In this lesson, you will learn how to use PictoBlox to program an Arduino board and create a script to make the Pin 13 LED blink. You will also learn about the UI elements of PictoBlox, its two working modes, and how to interface an Arduino board with PictoBlox.

* **Software Used:** PictoBlox
* **Difficulty Level:** Beginners
* **Category:** Arduino, Tutorial

---

## Introduction

Most of you must be familiar with Arduino and how to program it using conventional syntax-based programming languages. You might even know how complicated it can be to remember multiple lines of code just to make an LED blink. 

That is where Scratch comes into the picture—it is a graphical programming language that lets you write code by dragging and dropping blocks instead of typing them out. However, Scratch cannot directly control hardware out of the box. 

This is where **PictoBlox** comes to the rescue. PictoBlox is a Scratch 3.0-based programming software designed to bridge graphical block-based coding with physical microcontrollers.

In this tutorial, we will briefly review the UI elements of PictoBlox, its two working modes, how to interface an Arduino board with PictoBlox, and run a small activity to make the built-in Pin 13 LED blink.

---

## Installing PictoBlox

Choose your appropriate Operating System (Windows, macOS, Linux) and download PictoBlox from the official download center.

---

## Understanding the UI of PictoBlox

Just like the Scratch interface, PictoBlox includes the following basic core elements:

1. **Sprite:** The Sprite is a character or object that performs actions according to your project scripts. Technically, a sprite is the visual face of your project on the screen. In PictoBlox, **Tobi the bear** is your primary coding buddy. You can change or add new sprites at any time.
2. **Stage:** The stage is the area on screen where your sprite performs actions. The background image is known as the **Backdrop**. You can select backdrops from the library, draw your own, or upload an image file.
3. **Block:** Blocks are the fundamental elements of block coding. You drag and drop blocks into the scripting area to build logic, eliminating syntax errors entirely.
4. **Script & Scripting Area:** A script is your actual program composed of snapped-together blocks. You assemble and edit your blocks inside the **Scripting Area**.
5. **Mode:** PictoBlox offers two distinct working modes:
   * **Stage Mode:** Write scripts for sprites and boards (like Arduino, evive, etc.) to interact in real time with on-screen sprites. If the board is disconnected, real-time interaction stops.
   * **Upload Mode:** Write scripts and compile them directly onto the board's onboard chip memory so that the board can run autonomously without remaining connected to the computer.

---

## Interfacing Arduino to PictoBlox

To run scripts written in PictoBlox on your board, follow these steps to connect and configure your hardware:

1. Connect your board to your computer via USB cable and launch **PictoBlox**.
2. Navigate to the top navigation toolbar and click on the **Board** menu.
3. Select your microcontroller target (e.g., **Arduino Uno / Nano**).
4. Once selected, relevant block extensions (Actuators, Sensors, Display, etc.) will load into the Block Palette. If they do not appear automatically, click the purple **Add Extension** button in the bottom-left corner.
5. Click on the **Connect** menu on the top toolbar. From the drop-down menu, select the active Serial Port corresponding to your connected board (e.g., `COMXX` on Windows or `ttyXX` on macOS/Linux).
6. Once connected, the plug icon next to the **Connect** menu will display a green connected status.

---

## Activity: Make the Pin 13 LED Blink

### Step 1: Add the Digital Output Block
To control the LED on Pin 13, locate and drag out the block:
`set digital pin (13) output (HIGH)`

### Step 2: Set the LOW State
Right-click on the block to duplicate it. Change the second block's output state to `LOW`:
`set digital pin (13) output (LOW)`

### Step 3: Add Timing Delays
To control the speed of the blinking, open the **Control** palette and drag out two `wait (1) seconds` blocks. Place one wait block directly under each `set digital pin` block.

> **Reference Animation/GIF:**
> <p align="center">
>   <img src="https://ai.thestempedia.com/wp-content/uploads/2020/03/Duplicate.gif" alt="Duplicate and Wait Blocks" width="300">
> </p>

### Step 4: Stack the Sequence
Stack the blocks vertically in this order:
1. `set digital pin (13) output (HIGH)`
2. `wait (1) seconds`
3. `set digital pin (13) output (LOW)`
4. `wait (1) seconds`

> *Note: Without a loop, this script will execute only once—turning the LED ON, waiting 1 second, turning it OFF, and stopping.*

> **Reference Animation/GIF:**
> <p align="center">
>   <img src="https://ai.thestempedia.com/wp-content/uploads/2020/03/Stack-Together.gif" alt="Stack Together Blocks" width="300">
> </p>

### Step 5: Loop the Execution
To make the LED blink continuously, grab a `forever` block from the **Control** palette and wrap it around the block sequence you just created.

> **Reference Animation/GIF:**
> <p align="center">
>   <img src="https://ai.thestempedia.com/wp-content/uploads/2020/03/forever-block.gif" alt="Forever Block" width="300">
> </p>

### Step 6: Add the Startup Hat Block
Top your script with the startup hat block from the board palette:
`When Arduino starts up`

> **Reference Animation/GIF:**
> <p align="center">
>   <img src="https://ai.thestempedia.com/wp-content/uploads/2020/03/Drag-the-Arduino-Starts-Up-hat-Block.gif" alt="Arduino Starts Up Hat Block" width="300">
> </p>

### Step 7: Upload to the Board
1. Toggle the mode switch at the top right from **Stage** mode to **Upload** mode.
2. The Stage area will be replaced by an editor pane displaying the automatically generated equivalent C++ code.
3. Click the **Upload Code** button.

> **Reference Animation/GIF:**
> <p align="center">
>   <img src="https://ai.thestempedia.com/wp-content/uploads/2020/03/Uploading.gif" alt="Uploading Code" width="300">
> </p>

Once the upload process reaches 100%, your board will begin executing the script and the Pin 13 LED will start blinking continuously!

---

## Summary & Conclusion

You have successfully learned the fundamentals of PictoBlox, navigated its primary user interface elements, learned the difference between Stage and Upload modes, and successfully created and uploaded an autonomous LED blink program to your microcontroller board.