# Operational Transconductance Amplifier (OTA) Design Project

## Overview

The **Operational Transconductance Amplifier (OTA) Design Project** focuses on the design, simulation, and analysis of a high-performance OTA in the analog domain. OTAs are fundamental building blocks in analog signal processing, used in a wide range of applications such as filters, oscillators, and analog multipliers.

This project uses **Cadence Virtuoso** as the primary design tool and leverages the **GPDK90 technology**. The goal is to design an OTA that meets stringent performance criteria, suitable for integration in various analog circuits.

## Design Specifications

- **Voltage Gain**: 70 V/V
- **Load Capacitance**: 10 pF
- **Input Common Mode Range (ICMR+)**: 1.6 V
- **Input Common Mode Range (ICMR-)**: 0.8 V
- **Output Swing**: 1 Vpp
- **Power Dissipation**: ≤ 100 µW
- **Slew Rate**: ≥ 5 V/µs
- **Gain Bandwidth Product (GBW)**: ≥ 5 MHz
- **Transistor Length**: 0.5 µm

## Features

- **High Transconductance**: Designed to achieve a high transconductance to enhance performance in analog signal processing applications.
- **Low Power Consumption**: The design ensures minimal power usage, making it suitable for battery-powered devices.
- **Linearity**: Excellent linearity is maintained to reduce distortion in the processed signals.
- **Process Technology**: Implemented using GPDK90 technology, with each transistor having a length of 0.5 µm.

## Project Structure

- **/design**: Contains the schematic and layout design files developed using Cadence Virtuoso.
- **/simulation**: Includes simulation scripts, test benches, and results.
- **/docs**: Documentation detailing the design process, simulation results, and analysis.
- **/reports**: Final reports and presentations summarizing the project outcomes.

## Tools and Technologies

- **EDA Tool**: Cadence Virtuoso
- **Process Technology**: GPDK90

## Getting Started

1. **Clone the Repository**: Clone the project repository to your local machine using the command:
   ```bash
   git clone https://github.com/yourusername/OTA-Design-Project.git
