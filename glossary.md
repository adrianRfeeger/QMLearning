---
title: Glossary of Key Terms
---

# Glossary of Key Terms

This glossary collects every important term you'll encounter in this book. Each term is linked to the chapter where it's introduced.

---

## A

**Amplitude** (Ch. 3, 4)
A complex number that describes the "weight" of a quantum state. The probability of measuring a particular outcome is the *square of the magnitude* of its amplitude. Think of it like the "loudness" of a wave — but with a direction (phase) as well as a size.

**Anticommuting** (Ch. 4, 6)
Two operations anticommute if doing A then B gives the opposite result of doing B then A. The Pauli X and Z gates anticommute: `XZ = -ZX`.

## B

**Bell State** (Ch. 5)
One of four special entangled states of two qubits. They are `|Φ⁺⟩`, `|Φ⁻⟩`, `|Ψ⁺⟩`, and `|Ψ⁻⟩`. Each represents perfect correlation or anti-correlation between the two qubits.

**Bell's Inequality** (Ch. 5)
A mathematical limit (`|S| ≤ 2`) that any "local hidden variable" theory must obey. Quantum mechanics predicts values larger than 2, which experiments have confirmed.

**Bloch Sphere** (Ch. 4)
A 3D sphere that visualizes all possible states of a single qubit. The north pole is `|0⟩`, the south pole is `|1⟩`, and points on the equator represent superpositions. Rotations of the sphere correspond to quantum gates.

**Born's Rule** (Ch. 2, 3)
The rule that says the probability of an outcome is the square of the amplitude's magnitude: `P = |amplitude|²`. This connects the mathematics of quantum mechanics to actual measurements.

## C

**CNOT Gate** (Ch. 4, 5)
A two-qubit gate that flips the second (target) qubit if and only if the first (control) qubit is `|1⟩`. It's the simplest way to create entanglement.

**Complex Conjugate** (Ch. 2)
For a complex number `a + bi`, the conjugate is `a - bi`. If you multiply a complex number by its conjugate, you get a real number: `|z|² = z × z*`.

**Complex Number** (Ch. 2)
A number of the form `a + bi`, where `a` and `b` are real numbers and `i = √(-1)`. Complex numbers live on a 2D plane and are essential for describing quantum states.

**Computational Basis** (Ch. 4)
The standard pair of states `{|0⟩, |1⟩}` for a qubit, analogous to 0 and 1 in classical computing.

## D

**Deterministic** (Ch. 1)
A process is deterministic if the same input always produces the same output with no randomness. Classical physics is deterministic; quantum measurement is not.

## E

**Eigenvalue** (Ch. 2, 3)
When a matrix acts on a special vector (the eigenvector), it just scales it by a number — that number is the eigenvalue. The Schrödinger equation is an eigenvalue problem: applying the Hamiltonian to a state gives the energy eigenvalue times that state.

**Eigenvector** (Ch. 2, 3)
A vector that, when a matrix acts on it, only gets stretched (not rotated). In quantum mechanics, eigenvectors of an operator correspond to states with definite values for that observable.

**Entanglement** (Ch. 4, 5)
A quantum phenomenon where two or more particles have correlations that cannot be explained by independent states for each particle. Measurements on entangled particles are strongly correlated, but those correlations cannot be used for faster-than-light communication.

**Euler's Identity** (Ch. 2)
The equation `e^(iπ) + 1 = 0`, which connects five of the most important numbers in mathematics: 0, 1, e, i, and π. It's a special case of Euler's formula: `e^(iθ) = cos(θ) + i·sin(θ)`.

## G

**Grover's Algorithm** (Ch. 6)
A quantum search algorithm that finds a marked item in an unsorted database of N items using only O(√N) operations — a quadratic speedup over classical O(N). It uses amplitude amplification (oracle + diffusion operator) to iteratively increase the probability of measuring the target state.

**GHZ State** (Ch. 5)
A maximally entangled state of three or more qubits: `|GHZ⟩ = (|000⟩ + |111⟩)/√2`. Measuring any one qubit fixes the correlated outcomes for the others, demonstrating genuine multipartite entanglement.

## H

**Hamiltonian** (Ch. 3)
The operator representing the total energy (kinetic + potential) of a quantum system. The Schrödinger equation says `H|ψ⟩ = E|ψ⟩`: applying the Hamiltonian to a state gives the energy of that state.

**Hadamard Gate** (Ch. 4)
A quantum gate that creates superposition. `H|0⟩ = |+⟩ = (|0⟩ + |1⟩)/√2`. It performs a 180° rotation around the (X+Z)/√2 axis on the Bloch sphere. Applying H twice returns to the original state: `H² = I`.

**Heisenberg Uncertainty Principle** (Ch. 3)
You cannot simultaneously know both the exact position and exact momentum of a particle. The more precisely you know one, the less precisely you know the other: `Δx · Δp ≥ ℏ/2`.

**Hidden Variables** (Ch. 5)
Hypothetical underlying properties that would determine quantum outcomes in advance. Bell's theorem and its experimental verification ruled out *local* hidden variable theories.

## I

**Identity Matrix** (Ch. 2)
A square matrix with 1s on the diagonal and 0s elsewhere. Multiplying any vector by the identity matrix gives the same vector back: `I·v = v`.

