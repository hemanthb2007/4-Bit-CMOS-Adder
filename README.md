# 4-Bit-CMOS-Adder
Design and simulation of a 4-bit binary ripple-carry adder using transistor-level CMOS logic in LTspice.

## Contents

- `4bit_adder_cmos.cir` - LTspice-compatible transistor-level CMOS netlist
- `README.md` - project overview and simulation instructions

## Circuit structure

The design implements one CMOS 1-bit full adder and instantiates it four times:

`Sum = A XOR B XOR Cin`

`Cout = (A AND B) OR (Cin AND (A XOR B))`

The stages are chained as `C1 -> C2 -> C3 -> Cout`, while `Cin` is connected to ground. The simulation uses 5 V supplies and generic 0.18 um-style PMOS/NMOS models.

## Run in LTspice

1. Open LTspice.
2. Choose **File > Open** and select `4bit_adder_cmos.cir`.
3. Run the transient simulation.
4. Add `A0-A3`, `B0-B3`, `S0-S3`, and `Cout` to the waveform viewer.

The input sources form repeating binary patterns, allowing each sum and carry output to be observed across multiple input combinations.
