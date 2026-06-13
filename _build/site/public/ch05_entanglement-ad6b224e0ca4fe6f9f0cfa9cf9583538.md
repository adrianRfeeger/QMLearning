---
title: "Chapter 5 — Entanglement"
---

# Chapter 5: Entanglement

In the previous chapters, we explored how single qubits behave and how they can be manipulated using quantum gates. However, the most profound feature of quantum mechanics—and the one that provides the most power to quantum computers—is **entanglement**.

Albert Einstein famously referred to entanglement as *"spooky action at a distance."* While it seems paradoxical, it is a rigorous mathematical consequence of the tensor product structure of multi-qubit systems.

## 5.1 What is Entanglement?

A state of a multi-qubit system is **entangled** if it cannot be written as a product of the states of its individual qubits.

### Product States (Separable)
If we have two qubits, and the total state $|\Psi\rangle$ can be written as:
$$|\Psi\rangle = |\psi\rangle_A \otimes |\phi\rangle_B$$
then the state is **separable**. In a separable state, measuring qubit A tells you nothing about the state of qubit B. They are independent.

### Entangled States
If no such decomposition exists, the state is **entangled**. In an entangled state, the qubits share a collective identity. Measuring one qubit *instantly* collapses the state of the other, regardless of how far apart they are.

---

## 5.2 The Bell States

The most famous examples of entanglement are the four **Bell states** (or EPR pairs). These are maximally entangled states of two qubits.

The most common Bell state is $|\Phi^+\rangle$:
$$|\Phi^+\rangle = \frac{1}{\sqrt{2}}(|00\rangle + |11\rangle)$$

**Why is this entangled?**
If you measure the first qubit and get $|0\rangle$, the total state collapses to $|00\rangle$, meaning the second qubit *must* be $|0\rangle$. If you get $|1\rangle$, the second *must* be $|1\rangle$. They are perfectly correlated.

### Creating a Bell State
You can create $|\Phi^+\rangle$ using a Hadamard gate and a CNOT gate:
1. Start with $|00\rangle$.
2. Apply $H$ to the first qubit $\rightarrow \frac{1}{\sqrt{2}}(|0\rangle + |1\rangle)|0\rangle = \frac{1}{\sqrt{2}}(|00\rangle + |10\rangle)$.
3. Apply $\text{CNOT}_{0 \to 1} \rightarrow \frac{1}{\sqrt{2}}(|00\rangle + |11\rangle)$.

---

## 5.3 The EPR Paradox and Bell's Inequality

In 1935, Einstein, Podolsky, and Rosen (EPR) argued that quantum mechanics must be incomplete. They suggested there were "hidden variables"—pre-determined values—that decided the measurement outcomes, avoiding the need for "spooky action."

### Bell's Theorem
In 1964, John Bell proved that no theory of local hidden variables could reproduce all the predictions of quantum mechanics. He derived **Bell's Inequalities**, which provide a mathematical limit on the correlations possible in any classical (local) system.

Quantum mechanics violates these inequalities. Experimental tests (like the CHSH experiment) have consistently shown that nature is indeed non-local in the quantum sense.

---

## 5.4 Quantum Teleportation

Entanglement allows us to move a quantum state from one location to another without physically moving the particle. This is **Quantum Teleportation**.

**The Setup:**
- Alice wants to send an unknown state $|\psi\rangle$ to Bob.
- Alice and Bob share a Bell pair $|\Phi^+\rangle$.

**The Process:**
1. Alice performs a Bell measurement on her unknown qubit and her half of the Bell pair.
2. This measurement collapses Bob's qubit into a state that is a rotated version of $|\psi\rangle$.
3. Alice sends two classical bits to Bob telling him which rotation occurred.
4. Bob applies the corresponding gate ($I, X, Z,$ or $XZ$) to recover $|\psi\rangle$.

*Note: This does not allow faster-than-light communication because Alice must send the classical bits at the speed of light.*

---

## 5.5 Multi-Qubit Entanglement: GHZ States

Entanglement isn't limited to two qubits. The **GHZ state** (Greenberger-Horne-Zeilinger) is a maximally entangled state of three or more qubits:
$$|GHZ\rangle = \frac{1}{\sqrt{2}}(|000\rangle + |111\rangle)$$

GHZ states demonstrate "genuine tripartite entanglement," where the correlation is shared across all three particles simultaneously.

---

## 5.6 Quantum Cryptography (QKD)

Entanglement provides a way to communicate with absolute security. In **Quantum Key Distribution (QKD)**, such as the Ekert91 protocol:
- Alice and Bob share entangled pairs.
- They measure them in random bases.
- Because of Bell's theorem, any attempt by an eavesdropper (Eve) to intercept the qubits will disturb the entanglement and introduce errors.
- Alice and Bob can detect Eve simply by checking if Bell's inequality is still violated.

---

## 5.7 Summary Table

| Concept | Key Idea | Mathematical Form / Tool |
| :--- | :--- | :--- |
| **Separable State** | Independent qubits | $|\psi\rangle \otimes |\phi\rangle$ |
| **Entangled State** | Correlated qubits | Cannot be factored |
| **Bell States** | Max entanglement (2 qubits) | $\frac{1}{\sqrt{2}}(|00\rangle + |11\rangle)$ |
| **Bell's Theorem** | Proves non-locality | Violation of inequalities |
| **Teleportation** | Moving a state via entanglement | Bell measurement + Classical bits |
| **GHZ State** | Multi-qubit entanglement | $\frac{1}{\sqrt{2}}(|0\dots0\rangle + |1\dots1\rangle)$ |
