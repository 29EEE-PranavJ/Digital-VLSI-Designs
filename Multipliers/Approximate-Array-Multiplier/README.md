
## Approximate 4×4 Array Multiplier

------------------------------------------------------------
OVERVIEW:
------------------------------------------------------------
This project implements a 4-bit approximate array multiplier designed for reduced hardware complexity, lower power consumption, and faster computation compared to a conventional exact array multiplier. 

The design introduces controlled approximation by simplifying carry propagation in lower significant bits while maintaining reasonable accuracy in higher significant bits.

------------------------------------------------------------
FEATURES:
------------------------------------------------------------
- 4×4 bit unsigned multiplication
- Reduced carry propagation logic
- XOR-based approximate addition
- Lower area and power consumption
- Faster computation compared to exact array multiplier
- Fully combinational design (no clock required)

------------------------------------------------------------
WORKING PRINCIPLE:
------------------------------------------------------------
1. Partial products are generated using bitwise AND between inputs A and B.
2. Instead of full ripple-carry addition, partial products are combined using XOR operations.
3. Carry propagation is reduced or removed in lower significant bit positions.
4. Higher significant bits are preserved with better accuracy to maintain acceptable output quality.
5. Final output is an 8-bit approximate product.

This trade-off reduces hardware complexity at the cost of minor computational error.

------------------------------------------------------------
INPUTS:
------------------------------------------------------------
A : 4-bit unsigned multiplicand (A[3:0])
B : 4-bit unsigned multiplier   (B[3:0])

------------------------------------------------------------
OUTPUTS:
------------------------------------------------------------
P : 8-bit approximate product (P[7:0])

------------------------------------------------------------
APPLICATIONS:
------------------------------------------------------------
- Image processing systems
- Machine learning accelerators
- Digital signal processing (DSP)
- Edge computing devices
- Low-power embedded systems
- Approximate computing architectures

------------------------------------------------------------
LIMITATIONS:
------------------------------------------------------------
- Introduces numerical error compared to exact multiplication
- Not suitable for financial or high-precision arithmetic systems
- Error increases for certain input combinations
- No error correction mechanism implemented
- Only supports unsigned 4-bit multiplication

------------------------------------------------------------
FUTURE ENHANCEMENTS:
------------------------------------------------------------
- Error-compensation circuit integration
- Extension to 8×8 and 16×16 multipliers
- Hybrid design with Wallace/Booth architecture
- Dynamic precision scaling based on input significance
- FPGA optimization with pipelining
- Integration into approximate DSP/AI accelerator pipeline

------------------------------------------------------------

## Author

Pranav J
