# Array Multiplier

## Overview

A 4×4 Array Multiplier is a combinational arithmetic circuit used to multiply two 4-bit binary numbers and generate an 8-bit product.

The multiplication process is performed by generating partial products using AND gates and summing them using Half Adders (HA) and Full Adders (FA) arranged in a regular array structure.

Due to its simple and modular architecture, the Array Multiplier is widely used as a foundation for understanding more advanced multiplier designs.

---

## Features

- Parallel partial product generation
- Regular array structure
- Simple hardware implementation
- Suitable for FPGA and ASIC designs
- Easy scalability to higher bit widths

---

## Inputs and Outputs

| Signal | Description |
|----------|------------|
| A[3:0] | First 4-bit Operand |
| B[3:0] | Second 4-bit Operand |
| P[7:0] | 8-bit Product Output |

---

## Working Principle

The multiplication process consists of three stages:

### 1. Partial Product Generation

Each bit of operand A is multiplied with each bit of operand B.

```text
PPij = Ai × Bj
```

Total Partial Products:

```text
16 Partial Products
```

---

### 2. Partial Product Reduction

The generated partial products are arranged according to their significance and added using:

- Half Adders (HA)
- Full Adders (FA)

---

### 3. Product Generation

The final addition stage produces the 8-bit product.

```text
P = A × B
```

---

## Partial Product Matrix

```text
          A3 A2 A1 A0
×         B3 B2 B1 B0
----------------------
          PP00 PP01 PP02 PP03
     PP10 PP11 PP12 PP13
PP20 PP21 PP22 PP23
PP30 PP31 PP32 PP33
----------------------
      Product[7:0]
```


---

## Mathematical Example

```text
A = 1010 (10)

B = 0101 (5)

Product = 00110010 (50)
```

---

## Design Components

| Component | Quantity |
|------------|----------|
| AND Gates | 16 |
| Half Adders | Depends on implementation |
| Full Adders | Depends on implementation |

---

## Applications

- Arithmetic Logic Units (ALUs)
- Digital Signal Processing
- FPGA Designs
- Embedded Systems
- Image Processing
- Communication Systems
- VLSI Arithmetic Units

---

## Advantages

- Simple Design
- Regular Layout Structure
- Easy Verification
- Suitable for Small and Medium Word Lengths

---

## Limitations

- Large Area for Higher Bit Widths
- Higher Delay Compared to Wallace Tree Multipliers
- More Hardware Resources Required

---

## Comparison with Other Multipliers

| Multiplier | Speed | Area |
|------------|--------|------|
| Array Multiplier | Medium | Medium |
| Wallace Tree Multiplier | High | High |
| Dadda Multiplier | High | Lower |
| Booth Multiplier | Very High | Medium |
| Vedic Multiplier | High | Medium |

---

## Future Enhancements

- 8×8 Array Multiplier
- Signed Array Multiplier
- Wallace Tree Multiplier
- Dadda Multiplier
- Booth Multiplier
- Vedic Multiplier

---

## Author

Pranav J
