# 4-bit Ripple Carry Adder

## Overview

A Ripple Carry Adder (RCA) is a combinational arithmetic circuit used to add two multi-bit binary numbers.

It is constructed by cascading multiple Full Adders, where the carry output of one stage becomes the carry input of the next stage.

The carry propagates (ripples) through each stage until the final carry output is generated.

---

## Features

- 4-bit binary addition
- Full Adder based architecture
- Simple and modular design
- Easy to implement in FPGA and ASIC designs
- Fundamental building block of arithmetic units

---

## Block Diagram

```text
          A0  B0
           │   │
           ▼   ▼
        ┌─────────┐
Cin ───►│   FA0   │─── C1
        └─────────┘
              │
              ▼

          A1  B1
           │   │
           ▼   ▼
        ┌─────────┐
C1 ────►│   FA1   │─── C2
        └─────────┘
              │
              ▼

          A2  B2
           │   │
           ▼   ▼
        ┌─────────┐
C2 ────►│   FA2   │─── C3
        └─────────┘
              │
              ▼

          A3  B3
           │   │
           ▼   ▼
        ┌─────────┐
C3 ────►│   FA3   │─── Cout
        └─────────┘
```

---

## Inputs and Outputs

| Signal | Description |
|----------|------------|
| A[3:0] | First 4-bit Operand |
| B[3:0] | Second 4-bit Operand |
| Cin | Initial Carry Input |
| Sum[3:0] | Addition Result |
| Cout | Final Carry Output |

---

## Full Adder Equations

### Sum

| Equation |
|-----------|
| Sum = A ⊕ B ⊕ Cin |

### Carry

| Equation |
|-----------|
| Cout = AB + BCin + ACin |

---

## Truth Table of Full Adder

| A | B | Cin | Sum | Cout |
|---|---|-----|-----|------|
| 0 | 0 | 0 | 0 | 0 |
| 0 | 1 | 0 | 1 | 0 |
| 1 | 0 | 0 | 1 | 0 |
| 1 | 1 | 0 | 0 | 1 |
| 0 | 0 | 1 | 1 | 0 |
| 0 | 1 | 1 | 0 | 1 |
| 1 | 0 | 1 | 0 | 1 |
| 1 | 1 | 1 | 1 | 1 |

---

## Example Operation

```text
   A = 1010
 + B = 0101
 -----------
 Sum = 1111
```

---

## Carry Propagation Table

| Stage | Carry Input | Carry Output |
|---------|------------|--------------|
| FA0 | Cin | C1 |
| FA1 | C1 | C2 |
| FA2 | C2 | C3 |
| FA3 | C3 | Cout |

---

## Simulation

Simulation verifies:

- Correct binary addition
- Carry propagation
- Overflow generation
- Multi-bit arithmetic operation

### Simulation Tools

- ModelSim
- Vivado Simulator
- GTKWave
- EDA Playground

---

## Applications

- Arithmetic Logic Units (ALUs)
- Microprocessors
- Digital Signal Processing
- FPGA Designs
- Embedded Systems
- Digital Calculators

---

## Advantages

- Simple Design
- Easy Implementation
- Modular Architecture
- Low Hardware Complexity

---

## Limitations

- High Carry Propagation Delay
- Slower for Large Bit Widths
- Not Suitable for High-Speed Arithmetic

---

## Comparison with Other Adders

| Adder Type | Speed | Complexity |
|------------|--------|------------|
| Ripple Carry Adder | Low | Low |
| Carry Lookahead Adder | High | Medium |
| Carry Select Adder | Higher | High |
| Kogge-Stone Adder | Very High | Very High |

---

## Future Enhancements

- 8-bit RCA
- 16-bit RCA
- Carry Lookahead Adder
- Carry Select Adder
- Parallel Prefix Adders

---

## Author

Pranav J
