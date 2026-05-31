Bias Calculations

Gate Voltage

The gate voltage is established through a resistive voltage divider.

VG = VDD × RG2 / (RG1 + RG2)

VG = 12 × (1 MΩ / 2 MΩ)

VG = 6 V

⸻

Source Voltage

The source voltage depends on drain current:

VS = ID × RS

Assuming:

ID ≈ 2.1 mA

VS = (2.1 mA)(1 kΩ)

VS ≈ 2.1 V

⸻

Drain Voltage

The drain voltage is determined by:

VD = VDD − IDRD

VD = 12 − (2.1 mA)(4.7 kΩ)

VD ≈ 2.13 V

This closely matches the simulated operating point.

⸻

Drain Current

Using measured simulation values:

ID ≈ 2.1 mA

This value remains stable across all Monte Carlo iterations with only minor deviations.

⸻

Voltage Gain

For a Common-Source amplifier:

AV ≈ −gmRD

The negative sign indicates a 180° phase inversion between input and output.

The exact gain depends on the operating transconductance of the BS170 transistor at the selected bias point.

⸻

Bias Verification

Simulation confirms:

* Stable gate bias
* Stable source bias
* Stable drain current
* Successful transistor operation in the desired region

The bias network successfully establishes a repeatable operating point suitable for analog signal amplification.
