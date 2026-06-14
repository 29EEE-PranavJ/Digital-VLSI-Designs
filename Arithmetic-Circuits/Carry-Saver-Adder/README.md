# 4-bit Carry Save Adder (CSA)

## Overview

A Carry Save Adder (CSA) is a high-speed arithmetic circuit used to add three or more binary numbers simultaneously.

Unlike Ripple Carry Adders and Carry Lookahead Adders, a CSA does not immediately propagate carry bits. Instead, it saves carry outputs and generates partial sums in parallel.

This significantly reduces addition delay and makes CSA a fundamental building block in multiplier architectures such as:

- Wallace Tree Multiplier
- Dadda Multiplier
- Booth Multiplier
- DSP Arithmetic Units

---

## Features

- High-speed multi-operand addition
- Parallel carry generation
- Reduced propagation delay
- Efficient hardware utilization
- Widely used in VLSI arithmetic circuits

---

## Why Carry Save Adder?

### Conventional Addition

```text
A + B + C

Step 1:
A + B

Step 2:
Result + C
```

Multiple carry propagation stages increase delay.

---

### Carry Save Addition

```text
A
B
C
│
▼

Carry Save Adder

│
├── Sum Vector
└── Carry Vector
```

Carries are saved rather than propagated immediately.

---

## Inputs and Outputs

| Signal | Description |
|----------|------------|
| A[3:0] | First Operand |
| B[3:0] | Second Operand |
| C[3:0] | Third Operand |
| Sum[3:0] | Sum Output |
| Carry[3:0] | Carry Output |

---

## Full Adder Equations

Each CSA stage uses a Full Adder.

### Sum

```text
Sum = A ⊕ B ⊕ C
```

### Carry

```text
Carry = AB + BC + AC
```

---

## Full Adder Truth Table

| A | B | C | Sum | Carry |
|---|---|---|-----|-------|
| 0 | 0 | 0 | 0 | 0 |
| 0 | 0 | 1 | 1 | 0 |
| 0 | 1 | 0 | 1 | 0 |
| 0 | 1 | 1 | 0 | 1 |
| 1 | 0 | 0 | 1 | 0 |
| 1 | 0 | 1 | 0 | 1 |
| 1 | 1 | 0 | 0 | 1 |
| 1 | 1 | 1 | 1 | 1 |

---

## CSA Operation Example

```text
A = 1010
B = 0110
C = 0011

CSA Output

Sum   = 1111
Carry = 0010
```

Final Result:

```text
Result = Sum + (Carry << 1)
```


---

## Carry Save Concept

```text
Input Operands
A
B
C
│
▼

CSA

│
├── Sum
└── Carry

Final Adder

Result = Sum + Carry
```

---

## Applications

- Wallace Tree Multipliers
- Dadda Multipliers
- Booth Multipliers
- DSP Systems
- ALUs
- MAC Units
- FPGA Arithmetic Blocks

---

## Advantages

- High-Speed Addition
- Reduced Carry Propagation Delay
- Efficient for Multi-Operand Addition
- Ideal for Multiplier Architectures

---

## Limitations

- Requires Final Carry Propagation Adder
- More Hardware than RCA
- Not Suitable for Simple Two-Operand Addition

---

## Comparison with Other Adders

| Adder Type | Speed | Complexity |
|------------|--------|------------|
| Ripple Carry Adder | Low | Low |
| Carry Lookahead Adder | High | Medium |
| Carry Save Adder | Very High | Medium |
| Wallace Tree Adder | Extremely High | High |

---

## Future Enhancements

- 8-bit CSA
- 16-bit CSA
- Wallace Tree Multiplier
- Dadda Multiplier
- Booth Multiplier
- MAC Unit Design

---

## Author

Pranav J
