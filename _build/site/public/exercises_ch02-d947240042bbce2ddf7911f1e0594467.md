---
title: "Chapter 2 — Exercises"
---

# Chapter 2 Exercises: Mathematical Foundations

---

## Exercises

### Exercise 2.1: Complex Number Geometry

Plot these on the complex plane:
- `z₁ = 1 + i`
- `z₂ = -1 + i`
- `z₃ = -1 - i`
- `z₄ = 1 - i`

**Questions:**
a) What shape do they form?
b) What is the magnitude and angle of each?
c) What happens when you multiply `z₁` by `i`? By `i²`?

<details><summary>Click for answer</summary>

They form a **square** centered at the origin.

| Complex | Magnitude | Angle |
|---------|-----------|-------|
| 1 + i | √2 ≈ 1.414 | 45° (π/4) |
| -1 + i | √2 ≈ 1.414 | 135° (3π/4) |
| -1 - i | √2 ≈ 1.414 | 225° (5π/4) |
| 1 - i | √2 ≈ 1.414 | 315° (7π/4) |

Multiplying by `i` rotates 90° counterclockwise. Multiplying by `i² = -1` rotates 180°.

</details>

---

### Exercise 2.2: Matrix Multiplication

Given:
```
A = [[2, 1],
     [1, 3]]
B = [[1, 0],
     [0, 2]]
```

Calculate `AB`, `BA`, and `A²`. Do `AB` and `BA` give the same result?

<details><summary>Click for answer</summary>

`AB = [[2, 2], [1, 6]]`
`BA = [[2, 1], [2, 6]]`
`A² = [[5, 5], [5, 10]]`

`AB ≠ BA` — matrix multiplication is **not commutative** in general.

</details>

---

### Exercise 2.3: Normalizing a Qubit State

A qubit is in the state `|ψ⟩ = α|0⟩ + β|1⟩` where `α = 3/5` and `β = 4/5`.

**Questions:**
a) Is this properly normalized? (`|α|² + |β|² = 1`?)
b) If not, what factor do you multiply both by?
c) What are the measurement probabilities after normalizing?

<details><summary>Click for answer</summary>

a) `|3/5|² + |4/5|² = 9/25 + 16/25 = 25/25 = 1`. **Yes**, it's already normalized!

b) N/A — no scaling needed.

c) P(0) = 9/25 = 36%. P(1) = 16/25 = 64%.

</details>

---

### Exercise 2.4: Eigenvector Check

The Pauli-X gate is `X = [[0, 1], [1, 0]]`.

**Questions:**
a) Show that `[1, 1]` is an eigenvector of X and find its eigenvalue.
b) Show that `[1, -1]` is also an eigenvector of X and find its eigenvalue.
c) What do these eigenstates have to do with the `|+⟩` and `|-⟩` states?

<details><summary>Click for answer</summary>

a) `X[1,1] = [1,1]` → eigenvalue = 1

b) `X[1,-1] = [-1,1] = -1×[1,-1]` → eigenvalue = -1

c) The normalized versions are `|+⟩ = (1/√2)[1,1]` and `|-⟩ = (1/√2)[1,-1]`. These are the eigenstates of X!

</details>

---

### Exercise 2.5: Complex Arithmetic

Calculate `(1+i)(1-i)` and explain geometrically what happened.

<details><summary>Click for answer</summary>

`(1+i)(1-i) = 1 - i² = 1 + 1 = 2`

Geometrically: `1+i` is at angle 45°, `1-i` is at angle -45°. Multiplying adds angles: 45° + (-45°) = 0°. The result is a positive real number with magnitude = product of magnitudes = √2 × √2 = 2.

</details>
