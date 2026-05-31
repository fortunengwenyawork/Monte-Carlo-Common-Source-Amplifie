# Monte Carlo Common Source Amplifier

## Overview

This repository contains the complete design, simulation, and statistical verification of a BS170 Common-Source MOSFET Amplifier developed using LTspice.

The project investigates amplifier biasing, small-signal amplification behavior, transient response, and component tolerance sensitivity through Monte Carlo simulation techniques. Statistical analysis was performed using 100 simulation runs with ±5% resistor variation to evaluate design robustness under realistic manufacturing conditions.

---

## Objectives

- Design a Common-Source MOSFET amplifier using a BS170 transistor.
- Establish a stable DC operating point.
- Analyze transient response characteristics.
- Evaluate small-signal amplification behavior.
- Perform Monte Carlo analysis to assess component tolerance sensitivity.
- Quantify performance variability under manufacturing uncertainties.

---

## Circuit Specifications

| Parameter | Value |
|------------|---------|
| Supply Voltage | 12 V |
| MOSFET | BS170 |
| Drain Resistor | 4.7 kΩ |
| Source Resistor | 1 kΩ |
| Gate Bias Network | 1 MΩ / 1 MΩ |
| Load Resistor | 100 kΩ |
| Input Signal | 100 mV Peak, 1 kHz |

---

## Simulation Types

### DC Operating Point Analysis

Determines quiescent operating conditions and verifies transistor biasing.

### Transient Analysis

Evaluates time-domain amplifier response.

### Monte Carlo Analysis

100 simulation runs performed using ±5% resistor tolerance variation.

---

## Key Results

- Stable MOSFET bias point achieved.
- Consistent small-signal amplification observed.
- Statistical output spread quantified through Monte Carlo analysis.
- Circuit demonstrates tolerance robustness under realistic component variation.

---

## Repository Structure

```text
LTspice/         -> LTspice simulation files
Images/          -> Simulation screenshots
Reports/         -> Formal engineering report
Documentation/   -> Design notes and calculations
```

---

## Tools Used

- LTspice XVII
- Statistical Monte Carlo Analysis
- Analog Circuit Design Techniques
- MOSFET Small-Signal Theory

---

## Author

Fortune Ngwenya

Electrical Engineering Portfolio Project
