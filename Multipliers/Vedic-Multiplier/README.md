
## Vedic Multiplier using Urdhva Tiryagbhyam Sutra

------------------------------------------------------------
OVERVIEW:
------------------------------------------------------------
This file implements a Vedic multiplier based on the ancient Indian mathematical technique called Urdhva Tiryagbhyam (Vertically and Crosswise). 
It is a fast multiplication technique used in VLSI design to reduce computation delay by generating partial products in parallel rather than sequential addition as in conventional array multipliers.
The architecture is highly efficient for digital systems because it reduces propagation delay and increases throughput.

------------------------------------------------------------
THEORY:
------------------------------------------------------------
The Urdhva Tiryagbhyam Sutra is part of Vedic Mathematics and translates to "Vertically and Crosswise".

Unlike conventional multiplication methods where partial products are generated and then added sequentially, this method generates all partial products simultaneously and performs addition in a structured crosswise manner.

Key idea:
- Multiply bits vertically (bit-wise AND)
- Multiply crosswise combinations of bits
- Add results using parallel adders

This parallelism significantly reduces critical path delay in hardware implementation.

------------------------------------------------------------
ALGORITHM:
------------------------------------------------------------
For two 4-bit numbers:
A = A3 A2 A1 A0
B = B3 B2 B1 B0

Step 1: Multiply least significant bits
P0 = A0 × B0

Step 2: Crosswise multiplication and addition
P1 = (A1×B0 + A0×B1)

Step 3: Middle stage
P2 = (A2×B0 + A1×B1 + A0×B2)

Step 4: Next crosswise stage
P3 = (A3×B0 + A2×B1 + A1×B2 + A0×B3)

Step 5: Upper stages
P4 = (A3×B1 + A2×B2 + A1×B3)
P5 = (A3×B2 + A2×B3)
P6 = (A3×B3)

Final product is formed by adding all P0–P6 with proper carry propagation.

------------------------------------------------------------
FEATURES:
------------------------------------------------------------
- Parallel generation of partial products
- Reduced multiplication delay
- Faster than conventional array multipliers
- Scalable architecture (4×4, 8×8, 16×16)
- Regular and structured layout suitable for VLSI
- Efficient hardware utilization

------------------------------------------------------------
WORKING PRINCIPLE:
------------------------------------------------------------
1. Inputs are split into individual bits.
2. Bitwise AND operations generate partial products.
3. Crosswise multiplication is performed according to Urdhva Tiryagbhyam sutra.
4. All partial products are summed using adders arranged in hierarchical stages.
5. Carry propagation is minimized due to parallel structure.
6. Final output is obtained after summation of all intermediate results.

------------------------------------------------------------
INPUTS:
------------------------------------------------------------
A : 4-bit unsigned multiplicand (A[3:0])
B : 4-bit unsigned multiplier   (B[3:0])

------------------------------------------------------------
OUTPUTS:
------------------------------------------------------------
P : 8-bit product (P[7:0])

------------------------------------------------------------
APPLICATIONS:
------------------------------------------------------------
- High-speed arithmetic circuits
- Digital signal processing (DSP)
- FPGA and ASIC design
- Cryptographic hardware
- AI/ML accelerators
- Image and video processing systems

------------------------------------------------------------
LIMITATIONS:
------------------------------------------------------------
- Requires more adders than simple shift-add multipliers
- Hardware complexity increases with bit width
- Carry propagation still exists in final adder stage
- Not inherently approximate (exact arithmetic design)
- Area increases compared to basic shift multipliers

------------------------------------------------------------
FUTURE ENHANCEMENTS:
------------------------------------------------------------
- Hybrid Vedic + Booth multiplier design
- Pipeline architecture for higher frequency operation
- FPGA-optimized implementation with LUT reduction
- Approximate Vedic multiplier for low-power systems
- Integration with MAC (Multiply Accumulate) units
- Power gating for unused adder stages

------------------------------------------------------------

## AUTHOR:

Pranav J
