# Proof Techniques (证明技巧)
## Words:
- even (偶数)
- odd (奇数)
- integer (整数)
- rational (有理数)
- irrational (无理数)
- prime (质数)
- composite (合数)
- divisible (可被整除的)
- floor (下取整)
- ceiling (上取整)

## Direct Proof (直接证明)

### Steps:
1. Assume the hypothesis ($P$) is true.
2. Use logical reasoning, definitions, and algebra to show that the conclusion ($Q$) must also be true.
3. Conclude that the implication ($P \rightarrow Q$) is true.

### Example:

**Statement:** The sum of two even integers is even.

**Proof:**

Let $m = 2a$ and $n = 2b$, where $a, b \in \mathbb{Z}$ are two even integers.

Then,
$$
m + n = 2a + 2b = 2(a + b)
$$

Since $a + b$ is an integer, $m + n$ is even.

Proven by direct proof.

---

**Statement:** If $m$ is an even integer, then $m^2$ is even.

**Proof:**

Let $m = 2k$, where $k \in \mathbb{Z}$ is an even integer.

Then,
$$
m^2 = (2k)^2 = 4k^2 = 2(2k^2)
$$

Let $p = 2k^2$, where $p \in \mathbb{Z}$.

Then,
$$
m^2 = 2p
$$

Since $p$ is an integer, $m^2$ is even (by the definition of even).

Proven by direct proof.

---

**Statement:** $\sqrt{2}$ is irrational.

**Proof:**

Assume $\sqrt{2}$ is rational.

Then, $\sqrt{2} = \frac{a}{b}$, where $a, b \in \mathbb{Z}$, $b \neq 0$, and $\frac{a}{b}$ is in lowest terms.

Then,
$$
2 = \frac{a^2}{b^2}
$$
Thus,
$$
a^2 = 2b^2
$$

This implies that $a^2$ is even, which means $a$ is even (since the square of an odd integer is odd).

Let $a = 2k$, where $k \in \mathbb{Z}$.

Then,
$$
(2k)^2 = 2b^2 \implies 4k^2 = 2b^2
$$

Dividing both sides by 2, we get
$$
2k^2 = b^2
$$

This implies that $b^2$ is even, which means $b$ is even.

But if both $a$ and $b$ are even, then $\frac{a}{b}$ is not in lowest terms, which contradicts our assumption.

Therefore, $\sqrt{2}$ is irrational.

---

## Proof by Contradiction (反证法)

### Steps:
1. Assume the negation of the conclusion ($\neg Q$) is true.
2. Use logical steps until you reach a contradiction (a statement that is always false).
3. Conclude that the original conclusion ($Q$) must be true.

### Example:

**Statement:** No odd integer can be written as the sum of three even integers.

**Proof:**

Assume an odd integer $a$ can be written as the sum of three even integers.

Let $a = 2k + 1$, where $k \in \mathbb{Z}$, and let the three even integers be $2m$, $2n$, and $2p$, where $m, n, p \in \mathbb{Z}$.

Then,
$$
a = 2m + 2n + 2p = 2(m + n + p)
$$

Thus, $a$ is even, which contradicts the assumption that $a$ is odd.

Therefore, no odd integer can be written as the sum of three even integers.

---

## Disproof by Counterexample (反例法)

To disprove a statement, we can provide a counterexample that shows the statement is false.

### Example:

**Statement:** All prime numbers are odd.

**Counterexample:** $2$ is a prime number, but it is even.

Therefore, the statement is false.

---

**Statement:** $\forall n \in \mathbb{Z}^+, 2^n + 1$ is prime.

**Counterexample:**

Let $n = 3$, then $2^3 + 1 = 9$, which is not prime.

Therefore, the statement is false.