# Subtractors

# Half Subtractor

## Description

A Half Subtractor subtracts one single-bit binary number from another.

Inputs:

- A (Minuend)
- B (Subtrahend)

Outputs:

- Difference (D)
- Borrow (Bout)

A Half Subtractor cannot accept a borrow input from a previous stage.

---

## Block Diagram

```text
 A ──┐
     ├── Half Subtractor ──► Difference
 B ──┘
                     └──► Borrow
```

---

## Truth Table

| A | B | Difference | Borrow |
|---|---|------------|--------|
| 0 | 0 |     0      |   0    |
| 0 | 1 |     1      |   1    |
| 1 | 0 |     1      |   0    |
| 1 | 1 |     0      |   0    |

---

## Boolean Expressions

| Output | Equation |
|----------|----------|
| Difference | A ⊕ B |
| Borrow | A̅B |

---

## Logic Gate Implementation

| Output | Gate Used |
|----------|-----------|
| Difference | XOR Gate |
| Borrow | NOT + AND Gate |

---

## Applications

- Binary Subtraction
- Arithmetic Logic Units
- Digital Processors
- Full Subtractor Design

---

## Limitations

- No Borrow Input
- Cannot Perform Multi-bit Subtraction Independently

---

# Full Subtractor

## Description

A Full Subtractor subtracts two binary digits and a borrow input from a previous stage.

Inputs:

- A (Minuend)
- B (Subtrahend)
- Bin (Borrow Input)

Outputs:

- Difference (D)
- Borrow Output (Bout)

---

## Block Diagram

```text
 A ──┐
     │
 B ──┼──► Full Subtractor ──► Difference
     │
Bin ─┘
                      └──► Borrow Out
```

---

## Truth Table

| A | B | Bin | Difference | Borrow |
|---|---|-----|------------|--------|
| 0 | 0 |  0  |     0      |   0    |
| 0 | 1 |  0  |     1      |   1    |
| 1 | 0 |  0  |     1      |   0    |
| 1 | 1 |  0  |     0      |   0    |
| 0 | 0 |  1  |     1      |   1    |
| 0 | 1 |  1  |     0      |   1    |
| 1 | 0 |  1  |     0      |   0    |
| 1 | 1 |  1  |     1      |   1    |

---

## Boolean Expressions

| Output | Equation |
|----------|----------|
| Difference | A ⊕ B ⊕ Bin |
| Borrow | A̅B + A̅Bin + BBin |

---

## Full Subtractor Using Half Subtractors

```text
Half Subtractor 1

D1 = A ⊕ B
B1 = A̅B

Half Subtractor 2

Difference = D1 ⊕ Bin
B2 = D1̅Bin

Borrow Out

Bout = B1 + B2
```

---

## Logic Gate Implementation

| Output | Gate Used |
|----------|-----------|
| Difference | XOR Gates |
| Borrow | NOT + AND + OR Gates |

---

## Applications

- Binary Arithmetic Units
- ALUs
- Processors
- DSP Systems
- FPGA Designs

---

## Advantages

- Supports Borrow Input
- Suitable for Multi-bit Subtraction
- Modular Design

---

## Limitations

- Borrow Propagation Delay
- More Hardware than Half Subtractor

---

## Simulation Tools

- ModelSim
- Vivado Simulator
- GTKWave
- EDA Playground

---

## Author
Pranav J
