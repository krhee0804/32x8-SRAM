# SRAM Memory System Design

This repository contains the implementation of a 32x8 (256-bit) **SRAM Memory System** designed as part of the *Digital Integrated Circuits Term Project*.

## Project Overview
The project involves designing and simulating a complete SRAM memory system, including its peripheral circuits, schematic, layout, and post-simulation analysis. The goal was to meet the specifications of a 250 MHz operational frequency and transition times under 0.2 ns, while optimizing the layout for improved Figure of Merit (FoM).

## Key Features
- **Peripheral Circuit Design**:
  - Bitline Precharger
  - Write Driver
  - Read Sense Amplifier
  - Word Line Decoder
  - Word Line Driver
- **System Design**:
  - 32x8 SRAM Cell Array
  - Fully integrated layout with matched schematic
- **Simulation Results**:
  - Writing and reading data within 0.2 ns transition time
  - Functional verification at 250 MHz clock frequency
- **Optimization**:
  - Compact layout design
  - Measured FoM: 1.845 × 10⁹ / J·(μm)²

## Schematic Design
The schematic for each peripheral circuit was carefully designed to meet the stringent timing requirements. Each component was tested with proper testbenches to validate performance.

## Layout Design
- The layout was implemented following DRC and LVS rules.
- Optimization focused on aligning peripheral circuits with the SRAM cell array to minimize area and improve performance.
- Post-simulation results confirmed that the layout meets all design specifications.

## Simulation Details
- A 20 ns simulation was conducted with a 4 ns clock cycle.
- Write operations:
  - Address `11111`: Data `10101010` at 4 ns
  - Address `00000`: Data `01010101` at 8 ns
- Read operations:
  - Address `11111`: At 12 ns
  - Address `00000`: At 16 ns
- Precharging, enabling word lines, and sense amplifiers were precisely timed for each cycle.

## Analysis and Limitations
- **FoM Calculation**:
  - Power consumption averaged over two clock cycles: 106.36 μW
  - Total layout area: 1273.8 μm²
- **Limitations**:
  - Empty spaces in the layout limited further area reduction.
  - Routing optimization could improve parasitic characteristics for faster operation.

## Conclusion
The designed SRAM system successfully meets all required specifications, demonstrating robust functionality for both read and write operations at 250 MHz. Future improvements could include further layout optimization and rule-compliant routing for reduced parasitic effects.

## File Structure
- **`/schematics`**: Schematic files for all peripheral circuits.
- **`/layouts`**: Layout designs with DRC/LVS checks.
- **`/simulations`**: Pre- and post-layout simulation results.
- **`README.md`**: This file.
