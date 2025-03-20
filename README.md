# Amphibious Bot with Pick and Place Mechanism

This project demonstrates an **Amphibious Bot** equipped with a **pick and place mechanism**, controlled by an **Arduino Uno**. The bot uses a **custom-made controller** for navigation and manipulation tasks, and communicates wirelessly via **NRF modules** for data transmission and reception. The bot is capable of moving on both land and water, making it versatile for various environments.

## Features

- **Amphibious Design**: The bot can operate both on land and water, thanks to its specialized design and motor configuration.
- **Pick and Place Mechanism**: A mechanical arm is integrated into the bot, allowing it to pick up and place objects autonomously.
- **Wireless Control with NRF Modules**: The bot communicates with a custom controller using NRF modules, allowing for wireless data transmission and reception.
- **Arduino Uno**: The heart of the bot's control system is an **Arduino Uno**, used for processing signals and controlling the motors and actuators.

## Requirements

### Hardware

- **Amphibious Bot Chassis**: Custom-built or commercially available amphibious chassis.
- **Arduino Uno**: Used to control the bot and pick-and-place mechanism.
- **NRF24L01 Modules (x2)**: Wireless communication between the bot and the controller.
- **Motor Driver**: For controlling the motors of the bot (e.g., L298N or similar).
- **DC Motors (x4)**: For driving the bot on land and water.
- **Servos (x2)**: For the pick and place mechanism.
- **Battery**: A rechargeable battery to power the bot (e.g., LiPo or NiMH).
- **Custom-built Controller**: A separate controller unit for wireless communication with the bot.

### Software

- **Arduino IDE**: The development environment used for programming the Arduino Uno and the controller.
- **NRF24L01 Library**: Used for communication via the NRF modules.

## Installation

### 1. Hardware Setup

1. **Bot Assembly**:
   - Assemble the **amphibious chassis**, ensuring the motors are connected to the wheels (for land movement) and propellers (for water movement).
   - Attach the **servo motors** for the pick-and-place mechanism, ensuring they can move the arm for picking and placing objects.
   - Connect the **motor driver** to the **DC motors**, and make sure the power supply is properly connected.

2. **Wiring the NRF Modules**:
   - Connect one NRF24L01 module to the **Arduino Uno** on the bot, and the second one to your custom controller.
   - The wiring is as follows (based on the typical wiring for NRF24L01):
     - **VCC** to 3.3V (do not use 5V as it may damage the module)
     - **GND** to ground
     - **CE** to a chosen digital pin (e.g., D9)
     - **CSN** to another digital pin (e.g., D10)
     - **SCK** to pin D13
     - **MOSI** to pin D11
     - **MISO** to pin D12

3. **Pick and Place Mechanism**:
   - The arm is controlled by **two servos** to pick up and place objects. Connect these servos to PWM pins on the Arduino (e.g., D5 and D6).

4. **Power**:
   - Power the Arduino Uno and the motors/servos using a rechargeable battery. Ensure the voltage levels are compatible with your components.

### 2. Software Setup

1. **Install Libraries**:
   - Open the Arduino IDE and install the required libraries:
     - **NRF24L01 Library** for communication.
     - **Servo Library** for controlling the servos.

2. **Arduino Code**:
   - Clone or download the repository.
   - Open the Arduino IDE and load the sketch for the bot onto the **Arduino Uno**.
   - Similarly, load the custom controller sketch onto the second Arduino (or other controller device).

3. **Upload Code**:
   - Select the correct board (Arduino Uno) and port from the `Tools` menu.
   - Upload the code for both the **Bot** and **Controller** to their respective devices.

### 3. Custom Controller

The custom-built controller uses the **NRF24L01 module** to send control commands to the bot. It typically has buttons or joysticks to control movement and the pick-and-place mechanism.

## Usage

1. **Power On**:
   - Turn on the **bot** and the **controller** by supplying power via batteries.
   
2. **Controller Commands**:
   - Use the custom controller to send movement commands (e.g., forward, backward, left, right) to the bot via NRF24L01 modules.
   - Use dedicated buttons or joysticks to control the **pick and place mechanism**.
   
3. **Bot Movement**:
   - The bot can move on **land** using its DC motors and wheels.
   - For **water navigation**, use the **propellers** that are controlled by the same motor driver.
   
4. **Pick and Place**:
   - The bot’s arm can be controlled to **pick up** or **place** objects using the servos based on commands from the controller.

## Acknowledgments

- **Arduino**: For the incredible microcontroller platform used for prototyping.
- **NRF24L01**: For enabling wireless communication between the bot and the controller.
- **Servo Library**: For simplifying the control of the servos in the pick-and-place mechanism.
- **Open-Source Communities**: For providing inspiration, libraries, and solutions that helped build this project.

