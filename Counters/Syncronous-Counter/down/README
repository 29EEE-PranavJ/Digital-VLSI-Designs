# Synchronous Down Counter

## Overview

This project implements a **4-bit Synchronous Down Counter** using **Verilog HDL**.

A synchronous counter uses a **common clock signal** for all flip-flops.  
Unlike asynchronous counters, all flip-flops change state simultaneously on the clock edge.

The counter performs binary down counting:

```text
1111 → 1110 → 1101 → 1100 → ... → 0000
```

After reaching `0000`, the counter rolls back to `1111`.

---

## Features

- 4-bit synchronous down counting
- Common clock architecture
- Positive edge triggered
- Active high reset
- Simultaneous state transition
- Faster than ripple counters

---

## Working Principle

In synchronous counters:

- All flip-flops receive the same clock signal
- State transitions occur simultaneously
- Propagation delay is minimized

The counter decrements by `1` on every positive clock edge.

---

## State Table

| Present State | Next State |
|----------------|------------|
| 1111 | 1110 |
| 1110 | 1101 |
| 1101 | 1100 |
| 1100 | 1011 |
| 1011 | 1010 |
| 1010 | 1001 |
| 1001 | 1000 |
| 1000 | 0111 |
| 0111 | 0110 |
| 0110 | 0101 |
| 0101 | 0100 |
| 0100 | 0011 |
| 0011 | 0010 |
| 0010 | 0001 |
| 0001 | 0000 |
| 0000 | 1111 |

---

## Applications

- Digital timers
- Countdown systems
- FSM sequencing
- Processor control logic
- Address generation
- Event counters

---

## Advantages

- High speed operation
- Reduced propagation delay
- Better timing accuracy
- Scalable design
- Suitable for modern VLSI systems

---

## Limitations

- Requires more combinational logic
- Increased hardware complexity
- Higher switching activity

---

## Future Improvements

- Parameterized counter width
- Programmable modulus
- Clock gated implementation
- FPGA optimized design
- Low power architecture

