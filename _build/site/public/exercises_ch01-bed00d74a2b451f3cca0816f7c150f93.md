---
title: "Chapter 1 — Exercises"
---

# Chapter 1 Exercises: The Quantum World

Try these on your own first. Hints and full answers are at the bottom.

---

### Exercise 1.1: Thinking About Scale

Classical physics works perfectly for planets, cars, and baseballs. But it fails for atoms.

**Question:** An atom is about 10⁻¹⁰ meters across. A grain of sand is about 10⁻³ meters across. That's a factor of 10⁷ difference. Why do you think the rules change so dramatically at small scales? What property of light or matter would need to be "noticeable" at the atomic scale but not at the macroscopic scale?

---

### Exercise 1.2: Photoelectric Effect Calculation

A sodium surface has a work function of 2.28 eV (the minimum energy needed to eject an electron).

**a)** What is the minimum frequency of light that can eject electrons from sodium? (Use `E = hf`, where `h = 6.626 × 10⁻³⁴ J·s`)

**b)** What wavelength does that correspond to? Is it in the visible spectrum?

**c)** Why can't you eject electrons with very bright red light (650 nm) in the ordinary single-photon photoelectric effect, even if the light is extremely intense?

---

### Exercise 1.3: Hydrogen Transitions

**Question:** The Balmer series of hydrogen corresponds to electrons falling to the `n = 2` energy level. The red line (H-alpha) corresponds to the transition from `n = 3` to `n = 2`.

Using the formula `E_n = -13.6/n² eV`, calculate:

**a)** The energy difference for the `n = 3 → n = 2` transition.

**b)** The wavelength of the emitted photon.

**c)** If you heated hydrogen gas until electrons were excited to `n = 4`, what *other* spectral lines could you see as electrons cascade down?

---

### Exercise 1.4: The Observer Effect

**Scenario:** Imagine you modify the double-slit experiment so that an extremely sensitive detector at each slit tells you which slit *each electron goes through*.

**Questions:**

**a)** What happens to the interference pattern on the screen behind the slits?

**b)** Does the detector need to be "big" or "noisy" to destroy the pattern? Could you build an ideal, perfectly sensitive, completely non-disturbing detector?

**c)** If you could somehow *erase* the which-path information *after* the electron passed through the slits but *before* you looked at the detector record, would the interference pattern come back? (This is related to the famous "quantum eraser" experiments!)

---

### Exercise 1.5: Superposition Analogy

**Question:** We compared a spinning coin to a superposition. But consider a different analogy: a light bulb that is both ON and OFF at the same time. What's wrong with this analogy? How is a true quantum superposition *different* from simply not knowing whether the bulb is on or off?

---

## Answers

<details>
<summary>Click to reveal answers</summary>

### Answer 1.1
The key insight is that many quantum effects are tied to **Planck's constant** (`ℏ ≈ 1.055 × 10⁻³⁴ J·s`), an incredibly tiny number. Quantum effects become significant when they are *comparable to* or *larger than* this fundamental scale. At the atomic scale (10⁻¹⁰ m), quantum wavelengths are comparable to the size of the system. At the macroscopic scale, quantum effects are so tiny relative to the system size that they average out and become invisible.

Think of it like digital vs. analog: a smooth photo looks continuous from far away, but zoom in enough and you see individual pixels. Atoms are "pixelated" by quantum effects; everyday objects are too big to see the pixels.

### Answer 1.2

**a)** Minimum energy `E = 2.28 eV = 2.28 × 1.602 × 10⁻¹⁹ J = 3.653 × 10⁻¹⁹ J`

Frequency: `f = E/h = 3.653 × 10⁻¹⁹ / 6.626 × 10⁻³⁴ = 5.51 × 10¹⁴ Hz`

**b)** Wavelength: `λ = c/f = 3 × 10⁸ / 5.51 × 10¹⁴ = 544 × 10⁻⁹ m = 544 nm`

This is **green light** — right at the edge of the visible spectrum. Light with wavelength longer than 544 nm (yellow, orange, red, infrared) doesn't have enough energy per photon to eject electrons.

**c)** Because the ordinary photoelectric effect depends on the energy of *individual photons*, not the total light intensity. Each red photon (650 nm) carries only `E = hf = 3.06 × 10⁻¹⁹ J = 1.91 eV`, which is *less* than the 2.28 eV needed. Increasing brightness adds more low-energy photons, but it does not make each photon energetic enough. It's like trying to break a window by throwing ping-pong balls at it — even a million ping-pong balls won't break glass, but one baseball will.

### Answer 1.3

**a)** `E₃ = -13.6/9 = -1.511 eV`, `E₂ = -13.6/4 = -3.400 eV`

Energy difference: `ΔE = E₂ - E₃ = -3.400 - (-1.511) = -1.889 eV` (energy is *released*)

Photon energy: `1.889 eV`

**b)** `λ = hc/E = (6.626×10⁻³⁴)(3×10⁸) / (1.889 × 1.602×10⁻¹⁹) = 656 × 10⁻⁹ m = 656 nm`

This is the famous **red H-alpha line** of hydrogen!

**c)** Electrons at `n = 4` can cascade down in several ways:
- `4 → 3 → 2 → 1`: emits photons for each step
- `4 → 2 → 1`: skip `n = 3`, emit Balmer-beta (blue-green at 486 nm) and Lyman-alpha
- `4 → 1`: jump directly to ground state, emitting Lyman-gamma (ultraviolet)

The visible Balmer series lines you'd see include:
- `4 → 2`: blue-green (486 nm, H-beta)
- `3 → 2`: red (656 nm, H-alpha, from the cascade)

The ultraviolet Lyman series includes:
- `4 → 1`: ultraviolet
- `3 → 1`: ultraviolet

### Answer 1.4

**a)** The interference pattern is **destroyed**. You get two simple bands (like marbles through two slits), not the wavy interference pattern.

**b)** No! Even an *ideal* detector destroys the pattern. The act of gaining which-path information — even in principle — collapses the superposition. You cannot have definite path information *and* an interference pattern at the same time. This is a fundamental limit, not a technological limitation.

**c)** Remarkably, **yes!** Quantum eraser experiments have confirmed this. If you arrange the experiment so that the which-path information is irreversibly erased before you examine the detector records, the interference pattern is restored. This has been demonstrated with photons in real labs. The quantum system doesn't "know" you looked — it only responds to whether the information *exists* in the universe.

### Answer 1.5

The light bulb analogy is a **classical mixture**, not a quantum superposition. If you simply don't know whether the bulb is on or off, the bulb is *definitely* in one state or the other — you just lack information.

A true quantum superposition is different: the system genuinely occupies *both* states simultaneously, and the amplitudes from both states can **interfere** with each other. If you had two slightly different superpositions and combined them, they could add up constructively (like ocean waves) or destructively (canceling each other out). A classical "unknown" can't do that — either the bulb is on or it isn't, and the probabilities just add.

The key test: can you observe interference? If yes, it's a quantum superposition, not classical ignorance.

</details>