**Inner Product** (Ch. 2)
A way of "multiplying" two vectors to get a single number. For vectors `[a, b]` and `[c, d]`, the inner product is `ac + bd` (with complex conjugation for complex numbers). It measures how much the vectors point in the same direction.

## K

**Kronecker Product** (Ch. 2, 4)
A way to combine two matrices (or vectors) into a larger one. For qubits, the Kronecker product (`⊗`) combines single-qubit states into multi-qubit states: `|0⟩ ⊗ |1⟩ = |01⟩`.

## M

**Matrix** (Ch. 2)
A rectangular grid of numbers. In quantum mechanics, matrices represent operations (gates) that transform quantum states.

**Measurement** (Ch. 1, 3, 4)
The process of extracting information from a quantum system. Measurement forces the system into a definite state and produces a random outcome with probabilities given by Born's rule. After measurement, the original quantum state is destroyed.

**Normalization** (Ch. 2, 3)
Scaling a quantum state so that the total probability equals 1. If a state has components with amplitudes `α` and `β`, it's normalized when `|α|² + |β|² = 1`.

## O

**Observables** (Ch. 2, 3)
Physical quantities that can be measured, like position, momentum, spin, or energy. In quantum mechanics, observables are represented by matrices (operators).

**Oracle** (Ch. 6)
A "black box" function used in quantum algorithms that computes a specific function on input states. In Grover's algorithm, the oracle marks the target state by flipping its phase. In Deutsch-Jozsa, it evaluates the function being tested.

## P

**Photon** (Ch. 1)
A particle of light. Photons carry discrete packets of energy: `E = hf` (where `h` is Planck's constant and `f` is frequency).

**Pauli Gates** (Ch. 4)
Three fundamental quantum gates represented by the Pauli matrices:
- **X** (NOT gate): flips `|0⟩ ↔ |1⟩`
- **Y**: combines X and Z effects with a phase
- **Z**: flips the phase of `|1⟩` without changing `|0⟩`

**Probability Amplitude** (Ch. 2, 3)
A complex number whose squared magnitude gives the probability of an outcome. This is the core of quantum probability — amplitudes can interfere (add or cancel), unlike classical probabilities.

**Qubit** (Ch. 4)
The basic unit of quantum information. Like a classical bit, it has two basis states `|0⟩` and `|1⟩`, but it can also exist in any superposition `α|0⟩ + β|1⟩`.

**Quantum Error Correction** (Ch. 6)
Techniques to protect quantum information from decoherence and noise. The 3-qubit bit-flip code encodes one logical qubit into three physical qubits, detecting and correcting single bit-flip errors.

**Quantum Fourier Transform (QFT)** (Ch. 6)
The quantum analogue of the classical discrete Fourier transform. It maps `|x⟩ → (1/√N)Σ_y exp(2πixy/N)|y⟩`. The QFT can be implemented efficiently on amplitudes stored in a quantum state and is a key subroutine in phase estimation and Shor's factoring algorithm.

**Quantum Gate** (Ch. 4)
An operation that transforms one or more qubits. Gates are represented by unitary matrices (matrices that preserve total probability).

**Quantum State** (Ch. 1, 4)
A complete mathematical description of a quantum system. For a qubit, it's a vector in complex space. The quantum state encodes all the probabilities for possible measurement outcomes.

## S

**Schrödinger Equation** (Ch. 3)
The fundamental equation of quantum mechanics: `iℏ ∂ψ/∂t = Ĥψ`. It describes how quantum states evolve over time. For stationary states: `Ĥψ = Eψ`.

**Superposition** (Ch. 1, 4)
The principle that a quantum system can exist in multiple states simultaneously. A qubit in the state `α|0⟩ + β|1⟩` is *both* 0 and 1 until measured. This is not just "we don't know which" — it genuinely exists in both states at once.

## T

**Tensor Product** (Ch. 2, 4)
See **Kronecker Product**. It's how we combine quantum systems: two qubits are described by the tensor product of their individual states, creating a 4-dimensional state space.

**Tunneling** (Ch. 3)
A quantum phenomenon where a particle passes through a potential barrier even though its energy is lower than the barrier height. The wavefunction decays exponentially inside the barrier, and a non-zero amplitude survives to the other side. Used in STM microscopes, flash memory, and alpha decay.

## U

**Unitary Matrix** (Ch. 2, 4)
A matrix `U` where `U†U = I` (the conjugate transpose times the matrix equals the identity). Unitary matrices preserve the length of vectors, which means they preserve total probability. All quantum gates are unitary.

**Uncertainty Principle** (Ch. 3)
See **Heisenberg Uncertainty Principle**. It's a fundamental limit, not a limitation of measurement tools.

## W

**Wave Function** (Ch. 1, 3)
The quantum state of a particle in position space, usually denoted by Ψ (Psi) or ψ. Its squared magnitude `|ψ(x)|²` gives the probability density of finding the particle at position `x`.

**Wave-Particle Duality** (Ch. 1)
The phenomenon that quantum entities (electrons, photons, etc.) exhibit both wave-like properties (interference, diffraction) and particle-like properties (localized detection).

---

## How to Use This Glossary

- Terms are ordered alphabetically for quick lookup
- The chapter in parentheses tells you where to find the full explanation
- If you encounter an unfamiliar term, come back here
- For deep understanding, revisit the original chapter
