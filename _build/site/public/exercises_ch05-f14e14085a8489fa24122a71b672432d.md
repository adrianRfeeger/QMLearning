---
title: "Chapter 5 — Exercises"
---

# Chapter 5 Exercises: Entanglement

---

## Exercises

### Exercise 5.1: Detecting Entanglement

You are given a two-qubit state: `|ψ⟩ = (1/2)(|00⟩ + |01⟩ + |10⟩ + |11⟩)`.

**Questions:**
a) Can this state be written as `|a⟩ ⊗ |b⟩` for some single-qubit states `|a⟩` and `|b⟩`?
b) Is this state entangled?

*Hint:* Try `|a⟩ = (|0⟩+|1⟩)/√2` and `|b⟩ = (|0⟩+|1⟩)/√2`.

<details><summary>Click for answer</summary>

a) Yes! `(1/√2)(|0⟩+|1⟩) ⊗ (1/√2)(|0⟩+|1⟩) = (1/2)(|00⟩+|01⟩+|10⟩+|11⟩)`.

b) **Not entangled** — it's a product state. The qubits are independent. Entanglement means you *cannot* factor the state this way.

</details>

---

### Exercise 5.2: CHSH Simulation

Write a function that:
a) Generates random measurement angles for Alice and Bob
b) Simulates measurement outcomes for a Bell state
c) Computes the CHSH quantity S

<details><summary>Click for answer</summary>

```python
import numpy as np

def simulate_CHSH(n_measurements=10000):
    rng = np.random.default_rng(42)
    # One common set of optimal angles for ideal Bell correlations
    a, a_p = 0, np.pi/2          # Alice: 0°, 90°
    b, b_p = np.pi/4, -np.pi/4  # Bob: 45°, -45°
    
    # For this idealized Bell-pair model, correlation = cos(angle_diff)
    def E(angle_a, angle_b):
        expected = np.cos(angle_a - angle_b)
        p_same = (1 + expected) / 2
        products = np.where(rng.random(n_measurements // 4) < p_same, 1, -1)
        return np.mean(products)
    
    S = E(a, b) + E(a, b_p) + E(a_p, b) - E(a_p, b_p)
    return S

print(f"Simulated CHSH: S = {simulate_CHSH():.3f}")
print("Should be ≈ 2.83 (quantum) vs 2.00 (classical limit)")
```

</details>

---

### Exercise 5.3: GHZ State Measurement

The GHZ state is `|GHZ⟩ = (1/√2)(|000⟩ + |111⟩)`.

**Question:** If Alice measures her qubit and gets 0, what are Bob's and Charlie's qubits? What if Alice gets 1?

<details><summary>Click for answer</summary>

If Alice measures 0: the state collapses to `|000⟩`. Bob and Charlie both have `|0⟩`.

If Alice measures 1: the state collapses to `|111⟩`. Bob and Charlie both have `|1⟩`.

All three are perfectly correlated — measuring any one fixes the correlated outcomes for the others. This is stronger than pairwise entanglement: it's genuine tripartite entanglement.

</details>

---

### Exercise 5.4: Entanglement Swapping

Two independent Bell pairs exist: `|Φ⁺⟩_AB` (Alice-Bob) and `|Φ⁺⟩_CD` (Charlie-Dave).

If Charlie performs a Bell measurement on qubits B and C (one from each pair), what happens to qubits A and D?

<details><summary>Click for answer</summary>

**Entanglement is swapped!** Initially, A is entangled with B, and C is entangled with D. When Charlie measures B and C in the Bell basis, he projects them into one of the four Bell states. This projects qubits A and D into an entangled state — even though A and D never directly interacted.

The full 4-qubit state before measurement is:
`|Φ⁺⟩_AB ⊗ |Φ⁺⟩_CD = (|00⟩+|11⟩)/√2 ⊗ (|00⟩+|11⟩)/√2`

Rewriting in terms of B and C Bell basis, A and D become entangled. Specifically, depending on Charlie's measurement outcome, A and D end up in one of the four Bell states.

This is the basis of quantum repeaters for long-distance quantum communication.

</details>

---

### Exercise 5.5: No-Cloning Theorem

Show that a cloning operation cannot exist. If a unitary `U` cloned states, then `U|ψ⟩|0⟩ = |ψ⟩|ψ⟩` for any `|ψ⟩`.

**Hint:** Take two different states `|φ⟩` and `|ψ⟩`, compute `⟨φ|ψ⟩` using both sides of the cloning equation, and show a contradiction.

<details><summary>Click for answer</summary>

Assume U clones both `|φ⟩` and `|ψ⟩`:

`U|φ⟩|0⟩ = |φ⟩|φ⟩` and `U|ψ⟩|0⟩ = |ψ⟩|ψ⟩`

Taking inner products:
`⟨φ|⟨0|U†U|ψ⟩|0⟩ = ⟨φ|⟨0|ψ⟩|0⟩ = ⟨φ|ψ⟩`

But also: `⟨φ|⟨φ|ψ⟩|ψ⟩ = ⟨φ|ψ⟩²`

So `⟨φ|ψ⟩ = ⟨φ|ψ⟩²`, which means `⟨φ|ψ⟩ = 0` or `⟨φ|ψ⟩ = 1`.

This means U can only clone states that are either identical or orthogonal — not arbitrary superpositions! Since quantum gates must work for *all* states, cloning is impossible.

</details>
