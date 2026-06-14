# 4-bit Booth Multiplier

## Overview

The Booth Multiplier is a signed multiplication algorithm that reduces the number of partial products generated during multiplication.

Instead of generating a partial product for every multiplier bit, Booth Encoding examines adjacent bits and performs addition, subtraction, or shifting operations.

This significantly reduces hardware complexity and improves multiplication speed, especially when consecutive 1's appear in the multiplier.

Booth Multipliers are widely used in:

- Microprocessors
- DSP Systems
- FPGA Designs
- Arithmetic Logic Units
- AI Accelerators

---

## Features

- Supports signed multiplication
- Reduces partial products
- Faster than conventional array multiplication
- Efficient hardware utilization
- Suitable for VLSI implementation

---

## Inputs and Outputs

| Signal | Description |
|----------|------------|
| A[3:0] | Multiplicand |
| B[3:0] | Multiplier |
| P[7:0] | Product Output |

---

## Booth Encoding Rules

Booth algorithm examines two adjacent bits:

| Current Bit | Previous Bit | Operation |
|-------------|-------------|------------|
| 0 | 0 | No Operation |
| 0 | 1 | Add Multiplicand |
| 1 | 0 | Subtract Multiplicand |
| 1 | 1 | No Operation |

---

## Booth Algorithm

1. Initialize Product Register
2. Append extra bit Q(-1)=0
3. Examine Q0 and Q(-1)
4. Perform Add/Subtract operation
5. Arithmetic Right Shift
6. Repeat for n cycles
7. Generate Final Product



---

## Example

```text
Multiplicand = 0101 (5)

Multiplier   = 0011 (3)

Product      = 00001111 (15)
```

---

## Applications

- Signed Multiplication
- DSP Systems
- FPGA Designs
- AI Accelerators
- Embedded Systems
- VLSI Arithmetic Units

---

## Advantages

- Reduced Partial Products
- Supports Signed Numbers
- Faster Computation
- Efficient Hardware Utilization

---

## Limitations

- More Complex Control Logic
- Additional Encoding Hardware
- Less Efficient for Small Bit Widths

---

## Comparison

| Multiplier | Speed | Signed Support |
|------------|--------|---------------|
| Array Multiplier | Medium | No |
| Wallace Tree Multiplier | High | Limited |
| Dadda Multiplier | High | Limited |
| Booth Multiplier | Very High | Yes |



---

## Future Enhancements

- Radix-4 Booth Multiplier
- Modified Booth Multiplier
- Booth-Wallace Multiplier
- Booth-Dadda Multiplier

---

## Author

Pranav J
