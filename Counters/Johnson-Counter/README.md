# 4-bit Johnson Counter using D Flip-Flops

## Overview

This project implements a **4-bit Johnson Counter (Twisted Ring Counter)** using **D Flip-Flops** in **Verilog HDL**.

A Johnson Counter is a modified ring counter where the complement of the last flip-flop output is fed back to the input of the first flip-flop.

For an n-bit Johnson Counter:

```text
Number of States = 2n
```

Thus, a 4-bit Johnson Counter generates **8 unique states**.

---

## Features

- 4-bit Johnson Counter
- D Flip-Flop based design
- Positive edge triggered
- Active high reset
- Generates 8 unique states
- Simple sequential logic

---

## Working Principle

Unlike a Ring Counter, the inverted output of the last flip-flop is fed back to the first flip-flop.

```text
D0 = Q3̅
D1 = Q0
D2 = Q1
D3 = Q2
```

This creates a sequence of 2n states before repeating.

---

## State Table

| Present State | Next State |
|--------------|------------|
| 0000 | 0001 |
| 0001 | 0011 |
| 0011 | 0111 |
| 0111 | 1111 |
| 1111 | 1110 |
| 1110 | 1100 |
| 1100 | 1000 |
| 1000 | 0000 |

---

## State Transition Diagram

```text
0000 → 0001 → 0011 → 0111
 ↑                     ↓
0000 ← 1000 ← 1100 ← 1110
          ↑
         1111
```

---

## D Flip-Flop Characteristic Table

| D | Q(n+1) |
|---|--------|
| 0 |   0    |
| 1 |   1    |

---

## Excitation Table — 4-bit Johnson Counter

| Present State | Next State | Q3 | Q2 | Q1 | Q0 | D3 | D2 | D1 | D0 |
|--------------|------------|----|----|----|----|----|----|----|----|
| 0000 | 0001 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 1 |
| 0001 | 0011 | 0 | 0 | 0 | 1 | 0 | 0 | 1 | 1 |
| 0011 | 0111 | 0 | 0 | 1 | 1 | 0 | 1 | 1 | 1 |
| 0111 | 1111 | 0 | 1 | 1 | 1 | 1 | 1 | 1 | 1 |
| 1111 | 1110 | 1 | 1 | 1 | 1 | 1 | 1 | 1 | 0 |
| 1110 | 1100 | 1 | 1 | 1 | 0 | 1 | 1 | 0 | 0 |
| 1100 | 1000 | 1 | 1 | 0 | 0 | 1 | 0 | 0 | 0 |
| 1000 | 0000 | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |

---

## D Input Equations

| Flip-Flop | D Input |
|-----------|---------|
| D0 | Q3̅ |
| D1 | Q0 |
| D2 | Q1 |
| D3 | Q2 |

---

## Truth Table

| Clock Pulse | Output State |
|------------|--------------|
| 0 | 0000 |
| 1 | 0001 |
| 2 | 0011 |
| 3 | 0111 |
| 4 | 1111 |
| 5 | 1110 |
| 6 | 1100 |
| 7 | 1000 |
| 8 | 0000 |

---

## Files Included

```text
├── d_flipflop.v
├── johnson_counter.v
├── johnson_counter_tb.v
├── waveform.png
└── README.md
```

---

## Simulation

Simulation verifies:

- Johnson counting sequence
- Feedback inversion logic
- Reset functionality
- Clock synchronization
- Complete 8-state cycle

### Simulation Tools

- EDA Playground
- ModelSim
- Vivado Simulator
- GTKWave

---

## Applications

- Frequency division
- Sequence generation
- Timing circuits
- Digital pattern generators
- State machine design
- Control systems

---

## Advantages

- Generates 2n states using n flip-flops
- Simple hardware implementation
- Easy state decoding
- High-speed operation
- FPGA friendly design

---

## Limitations

- Not a natural binary counter
- Limited counting sequence
- Requires feedback logic

---

## Future Improvements

- Parameterized Johnson Counter
- Bidirectional Johnson Counter
- FPGA optimized implementation
- Low power design
- Programmable sequence generator

---

## Author

Part of a VLSI Digital Design repository focused on:

- RTL Design
- FPGA Systems
- Semiconductor Architecture
- Digital IC Design
- Low Power VLSI
