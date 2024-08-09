# Operational Transconductance Amplifier (OTA) Design Project

## Overview

The **Operational Transconductance Amplifier (OTA) Design Project** focuses on the design, simulation, and analysis of a high-performance OTA.

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

## Shortcomings
- **Gain Specs not met**: 70 V/V(close to 37 dB) is a very high gain which could not be provided by this amplifier. This amplifier can generate a maximum gain of 48 V/V (33.59 dB) for ICMR- and 40V/V (32 dB) for ICMR+.
- **Phase Margin**: At this point, phase margin is not included in the design. It will be added soon.

## Project Structure

- **/design**: Contains the image(Amplifier.png) as well as the design files(schematic folder) of the schematic developed using Cadence Virtuoso.
- **/simulation**: Contains circuit diagram with dc operating points and gain plot without frequency sweep and 1Vpp input signal. (see Procedure.md)

## Tools and Technologies

- **EDA Tool**: Cadence Virtuoso
- **Process Technology**: GPDK90

## Getting Started

1. **Clone the Repository**: Clone the project repository to your local machine using the command:
   ```bash
   git clone https://github.com/yourusername/OTA-Design-Project.git
