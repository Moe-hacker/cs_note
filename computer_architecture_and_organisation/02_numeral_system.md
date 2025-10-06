# Number Systems (数制)

Number systems express numbers in different bases. The most common are:

- **Decimal (十进制):** Base 10, digits 0–9
- **Binary (二进制):** Base 2, digits 0–1
- **Octal (八进制):** Base 8, digits 0–7
- **Hexadecimal (十六进制):** Base 16, digits 0–9 and A–F

---

# Converting Between Number Systems (数制转换)

## Converting Any Base to Decimal

Multiply each digit by its base raised to the power of its position (right to left, starting at 0), then sum the results.

**Example: Binary 1001 to Decimal**

| 2³ | 2² | 2¹ | 2⁰ |
|----|----|----|----|
|  1 |  0 |  0 |  1 |

Calculation:  
1×2³ + 0×2² + 0×2¹ + 1×2⁰ = 8 + 0 + 0 + 1 = **9 (decimal)**

**Example: Hexadecimal 1A3 to Decimal**

| 16² | 16¹ | 16⁰ |
|-----|-----|-----|
|  1  |  A  |  3  |

Calculation:  
1×16² + 10×16¹ + 3×16⁰ = 256 + 160 + 3 = **419 (decimal)**

---

## Converting Decimal to Other Bases

Repeatedly divide the decimal number by the target base, recording remainders. Read the remainders in reverse order.

**Example: Decimal 45 to Binary**

| Division | Quotient | Remainder |
|----------|----------|-----------|
| 45 ÷ 2   |   22     |     1     |
| 22 ÷ 2   |   11     |     0     |
| 11 ÷ 2   |    5     |     1     |
| 5 ÷ 2    |    2     |     1     |
| 2 ÷ 2    |    1     |     0     |
| 1 ÷ 2    |    0     |     1     |

Reading remainders in reverse: **101101 (binary)**

**Example: Decimal 514 to Hexadecimal**

| Division | Quotient | Remainder |
|----------|----------|-----------|
| 514 ÷ 16 |   32     |     2     |
| 32 ÷ 16  |    2     |     0     |
| 2 ÷ 16   |    0     |     2     |

Reading remainders in reverse: **202 (hexadecimal)**

---

### Table Method (Preferred)

**45 (decimal) to Binary:**

| 64 | 32 | 16 | 8 | 4 | 2 | 1 |
|----|----|----|---|---|---|---|
|  0 |  1 |  0 | 1 | 1 | 0 | 1 |

45 = 32 + 8 + 4 + 1 = **101101 (binary)**

**514 (decimal) to Hexadecimal:**

| 256 | 128 | 64 | 32 | 16 | 8 | 4 | 2 | 1 |
|-----|-----|----|----|----|---|---|---|---|
|  2  |  0  |  2 |  0 |  0 | 0 | 2 | 0 | 0 |

514 = 2×256 + 2×2 = **202 (hexadecimal)**