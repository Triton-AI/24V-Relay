
# 24V MOSFET Switching Board — Triton AI

This repository contains the Altium Designer schematic and PCB design files for a 6-channel, 24V solid-state switching board developed for Triton AI, UC San Diego's autonomous racing team.

## Project Overview

The board was designed to replace an older mechanical-relay-based PCB used to control 24V electrical loads on our autonomous go-kart.

The new design uses MOSFETs to electronically switch the 24V supply to individual outputs based on digital control signals from a microcontroller.

### Key Features

- 6 independently controlled switching channels
- 24V supply and switched outputs
- N-channel and P-channel MOSFET high-side switching architecture
- Gate-to-source Zener diode protection
- Designed in Altium Designer

## How It Works

Each channel uses an N-channel MOSFET to control the gate voltage of a P-channel MOSFET.

When the microcontroller asserts the control signal, the N-channel MOSFET turns on and pulls the P-channel MOSFET's gate voltage lower than its source voltage, allowing the 24V supply to reach the output.

When the control signal is deasserted, the P-channel MOSFET turns off, disconnecting the supply from the load.

## Testing and Integration

After PCB fabrication, the board was assembled and tested using a DC bench power supply, microcontroller control signals, and a multimeter.

Functional testing verified the switching behavior of the channels before integration into the go-kart.

Three channels were integrated to control 24V status indicator lights corresponding to the vehicle's operating modes:

- **Red:** Emergency mode
- **Yellow:** Semi-autonomous mode
- **Green:** Autonomous mode

The board was successfully integrated and functionally tested with the vehicle's status indication system.

## Demonstration

https://youtube.com/shorts/ltIXgFceDX0

## Schematic

![24V MOSFET Switching Board Schematic](schematic.png)

## Assembled PCB

![Assembled switching PCB — View 1](IMG_2417.jpeg)

![Assembled switching PCB — View 2](IMG_2419.jpeg)
