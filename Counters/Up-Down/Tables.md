
## State Table — Up Counter

| Present State | Next State |
|----------------|-------------|
| 000 | 001 |
| 001 | 010 |
| 010 | 011 |
| 011 | 100 |
| 100 | 101 |
| 101 | 110 |
| 110 | 111 |
| 111 | 000 |

---

## State Table — Down Counter

| Present State | Next State |
|----------------|-------------|
| 111 | 110 |
| 110 | 101 |
| 101 | 100 |
| 100 | 011 |
| 011 | 010 |
| 010 | 001 |
| 001 | 000 |
| 000 | 111 |

---

## T Flip-Flop Excitation Table

| Present State Q | Next State Q+ | T Input |
|----------------|----------------|---------|
| 0 | 0 | 0 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 0 |

---

## Simplified SOP Equations

### Up Counter Mode

| Flip-Flop | T Input Equation |
|------------|----------------|
| T0 | 1 |
| T1 | Q0 |
| T2 | Q1 · Q0 |

---

### Down Counter Mode

| Flip-Flop | T Input Equation |
|------------|----------------|
| T0 | 1 |
| T1 | Q0̅ |
| T2 | Q1̅ · Q0̅ |

---

## Combined Up-Down Logic

| Flip-Flop | SOP Equation |
|------------|----------------|
| T0 | 1 |
| T1 | mode·Q0 + mode̅·Q0̅ |
| T2 | mode·Q1·Q0 + mode̅·Q1̅·Q0̅ |
