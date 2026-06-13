---
title: "Chapter 5: Entanglement"
---

# 5. Quantum Entanglement

Einstein famously called it "spooky action at a distance." Quantum entanglement is arguably the most profoundly strange phenomenon in physics, yet it is completely real and forms the basis for quantum teleportation, quantum cryptography, and quantum computing.

## 5.1 What is Entanglement?

In Chapter 4, we learned about superpositions of single qubits. Now, imagine we have **two** qubits. 

Classically, the state of the first coin (heads or tails) and the state of the second coin are independent. But in the quantum world, two qubits can be combined in such a way that their states are **inextricably linked**, no matter how far apart they are.

For example, consider the **Bell State**:
$$|\Phi^+\rangle = \frac{1}{\sqrt{2}} (|00\rangle + |11\rangle)$$

In this state, the two qubits do not have individual, well-defined states. They exist in a combined superposition. 

- If you measure the first qubit and find it in state $|0\rangle$, the second qubit is **instantaneously** guaranteed to also be in state $|0\rangle$. 
- If you measure the first qubit and find it in state $|1\rangle$, the second qubit is instantly $|1\rangle$.

This correlation happens faster than the speed of light, even if the two qubits are light-years apart!

## 5.2 Bell's Theorem

Albert Einstein, Boris Podolsky, and Nathan Rosen (EPR) thought this "spooky action" meant quantum mechanics was incomplete. They proposed that there must be "hidden variables" that were decided when the particles were created, and the particles just look like they communicate instantly.

In 1964, physicist John Bell came up with a mathematical theorem to test this. He showed that if the universe worked using hidden variables (like the EPR paradox suggested), certain correlations between measurements could not exceed a specific limit (Bell's Inequality).

Decades of experiments have since shown that **Bell's Inequality is violated**. The universe truly is "non-local" in the quantum sense. There are no hidden variables; the particles really do decide their states at the exact moment of measurement, and they really are instantly correlated.

## 5.3 Applications of Entanglement

Far from just being a philosophical puzzle, entanglement is a resource:
- **Quantum Computing**: Entangled qubits allow quantum computers to perform massively parallel calculations, vastly outperforming classical supercomputers on specific tasks.
- **Quantum Cryptography**: Entanglement can be used to generate secure encryption keys. Any attempt to eavesdrop on the key distribution will destroy the entanglement, instantly alerting the users to the intrusion.

## Conclusion

You've made it through a whirlwind tour of the quantum world! From wave-particle duality to Schrödinger's wave functions, from spin to entanglement, you now have the conceptual and basic mathematical tools to explore deeper into quantum physics and quantum computing.
