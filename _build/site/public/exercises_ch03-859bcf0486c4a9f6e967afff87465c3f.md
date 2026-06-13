---
title: "Chapter 3 — Exercises"
---

# Chapter 3 Exercises: Wave Mechanics

---

## Exercises

### Exercise 3.1: Normalization of the Particle in a Box

The wave function is `ψₙ(x) = √(2/L) sin(nπx/L)`.

**Task:** Verify analytically that `∫₀ᴸ |ψₙ(x)|² dx = 1` for any `n`.

*Hint:* Use the identity `sin²(θ) = (1 - cos(2θ))/2`.

<details><summary>Click for answer</summary>

`∫₀ᴸ (2/L) sin²(nπx/L) dx = (2/L) ∫₀ᴸ (1 - cos(2nπx/L))/2 dx`

`= (1/L) [x - (L/2nπ)sin(2nπx/L)] from 0 to L`

`= (1/L) [(L - 0) - (L/2nπ)(sin(2nπ) - sin(0))]`

`= (1/L) [L - 0] = 1` ✓ (since `sin(2nπ) = 0` for all integer n)

</details>

---

### Exercise 3.2: Expectation Value of Momentum

For the particle in a box, show that `⟨p⟩ = 0` for any energy level `n`.

*Hint:* `⟨p⟩ = ∫ ψ*(x)(-iℏ d/dx)ψ(x) dx`. The wave function is real, so you're integrating `sin × cos`.

<details><summary>Click for answer</summary>

`dψₙ/dx = √(2/L) × (nπ/L) cos(nπx/L)`

`⟨p⟩ = -iℏ ∫₀ᴸ √(2/L)sin(nπx/L) × √(2/L)(nπ/L)cos(nπx/L) dx`

`= -iℏ(2nπ/L²) ∫₀ᴸ sin(nπx/L)cos(nπx/L) dx`

Since `sin·cos` is an odd function about `L/2`, the integral is 0. So `⟨p⟩ = 0`.

Physically: the particle bounces back and forth equally, so its average momentum is zero.

</details>

---

### Exercise 3.3: Tunneling Probability

A particle with energy `E = 2 eV` approaches a barrier of height `V = 5 eV` and width `L = 1 nm`.

The tunneling probability (approximately) is `T ≈ e^(-2κL)` where `κ = √(2m(V-E))/ℏ`.

For an electron, `m = 9.11×10⁻³¹ kg` and `ℏ = 1.055×10⁻³⁴ J·s`.

**Question:** Calculate `κ`, then `T`.

<details><summary>Click for answer</summary>

`V - E = 3 eV = 4.806×10⁻¹⁹ J`

`κ = √(2 × 9.11×10⁻³¹ × 4.806×10⁻¹⁹) / 1.055×10⁻³⁴ = 8.87×10⁹ m⁻¹`

`2κL = 2 × 8.87×10⁹ × 1×10⁻⁹ = 17.74`

`T ≈ e^(-17.74) ≈ 1.97×10⁻⁸`

Very small but nonzero — about 1 in 50 million chance. This tiny probability is what makes scanning tunneling microscopes work!

</details>

---

### Exercise 3.4: Ground State Energy Scaling

The ground state energy of a particle in a box is `E₁ = h²/(8mL²)`.

**Questions:**
a) If you double the box size, what happens to `E₁`?
b) If you replace the electron with a proton (≈1836× heavier), what happens to `E₁`?
c) Why can't atoms be infinitely small?

<details><summary>Click for answer</summary>

a) `E₁ ∝ 1/L²`, so doubling L reduces E₁ by a factor of 4.

b) `E₁ ∝ 1/m`, so using a proton reduces E₁ by 1836×. Heavier particles have lower zero-point energy.

c) Confining a particle to a very small space increases its kinetic energy (via the uncertainty principle). For electrons in nuclei, this energy would be enormous. This is why atoms have a characteristic size — the balance between electrostatic attraction and quantum confinement energy.

</details>

---

### Exercise 3.5: Uncertainty Principle Check

For the ground state of a particle in a box (`n=1`):
- `⟨x⟩ = L/2`
- `⟨x²⟩ = L²(1/3 - 1/(2π²))`
- `⟨p⟩ = 0`
- `⟨p²⟩ = (πℏ/L)²`

Verify that `Δx · Δp ≥ ℏ/2`.

<details><summary>Click for answer</summary>

`Δx = √(⟨x²⟩ - ⟨x⟩²) = √(L²(1/3 - 1/(2π²)) - L²/4) = L√(1/12 - 1/(2π²)) ≈ 0.181L`

`Δp = √(⟨p²⟩ - ⟨p⟩²) = πℏ/L`

`Δx · Δp ≈ 0.181L · πℏ/L = 0.181πℏ ≈ 0.569ℏ`

Since `0.569ℏ > 0.5ℏ`, the uncertainty principle is satisfied ✓

</details>
