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
## Binary Addition (二进制加法)
Binary addition follows the same principles as decimal addition, with carries occurring when sums exceed the base (2 in this case).
| A | B | Sum | Carry |
|---|---|-----|-------|
| 0 | 0 |  0  |   0   |
| 0 | 1 |  1  |   0   |
| 1 | 0 |  1  |   0   |
| 1 | 1 |  0  |   1   |
For programming, binary addition can be implemented using bitwise operations:

```c
/*
 * Add two unsigned integers using bitwise operations.
 * This implements the elementary school algorithm in base 2:
 *   - Sum without carry is A XOR B.
 *   - Carry is (A AND B) shifted left by 1.
 *   - Repeat until there is no carry.
 *
 * Notes:
 *   - Runs in O(number_of_bits) iterations.
 *   - May overflow the unsigned int result (wraps modulo 2^N). No overflow checks are performed.
 */
unsigned int binary_add(unsigned int a, unsigned int b) {
    while (b != 0) {
        unsigned int carry = a & b;  // Calculate carry bits.
        a = a ^ b;                   // Sum without carry.
        b = carry << 1;              // Prepare carry for next position.
    }
    return a;
}

```

## Binary Subtraction (二进制减法)

We can compute subtraction by adding the two's complement (negation) of the subtrahend. The common shorthand is:

$$
A - B = A + (-B) = A + (\sim B + 1)
$$

This works in fixed-width, n-bit arithmetic (i.e. arithmetic modulo $2^{n}$). To see why, note that the additive inverse of an integer $N$ modulo $2^{n}$ can be represented as

$$
-N \equiv 2^{n} - N \pmod{2^{n}}.
$$

Now observe

$$
2^{n} - N = (2^{n} - 1) - N + 1 = (\sim N) + 1,
$$

because the n-bit number $2^{n}-1$ is all ones (111...111) and bitwise NOT (~) is defined as

$$
\sim N = (2^{n}-1) - N.
$$

Combining these gives the two's-complement identity

$$
-N \equiv \sim N + 1 \pmod{2^{n}}.
$$

So subtraction reduces to addition of the two's complement. The comment "overflow bit is discarded" means that any carry out of the most-significant (n-th) bit (which equals $2^{n}$) is ignored when working modulo $2^{n}$.

### Small numeric example (n = 4 bits)

Take $A = 6$ (0110₂) and $B = 3$ (0011₂). Compute $A - B$ via two's complement:

1. Bitwise NOT of $B$ (4 bits): $\sim B = 1100_{2}$ (12).
2. $\sim B + 1 = 1100_{2} + 0001_{2} = 1101_{2}$ (13). This is $-3$ modulo 16 because $3 + 13 = 16 \equiv 0 \pmod{16}$.
3. $A + (\sim B + 1) = 0110_{2} + 1101_{2} = 1\,0011_{2}$. The leading `1` is the carry-out (16) and is discarded, leaving $0011_{2} = 3$, which matches $6 - 3 = 3$.

# Binary Multiplication (二进制乘法)
We use shift-and-add, similar to decimal multiplication.
**Example: Multiply 1011₂ (11 decimal) by 101₂ (5 decimal)**

```
      1011    (11)
    x  101    (5)
    --------
      1011    (1011 * 1)
     0000     (1011 * 0, shifted left)
    1011      (1011 * 1, shifted left twice)
    --------
   110111    (55 decimal)
```
# Binary Division (二进制除法)
We use shift-and-subtract, similar to decimal long division.
**Example: Divide 1101₂ (13 decimal) by 11₂ (3 decimal)**

```
      1101    (13)
    ÷  0011   (3)
    --------
      0010    (2)
    --------
      0001    (1)
    --------
      0000    (0)
```
Quotient: 10₂ (2 decimal), Remainder: 1₂ (1 decimal)

For programming, C implementation with bitwise operations:

```c
/* 
 * Multiply two unsigned integers using the binary "shift-and-add" method.
 * This implements the elementary school algorithm in base 2:
 *   - If the low bit of b is 1, add the current a to the result.
 *   - Shift a left (multiply by 2) and b right (process next bit).
 *
 * Notes:
 *   - Runs in O(number_of_bits_in_b) iterations.
 *   - May overflow the unsigned int result (wraps modulo 2^N). No overflow checks are performed.
 */
unsigned int binary_multiply(unsigned int a, unsigned int b) {
    unsigned int result = 0;           // Accumulator for the product.

    // Process each bit of b until all bits have been handled.
    while (b > 0) {
        // If the least-significant bit of b is 1, add the current a to the result.
        // This corresponds to adding a * (1 << current_bit_position).
        if (b & 1U) { // Use unsigned literal for clarity.
            result += a; // Addition (may overflow/wrap).
        }

        // Prepare for the next bit:
        // - Shift a left to represent a * 2^(next_bit_position).
        // - Shift b right to move the next bit into the LSB position.
        a <<= 1;       // Multiply a by 2 (shift to next weight).
        b >>= 1;       // Drop the bit we just processed.
    }

    return result;
}

/*
 * Divide two unsigned integers using binary long division (shift-and-subtract).
 * This computes the integer quotient (dividend / divisor).
 *
 * Algorithm outline:
 *   - Iterate i from most-significant bit down to 0.
 *   - Shift the remainder left by 1 and bring in the next bit of the dividend.
 *   - If remainder >= divisor, subtract divisor and set the quotient bit i to 1.
 *
 * Notes:
 *   - Returns the quotient only. The final remainder (dividend % divisor) is left
 *     in the variable `remainder` at the end of the function; modify the function
 *     if you need to return or store it.
 *   - If divisor == 0, this implementation returns UINT_MAX as an error indicator.
 *     Adjust behavior as needed for your application.
 *   - Time complexity: O(word_size) (e.g., 32 or 64 iterations depending on sizeof).
 */
unsigned int binary_divide(unsigned int dividend, unsigned int divisor) {
    unsigned int quotient = 0;   // Accumulates the quotient bits.
    unsigned int remainder = 0;  // Running remainder (partial dividend).

    // Guard against division by zero. Here we return UINT_MAX to indicate error.
    if (divisor == 0) {
        return (unsigned int)-1; // UINT_MAX
    }

    // Start from the most significant bit of dividend and work downwards.
    // sizeof(dividend) * 8 gives the number of bits in the unsigned int type.
    for (int i = (int)(sizeof(dividend) * 8 - 1); i >= 0; --i) {
        // Shift remainder left by 1 to make room for the next bit.
        remainder = (remainder << 1) | ((dividend >> i) & 1U);
        // If the partial remainder is at least the divisor, subtract and set quotient bit.
        if (remainder >= divisor) {
            remainder -= divisor;
            quotient |= (1U << i); // Set bit i in the quotient.
        }
    }

    // At this point:
    //   - quotient contains dividend / divisor
    //   - remainder contains dividend % divisor (if you need it, return or store it)
    return quotient;
}
```