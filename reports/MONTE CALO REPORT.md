Monte Carlo Tolerance Analysis of a Common-Source MOSFET Amplifier

Author: Fortune Ngwenya

⸻

Abstract

This project investigates the performance and robustness of a Common-Source MOSFET amplifier through statistical Monte Carlo simulation in LTspice. The amplifier was designed using a BS170 enhancement-mode MOSFET and biased using a resistive voltage-divider network. Component tolerances were incorporated to emulate real-world manufacturing variation and evaluate their impact on amplifier behavior.

A total of 100 simulation runs were performed with ±5% resistor tolerances. The resulting data demonstrates the circuit’s sensitivity to component variation while verifying stable operation across all tested conditions. The project combines analog circuit design, bias-point analysis, transient simulation, and statistical verification techniques commonly employed during electronic design validation.

⸻

Introduction

Analog circuits rarely operate with ideal component values. Manufacturing tolerances introduce unavoidable variations in resistor, capacitor, and semiconductor parameters. These variations can influence operating point stability, gain, output voltage swing, frequency response, and overall reliability.

To account for these effects, engineers frequently perform Monte Carlo simulations during the design process. Monte Carlo analysis generates multiple randomized versions of a circuit, allowing designers to evaluate expected performance distributions before physical prototyping.

The objective of this project was to design a Common-Source MOSFET amplifier and investigate how resistor tolerances influence amplifier behavior through statistical simulation.

⸻

Design Objectives

The primary goals of this project were:

• Design a functioning Common-Source MOSFET amplifier.

• Establish a stable DC operating point.

• Amplify a small AC input signal.

• Evaluate circuit sensitivity to resistor tolerances.

• Perform statistical Monte Carlo verification.

• Document the resulting variations in circuit performance.

⸻

Circuit Description

The amplifier consists of five major functional sections:

Power Supply

A 12 V DC source provides the operating voltage for the amplifier.

Gate Bias Network

Two 1 MΩ resistors form a voltage divider that establishes the MOSFET gate bias voltage.

Source Stabilization Network

A 1 kΩ source resistor provides negative feedback and operating point stabilization. A 100 μF bypass capacitor improves AC gain by reducing source degeneration at signal frequencies.

Drain Load

A 4.7 kΩ drain resistor converts drain current variations into output voltage variations, enabling voltage amplification.

Coupling Capacitors

Input and output capacitors isolate DC bias conditions while allowing AC signals to pass between stages.

⸻

Circuit Parameters

Supply Voltage (VDD): 12 V

MOSFET: BS170

Drain Resistor (RD): 4.7 kΩ

Source Resistor (RS): 1 kΩ

Gate Bias Resistors (RG1, RG2): 1 MΩ

Load Resistor (RL): 100 kΩ

Input Capacitor (Cin): 10 μF

Output Capacitor (Cout): 10 μF

Source Bypass Capacitor (CS): 100 μF

Input Signal: 100 mV Peak, 1 kHz Sine Wave

⸻

Theoretical Analysis

Gate Voltage

The gate voltage is established through the voltage divider:

VG = VDD × RG2 / (RG1 + RG2)

VG = 12 × 1 MΩ / (1 MΩ + 1 MΩ)

VG = 6 V

⸻

Source Voltage

The source resistor develops a voltage proportional to drain current:

VS = ID × RS

This creates negative feedback that stabilizes MOSFET operation.

⸻

Drain Voltage

The drain voltage is determined by:

VD = VDD − IDRD

A properly biased transistor places the drain near the middle of the supply range, maximizing available signal swing.

⸻

Small-Signal Voltage Gain

The approximate voltage gain is:

AV ≈ −gmRD

where gm represents MOSFET transconductance.

The negative sign indicates the characteristic 180-degree phase inversion of the Common-Source amplifier.

⸻

LTspice Implementation

The circuit was implemented and simulated using LTspice.

Simulation Commands

.tran 20m

.op

⸻

Monte Carlo Configuration

To simulate manufacturing variation, resistor values were modeled using LTspice’s Monte Carlo function.

Tolerance Definition

.param tol=0.05

⸻

Monte Carlo Sweep

.step param run 1 100 1

⸻

Randomized Components

RD = {mc(4.7k,tol)}

RS = {mc(1k,tol)}

RG1 = {mc(1Meg,tol)}

RG2 = {mc(1Meg,tol)}

RL = {mc(100k,tol)}

⸻

Simulation Results

DC Operating Point

The operating point analysis confirmed successful transistor biasing and stable circuit operation.

The MOSFET remained in its intended operating region throughout all simulation runs.

⸻

Output Voltage Analysis

The output voltage waveform exhibited stable amplification behavior with minimal variation across Monte Carlo iterations.

Measured output voltages clustered around approximately 2.1–2.3 V depending on the randomized resistor values.

The narrow distribution demonstrates robust bias-point stability.

⸻

Input Signal Analysis

The input waveform remained a clean 100 mV, 1 kHz sinusoid.

This served as a consistent excitation source for all simulations.

⸻

Drain Current Analysis

Drain current remained centered around approximately 2.1 mA.

Minor deviations were observed as resistor values varied.

These deviations are expected and represent realistic manufacturing effects.

⸻

Monte Carlo Overlay Analysis

The Monte Carlo overlays reveal how circuit performance changes across 100 randomized instances.

The observed spread in waveform amplitude demonstrates the influence of component tolerances on gain and operating point.

Despite these variations, the amplifier remained fully functional across all simulations.

No unstable operating points or catastrophic failures were observed.

⸻

Engineering Interpretation

The simulation results indicate that the design possesses strong tolerance immunity.

Key observations include:

• Stable DC operating point across all runs.

• Consistent drain current behavior.

• Predictable gain variation.

• Successful amplification under component variation.

• No evidence of bias collapse or transistor cutoff.

These characteristics suggest the design would perform reliably when implemented using commercially available components.

⸻

Practical Significance

Monte Carlo analysis is a critical verification technique used in professional analog design environments.

Applications include:

• Analog Integrated Circuit Design

• Mixed-Signal Verification

• Sensor Interface Design

• Power Electronics

• Automotive Electronics

• Aerospace Systems

• Reliability Engineering

This project demonstrates the ability to apply these verification methods within a practical analog amplifier design workflow.

⸻

Skills Demonstrated

Analog Circuit Design

MOSFET Biasing

Common-Source Amplifier Design

LTspice Simulation

DC Operating Point Analysis

Transient Analysis

Monte Carlo Simulation

Tolerance Modeling

Statistical Circuit Verification

Engineering Documentation

Waveform Interpretation

Design Validation

⸻

Conclusion

A Common-Source MOSFET amplifier was successfully designed, simulated, and statistically evaluated using LTspice. Monte Carlo analysis incorporating ±5% resistor tolerances verified stable operation across 100 randomized circuit instances.

The results demonstrate that the amplifier maintains a robust operating point, predictable gain characteristics, and reliable performance despite realistic component variation. This project illustrates a complete analog design verification workflow, combining theoretical analysis, simulation, statistical modeling, and engineering interpretation.

The methodology employed in this study reflects industry-standard approaches used to validate analog circuits prior to fabrication and deployment.
