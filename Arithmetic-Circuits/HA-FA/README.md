# ADDERS

# Half Adder

## Overview

A Half Adder is a combinational logic circuit used to add two single-bit binary numbers.

It produces:

- Sum (S)
- Carry (C)

A Half Adder cannot account for a carry input from a previous stage.

---

## Block Diagram

```text
 A ──┐
     ├── Half Adder ──► Sum
 B ──┘
                 └──► Carry
```

---

## Truth Table

| A | B | Sum | Carry |
|---|---|-----|-------|
| 0 | 0 |  0  |   0   |
| 0 | 1 |  1  |   0   |
| 1 | 0 |  1  |   0   |
| 1 | 1 |  0  |   1   |

---

## Boolean Expressions

| Output | Equation |
|---------|----------|
| Sum | A ⊕ B |
| Carry | A · B |

---

## Logic Gate Implementation

| Output | Gate Used |
|----------|-----------|
| Sum | XOR Gate |
| Carry | AND Gate |

---

## Applications

- Binary Addition
- Arithmetic Logic Units (ALUs)
- Full Adder Design
- Digital Signal Processing
- VLSI Arithmetic Circuits

---

## Advantages

- Simple Design
- Low Hardware Requirement
- Fast Operation

---

## Limitations

- No Carry Input
- Cannot Perform Multi-bit Addition Alone

---



# Full Adder

## Overview

A Full Adder is a combinational logic circuit used to add three single-bit binary inputs.

Inputs:

- A
- B
- Carry Input (Cin)

Outputs:

- Sum (S)
- Carry Output (Cout)

A Full Adder overcomes the limitation of a Half Adder by accepting a carry input.

---

## Block Diagram

```text
 A ──┐
     │
 B ──┼──► Full Adder ──► Sum
     │
Cin ─┘
                   └──► Carry Out
```

---

## Truth Table

| A | B | Cin | Sum | Cout |
|---|---|-----|-----|------|
| 0 | 0 |  0  |  0  |  0   |
| 0 | 1 |  0  |  1  |  0   |
| 1 | 0 |  0  |  1  |  0   |
| 1 | 1 |  0  |  0  |  1   |
| 0 | 0 |  1  |  1  |  0   |
| 0 | 1 |  1  |  0  |  1   |
| 1 | 0 |  1  |  0  |  1   |
| 1 | 1 |  1  |  1  |  1   |

---

## Boolean Expressions

| Output | Equation |
|---------|----------|
| Sum | A ⊕ B ⊕ Cin |
| Cout | AB + BCin + ACin |

---

## Logic Gate Implementation

| Output | Gate Used |
|----------|-----------|
| Sum | XOR Gates |
| Cout | AND + OR Gates |

---

## Full Adder Using Half Adders

```text
Half Adder 1:
S1 = A ⊕ B
C1 = AB

Half Adder 2:
Sum = S1 ⊕ Cin
C2 = S1Cin

Carry Out:
Cout = C1 + C2
```

---

## Applications

- Ripple Carry Adders
- Carry Lookahead Adders
- ALUs
- DSP Processors
- Microprocessors
- FPGA Designs

---

## Advantages

- Supports Carry Input
- Suitable for Multi-bit Addition
- Modular Design

---

## Limitations

- Ripple Carry Delay in Large Adders
- Higher Hardware Requirement than Half Adder

---

```
