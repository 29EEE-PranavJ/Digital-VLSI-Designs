# 4-bit Ring Counter using D Flip-Flops

## Overview

This project implements a **4-bit Ring Counter** using **D Flip-Flops** in **Verilog HDL**.

A Ring Counter is a special type of shift register in which the output of the last flip-flop is connected back to the input of the first flip-flop.

A single logic '1' circulates continuously through the register, producing a repeating sequence of states.

---

## Features

- 4-bit Ring Counter
- D Flip-Flop based design
- Positive edge triggered
- Active high reset
- One-hot state encoding
- Simple sequential logic design

---

## Working Principle

A Ring Counter is initialized with a single logic '1'.

At every clock pulse, the logic '1' shifts to the next flip-flop.

### Counting Sequence

```text
0001 → 0010 → 0100 → 1000 → 0001
```

The sequence repeats indefinitely.

---

## State Table

| Present State | Next State |
|--------------|-------------|
| 0001 | 0010 |
| 0010 | 0100 |
| 0100 | 1000 |
| 1000 | 0001 |

---

## State Diagram

```text
      0001
        ↓
      0010
        ↓
      0100
        ↓
      1000
        ↓
      0001
```

---

## D Flip-Flop Characteristic Table

| D | Q(n+1) |
|---|---------|
| 0 |    0    |
| 1 |    1    |

---

## D Input Equations

| Flip-Flop | D Input |
|------------|---------|
| D0 | Q3 |
| D1 | Q0 |
| D2 | Q1 |
| D3 | Q2 |

---

## Truth Table

| Clock Pulse | Output State |
|------------|--------------|
| 0 | 0001 |
| 1 | 0010 |
| 2 | 0100 |
| 3 | 1000 |
| 4 | 0001 |

---

## Files Included

```text
├── d_flipflop.v
├── ring_counter.v
├── ring_counter_tb.v
├── waveform.png
└── README.md
```

---

## Simulation

Simulation verifies:

- Circular shifting operation
- One-hot state generation
- Reset functionality
- Clock synchronization

### Simulation Tools

- EDA Playground
- ModelSim
- Vivado Simulator
- GTKWave

---

## Applications

- Sequence generators
- Traffic light controllers
- FSM implementation
- Timing circuits
- Digital pattern generators
- Control systems

---

## Advantages

- Simple architecture
- Easy state decoding
- Glitch-free operation
- High-speed implementation
- Suitable for FPGA applications

---

## Limitations

- Requires more flip-flops than binary counters
- Limited number of states
- Inefficient hardware utilization

---

## Future Improvements

- Parameterized ring counter
- Bidirectional ring counter
- Self-correcting ring counter
- FPGA optimized implementation
- Low power design

---

## Author

Part of a VLSI Digital Design repository focused on:

- RTL Design
- FPGA Systems
- Semiconductor Architecture
- Digital IC Design
- Low Power VLSI
