
# Monte Carlo Analysis of a Common-Source MOSFET Amplifier

## Overview

This project presents the design, simulation, and statistical analysis of a Common-Source MOSFET amplifier using LTspice. The objective was to evaluate amplifier performance under realistic component tolerances through Monte Carlo simulation techniques.

The study investigates how resistor variations influence operating point stability, output voltage, drain current, and small-signal gain. By performing 100 Monte Carlo simulation runs with ±5% component tolerance, the robustness and sensitivity of the amplifier design were quantified.

---

## Project Objectives

- Design a Common-Source MOSFET amplifier using a BS170 transistor.
- Establish a stable DC operating point through resistive biasing.
- Analyze AC signal amplification behavior.
- Evaluate circuit sensitivity to manufacturing tolerances.
- Perform statistical Monte Carlo analysis using LTspice.
- Document performance variations across multiple simulation runs.

---

## Circuit Specifications

| Parameter | Value |
|------------|----------|
| Supply Voltage (VDD) | 12 V |
| MOSFET | BS170 |
| Drain Resistor (RD) | 4.7 kΩ |
| Source Resistor (RS) | 1 kΩ |
| Gate Bias Resistors | 1 MΩ / 1 MΩ |
| Load Resistor (RL) | 100 kΩ |
| Input Capacitor | 10 µF |
| Output Capacitor | 10 µF |
| Source Bypass Capacitor | 100 µF |
| Input Signal | 100 mV, 1 kHz |

---

## Monte Carlo Configuration

The following LTspice directives were used:

```spice
.param tol=0.05
.step param run 1 100 1
.tran 20m
```

Component tolerances were modeled using:

```spice
{mc(4.7k,tol)}
{mc(1k,tol)}
{mc(1Meg,tol)}
{mc(100k,tol)}
```

This generated 100 unique circuit instances representing realistic manufacturing variation.

---

## Simulations Performed

### 1. DC Operating Point Analysis
Determined MOSFET bias conditions and quiescent operating point.

### 2. Transient Analysis
Evaluated amplifier response to a 1 kHz sinusoidal input.

### 3. Output Voltage Analysis
Measured amplified output signal behavior.

### 4. Drain Current Analysis
Observed current variation through the drain resistor.

### 5. Monte Carlo Statistical Analysis
Compared performance across 100 tolerance runs.

---

## Results Summary

### Output Voltage

The amplifier maintained stable operation across all Monte Carlo iterations. Output voltage variation remained within expected tolerance limits while preserving signal integrity.

### Drain Current

Drain current showed minor variations resulting from resistor tolerance effects. The bias network successfully maintained transistor operation in the desired region.

### Gain Stability

Despite component variation, amplifier gain remained highly consistent, demonstrating robust design margins.

### Sensitivity Findings

The largest contributors to variation were:

- Drain resistor tolerance
- Source resistor tolerance
- Gate bias network tolerances

The circuit exhibited excellent tolerance immunity and predictable behavior.

---

## Key Engineering Skills Demonstrated

- Analog Circuit Design
- MOSFET Biasing Techniques
- LTspice Simulation
- Statistical Monte Carlo Analysis
- Sensitivity Analysis
- Signal Integrity Evaluation
- Data Interpretation
- Engineering Documentation
- Design Verification
- Tolerance Modeling

---

## Repository Structure

```text
Monte-Carlo-Common-Source-Amplifier
│
├── LTspice
│   └── CommonSourceAmplifier.asc
│
├── Reports
│   └── Monte_Carlo_Common_Source_Amplifier_Report.pdf
│
├── Images
│   ├── Circuit_Schematic.png
│   ├── Output_Voltage.png
│   ├── Input_Signal.png
│   ├── Drain_Current.png
│   ├── MonteCarlo_Output.png
│   └── MonteCarlo_Input.png
│
└── README.md
```

---

## Software Used

- LTspice XVII
- GitHub
- Microsoft Word / PDF Documentation Tools

---

## Author

**Fortune Ngwenya**

This project demonstrates the application of statistical simulation techniques to analog circuit verification, providing insight into real-world manufacturing variability and design robustness.
