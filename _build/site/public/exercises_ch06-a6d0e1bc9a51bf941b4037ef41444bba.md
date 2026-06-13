---
title: "Chapter 6 — Exercises"
---

# Chapter 6 Exercises: Quantum Algorithms

---

## Exercises

### Exercise 6.1: The Deutsch-Jozsa Logic

In the Deutsch-Jozsa algorithm, we use a standard function oracle that maps $|x\rangle|y\rangle \to |x\rangle|y \oplus f(x)\rangle$. 

**Question:**
If we prepare the auxiliary qubit in the state $|-\rangle = \frac{1}{\sqrt{2}}(|0\rangle - |1\rangle)$, the oracle effectively performs:
$$U_f |x\rangle|-\rangle = (-1)^{f(x)} |x\rangle|-\rangle$$
Explain why this "phase kickback" is essential for the algorithm to work. How does it allow us to use interference in the final Hadamard step?

<details><summary>Click for answer</summary>

The phase kickback converts the output of the function $f(x)$ (which is stored in the auxiliary qubit) into a **phase** on the input state $|x\rangle$. 

Because the result is now in the phase, we can apply a final set of Hadamard gates. If $f(x)$ is constant, the phases are all the same, leading to constructive interference at $|0\rangle^{\otimes n}$. If $f(x)$ is balanced, the phases are split exactly 50/50 between $+1$ and $-1$, leading to complete destructive interference at $|0\rangle^{\otimes n}$, ensuring we measure something else.

</details>

---

### Exercise 6.2: Grover's Iteration Count

You are searching for a single target item in a database of $N = 1024$ items.

**Questions:**
a) How many qubits are required to represent this database?
b) Approximately how many Grover iterations $\approx \frac{\pi}{4}\sqrt{N}$ are needed to maximize the probability of finding the target?
c) What happens if you perform significantly more iterations than this optimal number?

<details><summary>Click for answer</summary>

a) $n = \log_2(1024) = 10$ qubits.

b) $\frac{\pi}{4}\sqrt{1024} = \frac{\pi}{4} \times 32 \approx 0.785 \times 32 \approx 25$ iterations.

c) The probability of measuring the target state will begin to **decrease**. Grover's algorithm is essentially a rotation in Hilbert space; if you rotate too far, you "overshoot" the target state and move back toward the uniform superposition.

</details>

---

### Exercise 6.3: QFT and Period Finding

The Quantum Fourier Transform (QFT) is the core of Shor's algorithm. 

**Question:**
If we have a quantum state that is a superposition of states with period $r$:
$$|\psi\rangle = \frac{1}{\sqrt{M}} \sum_{k=0}^{M-1} |kr + x_0\rangle$$
What does the QFT do to this state? Why is this useful for factoring numbers?

<details><summary>Click for answer</summary>

For a register of size $N$, the QFT transforms a state with period $r$ into a state where the probability amplitudes are concentrated near integer multiples of $N/r$. 

By measuring the output of the QFT, we obtain a value that is very close to $m \cdot (N/r)$. With a bit of classical post-processing (continued fractions), we can extract the exact value of $r$. Once we have the period $r$ of the function $f(x) = a^x \bmod N$, we can find the factors of $N$ using $\gcd(a^{r/2} \pm 1, N)$.

</details>

---

### Exercise 6.4: Quantum Error Correction (Bit-Flip)

Consider the 3-qubit bit-flip code: $|0_L\rangle = |000\rangle$ and $|1_L\rangle = |111\rangle$.

**Scenario:**
A noise event occurs, and the state becomes $|\psi_{noisy}\rangle = \alpha|100\rangle + \beta|011\rangle$.

**Questions:**
a) Which qubit suffered a bit-flip error?
b) How can we detect this without measuring the qubits directly (which would collapse $\alpha$ and $\beta$)?

<details><summary>Click for answer</summary>

a) **Qubit 0** suffered the flip. (The first qubit is flipped relative to the other two in both components of the superposition).

b) We measure **syndromes** (parity checks). 
- Check parity of Qubit 0 and 1: They are different $\rightarrow$ Error is in 0 or 1.
- Check parity of Qubit 1 and 2: They are the same $\rightarrow$ Error is not in 1 or 2.
- Conclusion: The error must be in Qubit 0.

By measuring $Z_0 Z_1$ and $Z_1 Z_2$, we find the error location without ever learning whether the state was $|0\rangle$ or $|1\rangle$.

</details>

---

### Exercise 6.5: Coding Challenge — Oracle Design

Write a Python function that creates a Grover oracle for $n=2$ qubits that marks the state $|11\rangle$. 

*Hint: The oracle should be a $4 \times 4$ matrix that is the identity, except for the element at index [3,3], which should be -1.*

<details><summary>Click for answer</summary>

```python
import numpy as np

def oracle_11():
    # Identity matrix for 2 qubits (4x4)
    oracle = np.eye(4, dtype=complex)
    # Mark state |11> (index 3) by flipping its phase
    oracle[3, 3] = -1
    return oracle

# Verification
target_state = np.array([0, 0, 0, 1]) # |11>
result = oracle_11() @ target_state
print(f"Result: {result}") 
# Expected: [0, 0, 0, -1]
```

</details>
