Design Requirements

Project Overview

This project implements and validates a Common-Source MOSFET amplifier using LTspice. The design incorporates statistical Monte Carlo analysis to evaluate the impact of component tolerances on circuit performance and operating point stability.

Functional Requirements

Amplification

* Amplify a 1 kHz sinusoidal input signal.
* Maintain linear operation around the selected bias point.
* Demonstrate characteristic phase inversion of a Common-Source amplifier.

Bias Stability

* Establish a stable MOSFET operating point.
* Maintain transistor operation within the saturation region.
* Prevent cutoff or excessive conduction across expected component variations.

Statistical Verification

* Perform 100 Monte Carlo simulation runs.
* Apply ±5% resistor tolerances.
* Observe resulting variations in operating point and signal behavior.

Simulation Requirements

* DC Operating Point Analysis (.op)
* Transient Analysis (.tran)
* Monte Carlo Statistical Sweep (.step)

Hardware Parameters

Parameter	Value
VDD	12 V
MOSFET	BS170
RD	4.7 kΩ
RS	1 kΩ
RG1	1 MΩ
RG2	1 MΩ
RL	100 kΩ
Cin	10 µF
Cout	10 µF
CS	100 µF

Success Criteria

* Stable bias point achieved.
* Successful signal amplification observed.
* Consistent operation across 100 Monte Carlo runs.
* No simulation failures or unstable operating points.
