# 3-bit Synchronous Up-Down Counter using T Flip-Flops

## Overview

This project implements a **3-bit Synchronous Up-Down Counter** using **T Flip-Flops** in **Verilog HDL**.

A synchronous counter uses a common clock signal for all flip-flops.  
All flip-flops change state simultaneously on the positive clock edge.

The counter supports both:

- Up Counting
- Down Counting

based on the control input `mode`.

```text
mode = 1 → Up Counter
mode = 0 → Down Counter
```

---

## Features

- 3-bit synchronous counting
- Up and Down counting operation
- T Flip-Flop based design
- Common clock architecture
- Positive edge triggered
- Active high reset
- Simultaneous state transitions

---

## Working Principle

The counter operation depends on the `mode` input.

### Up Counting

```text
000 → 001 → 010 → 011 → 100 → 101 → 110 → 111
```

### Down Counting

```text
111 → 110 → 101 → 100 → 011 → 010 → 001 → 000
```

All flip-flops receive the same clock signal, eliminating ripple delay.


---

## Applications

- Digital timers
- FSM sequencing
- Position tracking
- Frequency division
- Address generation
- Processor control logic

---

## Advantages

- Faster than ripple counters
- Reduced propagation delay
- Flexible counting operation
- Scalable architecture
- Suitable for FPGA and VLSI systems

---

## Future Improvements

- Parameterized counter width
- Clock gated architecture
- Low power implementation
- FPGA optimized design
- Programmable modulus support

---
