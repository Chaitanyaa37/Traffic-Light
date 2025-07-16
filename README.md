# Traffic Light System Using 8051 Microcontroller

This project simulates a four-way traffic light control system using the 8051 microcontroller. The traffic lights are controlled via C code written for the Keil µVision IDE and compiled into a HEX file for uploading to the microcontroller.

# Project Overview

This traffic light controller manages traffic at a four-way intersection. It cycles through each direction with realistic timing for red, yellow, and green lights using delays.

# Microcontroller:
- AT89C51 / 8051 family

# Development Tools:
- Keil µVision IDE (.uvproj file)
- C language (.c file)
- HEX file for microcontroller programming (.hex file)

# Hardware Connections

Port mappings:
- P2.0–P2.2: Red, Yellow, Green for Direction 1
- P2.3–P2.5: Red, Yellow, Green for Direction 2
- P3.3–P3.5: Red, Yellow, Green for Direction 3
- P3.0–P3.2: Red, Yellow, Green for Direction 4

# Sequence Logic

Each direction gets a green signal for 45 units of time followed by a yellow for 5 units before turning red. The sequence then shifts to the next direction in a round-robin fashion.

# Files

| File Name              | Description                          |
|------------------------|--------------------------------------|
| `Traffic Light.c`      | Source code for traffic light logic |
| `Traffic Lights.hex`   | Compiled HEX file for 8051          |
| `Traffic Lights.uvproj`| Keil project file                    |

# How to Run

1. Open `Traffic Lights.uvproj` in Keil µVision.
2. Compile the project.
3. Load the `Traffic Lights.hex` into your 8051 microcontroller using any suitable programmer.
4. Connect LEDs to the appropriate pins as per the port mapping.
5. Power on the circuit to observe the traffic light sequencing.

# Notes

- The `delay()` function is software-based and not time-accurate for real-world systems. For real deployment, use a timer-based delay or RTOS.
- Timings can be adjusted in the `delay()` function.
