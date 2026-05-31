Results and Discussion

Overview

The objective of this project was to evaluate the performance and robustness of a Common-Source BS170 MOSFET amplifier through both conventional transient analysis and statistical Monte Carlo simulation. The amplifier was designed using a resistive voltage-divider bias network and evaluated under realistic manufacturing tolerances to determine its sensitivity to component variation.

A combination of DC operating point analysis, transient response evaluation, and 100-run Monte Carlo simulations was performed using LTspice.

⸻

DC Operating Point Results

The operating point analysis verified that the MOSFET was successfully biased in its intended operating region.

The voltage-divider network established a gate voltage of approximately 6 V, providing sufficient gate-to-source voltage to enable conduction through the BS170 transistor.

The source resistor developed a stable source voltage, creating negative feedback that improved operating point stability. The drain resistor converted drain current variations into output voltage variations, allowing voltage amplification to occur.

The operating point results demonstrated that the amplifier maintained a stable quiescent condition suitable for small-signal amplification.

Key Observations

* Stable gate bias voltage achieved.
* Consistent source voltage established through source degeneration.
* Drain current remained within the expected operating range.
* No evidence of transistor cutoff or excessive conduction.
* Operating point remained suitable for signal amplification.

⸻

Transient Response Analysis

Transient simulations were performed using a 100 mV, 1 kHz sinusoidal input signal.

The amplifier successfully reproduced and amplified the input waveform. The output exhibited the expected behavior of a Common-Source amplifier, including phase inversion between input and output signals.

The drain waveform demonstrated that small variations in gate voltage produced significantly larger voltage variations at the drain node. This behavior confirms proper transistor operation and validates the fundamental amplification mechanism of the circuit.

The coupling capacitors successfully blocked DC bias voltages while allowing the AC signal component to propagate through the circuit.

Key Observations

* Stable sinusoidal output obtained.
* Successful voltage amplification achieved.
* Expected phase inversion observed.
* No distortion or instability detected.
* Proper operation of coupling capacitors verified.

⸻

Drain Voltage Analysis

The drain voltage waveform provided insight into the amplification process occurring within the MOSFET.

As the gate voltage increased, drain current increased, producing a larger voltage drop across the drain resistor. This caused the drain voltage to decrease. Conversely, when gate voltage decreased, drain current decreased and the drain voltage increased.

This inverse relationship between gate excitation and drain voltage is characteristic of Common-Source amplifier operation and is responsible for the observed phase inversion.

The measured drain waveform confirmed that the transistor was operating in an active amplification region rather than functioning as a simple switch.

Key Observations

* Drain voltage responded dynamically to input excitation.
* Inversion behavior matched theoretical expectations.
* Active-region operation was maintained.
* Stable signal amplification observed throughout the simulation.

⸻

Monte Carlo Simulation Results

The most significant portion of the project involved statistical verification using Monte Carlo analysis.

A total of 100 simulation runs were performed. During each run, resistor values were randomly varied within a ±5% tolerance range to emulate realistic manufacturing variation.

This process produced 100 unique amplifier realizations, each representing a physically plausible circuit that could be constructed using commercially available components.

The resulting waveform overlays created a visual representation of performance variation across the entire population of simulated circuits.

⸻

Output Voltage Variation

The Monte Carlo output voltage overlays demonstrated that the amplifier maintained functionality across all 100 simulation runs.

Although small differences in output amplitude were observed, the overall waveform shape remained consistent.

The variation in amplitude resulted from changes in resistor values, which slightly altered transistor bias conditions and gain characteristics.

Despite these variations, the amplifier continued to operate correctly in every simulation instance.

Key Observations

* All simulation runs remained operational.
* Output waveforms remained stable.
* Gain variation was limited.
* No catastrophic failures occurred.
* No unstable operating points were observed.

⸻

Drain Current Variation

Drain current variation was also monitored throughout the Monte Carlo analysis.

The resulting current distributions demonstrated that resistor tolerances produced measurable but controlled changes in MOSFET operating current.

The source resistor provided effective negative feedback, limiting excessive current variation and improving circuit robustness.

The observed drain current spread closely matched theoretical expectations for a resistor-tolerance-driven variation study.

Key Observations

* Drain current remained within expected bounds.
* Negative feedback improved stability.
* No excessive current conditions occurred.
* Current variation remained predictable.

⸻

Statistical Robustness Assessment

One of the primary goals of Monte Carlo analysis is determining whether a circuit remains functional despite manufacturing uncertainty.

The results obtained during this project indicate a robust design.

Across all 100 simulations:

* The amplifier remained biased correctly.
* Signal amplification was preserved.
* Output waveforms remained stable.
* No simulation failures occurred.
* No unstable operating conditions were observed.

These findings indicate that the amplifier possesses strong tolerance immunity and is capable of maintaining acceptable performance even when component values deviate from their nominal specifications.

⸻

Engineering Significance

Statistical verification is an essential step in professional analog design workflows.

Real-world electronic systems are never assembled using ideal components. Every resistor, capacitor, transistor, and semiconductor device exhibits some degree of manufacturing variation.

Monte Carlo analysis provides a practical method for evaluating these effects before hardware fabrication.

The methodology implemented in this project mirrors verification approaches commonly used in:

* Analog Integrated Circuit Design
* Mixed-Signal Verification
* Power Electronics Design
* Automotive Electronics
* Aerospace Electronics
* Reliability Engineering

By incorporating tolerance analysis into the design process, engineers can identify potential weaknesses early and ensure reliable operation across large production volumes.

⸻

Discussion

The results obtained from this investigation demonstrate that the Common-Source MOSFET amplifier is both functional and robust.

The circuit achieved successful amplification under nominal conditions while maintaining acceptable performance under statistically varied conditions.

The Monte Carlo analysis revealed that manufacturing tolerances produce measurable changes in gain, operating point, and drain current; however, these changes remain sufficiently small that amplifier functionality is preserved.

The successful completion of 100 simulation runs without failure provides strong evidence that the design possesses adequate design margin and tolerance immunity.

This project demonstrates a complete analog verification workflow, combining theoretical analysis, operating point validation, transient simulation, statistical modeling, and engineering interpretation.

⸻

Conclusion

The Common-Source BS170 MOSFET amplifier successfully satisfied all design objectives. Operating point analysis confirmed stable transistor biasing, transient analysis verified signal amplification, and Monte Carlo simulation demonstrated robust operation under realistic manufacturing variation.

The statistical analysis showed that the amplifier maintained functionality across 100 randomized simulation runs using ±5% resistor tolerances. The resulting performance variations were predictable, controlled, and consistent with theoretical expectations.

The project demonstrates the practical application of analog circuit design principles, simulation-driven verification, and statistical tolerance analysis within a professional engineering workflow.
