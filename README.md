# RFID Security System with Door Locking - Arduino Project

Radio Frequency Identification (RFID) Security System is a low-cost technology-based project aimed at creating an efficient access control and security solution. This project utilizes passive RFID technology to develop a security system for restricted areas where only authorized individuals are allowed access. The system provides real-time user verification and door unlocking capabilities using an RFID tag.

## Overview

The main objective of this project is to design and deploy a secure access control system that grants access to authorized personnel only. By utilizing passive RFID technology, the system allows users to gain entry by presenting an RFID tag close to the RFID reader. Upon successful verification, the door lock mechanism operates in real-time, unlocking the door for authorized access. The system includes an RFID reader as an input device, an LED for visual feedback, and a servo motor for door locking/unlocking.

## Theory

The RFID reader used in this project is the MFRC-522, a two-way radio transmitter-receiver reader. It communicates with an Arduino microcontroller using SPI (Serial Peripheral Interface) communication. The pins of the MFRC-522 are connected as follows:

SDA: Digital 10
SCK: Digital 13
MOSI: Digital 11
MISO: Digital 12
IRQ: Unconnected
GND: GND
RST: Digital 9
3.3V: 3.3V
For the door locking mechanism, a servo motor is used, which is connected to digital pin 2 of the Arduino board. When a valid RFID tag is scanned, the servo motor rotates about 90 degrees, unlocking the lock on the box. After a brief delay of 10 seconds, the servo motor returns to its original position, allowing the user to manually lock the box again. Additionally, an LED connected to digital pin 2 provides visual indication to the user when the lock is open.

## Components

The project requires the following components:

1. Arduino board (e.g., Arduino Uno)
2. MFRC-522 RFID reader module
3. Passive RFID cards or tags
4. Servo motor
5. LED
6. Jumper wires
7. Breadboard
8. Small box (for demonstration purposes)

## Setup and Installation

1. Connect the MFRC-522 RFID reader module to the Arduino board according to the pin configuration mentioned in the Theory section.

2. Connect the servo motor to digital pin 2 of the Arduino board.

3. Connect an LED to digital pin 2 for visual feedback.

4. Make sure the Arduino IDE is installed on your computer.

5. Clone or download this project repository to your local machine.

6. Open the Arduino IDE and load the project's Arduino sketch (.ino) file.

7. Connect your Arduino board to your computer via USB, select the correct board and port from the Arduino IDE.

8. Upload the sketch to the Arduino board.

## Usage

1. Ensure that the RFID reader and the components are set up correctly and the Arduino board is powered on.

2. Place the RFID tag or card near the RFID reader.

3. The RFID reader will read the tag and send the signal to the Arduino.

4. The Arduino will verify the legitimacy of the RFID card.

5. If the RFID card is valid, the LED will blink, and the servo motor will unlock the door, displaying "Authorized Access" on the serial monitor.

6. If the RFID card is invalid, "Access Denied" will be displayed on the serial monitor, and no output will be generated.

7. After 10 seconds, the servo motor will return to its original position, and the user can manually lock the box again.
