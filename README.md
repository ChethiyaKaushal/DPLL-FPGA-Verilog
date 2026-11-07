# DPLL FPGA Implementation Using Verilog HDL

## Overview

This project focuses on the design, simulation, and FPGA implementation of a Digital Phase-Locked Loop (DPLL) using Verilog HDL on the Digilent Nexys A7 development board.

The DPLL synchronizes a digitally generated output signal with an external reference clock by continuously measuring phase differences and adjusting the output frequency through a closed-loop feedback system.

## Objectives

- Design a modular Digital Phase-Locked Loop using Verilog HDL.
- Implement an input synchronizer and digital phase detector.
- Develop a digital Proportional–Integral (PI) loop filter.
- Implement a 32-bit Numerically Controlled Oscillator (NCO).
- Detect phase-lock conditions using a lock detector.
- Simulate and verify individual modules and the complete system.
- Implement and validate the design on the Nexys A7 FPGA.

## Hardware and Software

**Hardware**
- Digilent Nexys A7 FPGA development board
- Function generator
- Jumper wires and suitable connectors
- Oscilloscope or logic analyzer for hardware verification

**Software**
- Verilog HDL
- AMD Vivado Design Suite
- Icarus Verilog
- GTKWave
- Visual Studio Code

## Initial Design Specifications

| Parameter | Target |
|---|---|
| FPGA system clock | 100 MHz |
| External reference | 1 MHz |
| NCO output | Approximately 1 MHz |
| NCO accumulator | 32 bits |
| Initial frequency control word | 42,949,673 |

## System Architecture

External Reference → Input Synchronizer → Phase Detector → PI Loop Filter → NCO → Output

The NCO output is fed back to the phase detector, forming a closed-loop control system.

A separate lock detector monitors synchronization status.

## Project Structure

- `rtl/` — Synthesizable Verilog modules
- `testbench/` — Verilog simulation testbenches
- `simulation/` — Simulation-related files
- `constraints/` — FPGA pin and timing constraints
- `docs/` — Architecture and project documentation

## Development Status

The project is currently in the initial design and module implementation stage.

Planned development includes individual module verification, full DPLL integration, closed-loop testing, FPGA synthesis, and hardware validation.

## Expected Outcome

A working FPGA-based DPLL capable of tracking an external reference signal and producing a synchronized digital output, with observable lock status.

## Author

Chethiya Kaushal

University of Ruhuna — Faculty of Engineering
