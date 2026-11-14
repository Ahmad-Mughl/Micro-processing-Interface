# Micro-processing-Interface
🗳️ Electronic Voting Machine (EVM) – PIC18F458 Assembly

📌 Project Overview

The Electronic Voting Machine (EVM) is an embedded systems project developed using Assembly Language for the PIC18F458 microcontroller.

The system allows users to cast votes for two candidates, Trump and Harris, using a keypad interface. It maintains separate vote counts for both candidates and displays their names and vote counts on a 16×2 LCD.

The project demonstrates the use of microcontroller interrupts, keypad input handling, LCD interfacing, timers, and Assembly Language programming.

✨ Features

Supports two candidates: Trump and Harris.

Maintains separate vote counters for both candidates.

Uses PORTB interrupt-on-change functionality for vote input detection.

Increments the corresponding candidate's vote count.

Provides a reset operation to clear both vote counters.

Displays candidate names and vote counts on an LCD.

Uses Timer0 to generate delays for LCD operations.

🛠️ Hardware and Software Requirements

Hardware

PIC18F458 Microcontroller

16×2 LCD Display

Keypad / Push-button input interface

Connecting wires

Microcontroller development board

Software

Assembly Language

MPLAB IDE / MPASM

PIC18F458 microcontroller support

⚙️ Working Principle

The system initializes the PIC18F458 ports, configures the keypad input pins, enables PORTB interrupt-on-change, and initializes the LCD.

The program uses three input conditions to control voting:

Input Pin

Operation

RB4

Increment Trump's vote count

RB5

Increment Harris's vote count

RB6

Reset both vote counts

Voting Process

The system initializes both vote counters to 0x30, representing ASCII character 0.

When the RB4 input condition is detected, Trump's vote count is incremented.

When the RB5 input condition is detected, Harris's vote count is incremented.

When the RB6 input condition is detected, both vote counters are reset to zero.

The LCD displays the candidate names and their respective vote counts.

🖥️ LCD Display

The LCD displays the two candidates and their vote counts.
The vote counts are stored as ASCII values to allow direct display on the LCD.

🧠 Assembly Language Concepts Used

Concept

Implementation

Interrupt Handling

PORTB interrupt-on-change

Timer0

Delay generation

Port Configuration

TRIS registers

Register Operations

MOVLW, MOVWF, MOVF

Bit Manipulation

BSF, BCF, BTFSS

Subroutines

CALL and RETURN

LCD Interfacing

LCD command and data routines

Counter Operations

INCF instruction

Program Control

GOTO and conditional branching
