# Asynchronous Ripple Counter

## Overview

This project implements a 4-bit Asynchronous Ripple Counter using Verilog HDL.

In an asynchronous counter, only the first flip-flop receives the external clock signal.  
The output of one flip-flop acts as the clock input for the next flip-flop, creating a ripple effect.

Due to sequential triggering, propagation delay accumulates across stages.

---

# Features

- 4-bit binary counting
- Negative edge triggered operation
- Ripple based clock propagation
- Active high reset
- Simple hardware implementation

---

# Theory

An asynchronous counter is also called a ripple counter because the clock transition ripples through each flip-flop stage.

### Working Principle

- First flip-flop toggles on every clock pulse
- Second flip-flop toggles based on output of first flip-flop
- Third flip-flop toggles based on output of second flip-flop
- And so on...

This creates binary counting behavior.

---

# Truth Table

| Clock Pulses | Counter Output |
|---|---|
| 0 | 0000 |
| 1 | 0001 |
| 2 | 0010 |
| 3 | 0011 |
| 4 | 0100 |
| ... | ... |
| 15 | 1111 |

---


# Applications

- Frequency division
- Event counting
- Digital clocks
- Timer circuits
- Low complexity digital systems

---

# Limitations

Asynchronous counters suffer from:
- Propagation delay accumulation
- Lower speed operation
- Glitch generation
- Poor scalability for high-frequency systems

Because of this, synchronous counters are preferred in modern high-speed VLSI systems.

---

# Future Improvements

Possible upgrades:
- Parameterized counter width
- Low power implementation
- Clock gated architecture
- Gray code ripple counter
- FPGA optimized design

---
