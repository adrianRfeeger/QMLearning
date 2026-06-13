---
title: "Chapter 4 — Exercises"
---

# Chapter 4 Exercises: Spin and Qubits

---

## Exercises

### Exercise 4.1: Gate Sequences

Starting from `|0⟩`:

a) Apply H, then X. What state do you get?
b) Apply X, then H. What state do you get?
c) Are these the same? Do the operations commute?

<details><summary>Click for answer</summary>

a) `H|0⟩ = |+⟩ = (1/√2)[1, 1]`. Then `X|+⟩ = (1/√2)[1, 1]` (X swaps the components, they're equal, so it stays). Result: `|+⟩`.

b) `X|0⟩ = |1⟩ = [0, 1]`. Then `H|1⟩ = |−⟩ = (1/√2)[1, -1]`. Result: `|−⟩`.

c) **No.** Applying H then X gives `XH|0⟩ = |+⟩`, while applying X then H gives `HX|0⟩ = |−⟩`. Gates don't commute. This is like the commutator `[H, X] = HX - XH ≠ 0`.

</details>

---

### Exercise 4.2: Bloch Sphere Coordinates

A qubit state is `|ψ⟩ = (3/5)|0⟩ + (4/5)|1⟩`.

**Questions:**
a) What are the polar angle `θ` and azimuthal angle `φ`?
b) Where is this on the Bloch sphere?
c) If you measure in the Z basis, what's the probability of getting 0?

<details><summary>Click for answer</summary>

a) `α = cos(θ/2) = 3/5`, so `θ/2 = arccos(3/5) = 0.927 rad`, `θ = 1.854 rad = 106.3°`.

`β = e^(iφ)sin(θ/2)`. Since `sin(θ/2) = 4/5` and β is real and positive, `φ = 0`.

b) In the XZ plane, mostly toward +X and slightly below the equator (θ > 90°), with Bloch vector `(24/25, 0, -7/25)`.

c) P(0) = |α|² = (3/5)² = 9/25 = 36%.

</details>

---

### Exercise 4.3: Matrix Powers

Compute `X²`, `Z²`, `H²`, and `S²`. What do you notice?

<details><summary>Click for answer</summary>

`X² = [[1,0],[0,1]] = I` — X is its own inverse
`Z² = [[1,0],[0,1]] = I` — Z is its own inverse
`H² = [[1,0],[0,1]] = I` — Two Hadamards undo each other
`S² = [[1,0],[0,-1]] = Z` — S is the square root of Z, corresponding to a quarter-turn around Z up to a global phase

Gates that square to identity are called **involutions**. X, Z, and H are involutions; S is not, because `S² = Z`.

</details>

---

### Exercise 4.4: Phase Kickback

When a controlled-Z gate acts on `(α|0⟩ + β|1⟩) ⊗ |1⟩`, show that the control qubit picks up a phase.

<details><summary>Click for answer</summary>

Initial state: `α|0⟩|1⟩ + β|1⟩|1⟩`

After C-Z: `α|0⟩|1⟩ - β|1⟩|1⟩`
         `= (α|0⟩ - β|1⟩) ⊗ |1⟩`

The target qubit is an eigenstate of Z with eigenvalue `-1`, because `Z|1⟩ = -|1⟩`. The minus sign therefore appears on the `|1⟩` component of the control qubit. This is ***phase kickback***: a phase applied to the target by the controlled gate "kicks back" onto the control amplitude.

More generally, when a controlled gate `CU` acts on `(α|0⟩ + β|1⟩)|t⟩`, and `|t⟩` is an eigenstate of `U` with eigenvalue `e^(iφ)`, the result is `(α|0⟩ + e^(iφ)β|1⟩)|t⟩`.

</details>

---

### Exercise 4.5: Multi-Qubit Basis States

For 3 qubits, there are 8 basis states. List them and their binary/decimal equivalents.

<details><summary>Click for answer</summary>

| Ket notation | Binary | Decimal | Vector |
|---|---|---|---|
| `|000⟩` | 000 | 0 | [1,0,0,0,0,0,0,0] |
| `|001⟩` | 001 | 1 | [0,1,0,0,0,0,0,0] |
| `|010⟩` | 010 | 2 | [0,0,1,0,0,0,0,0] |
| `|011⟩` | 011 | 3 | [0,0,0,1,0,0,0,0] |
| `|100⟩` | 100 | 4 | [0,0,0,0,1,0,0,0] |
| `|101⟩` | 101 | 5 | [0,0,0,0,0,1,0,0] |
| `|110⟩` | 110 | 6 | [0,0,0,0,0,0,1,0] |
| `|111⟩` | 111 | 7 | [0,0,0,0,0,0,0,1] |

There are `2^n` basis states for `n` qubits.

</details>
