# Bernstein–Vazirani Algorithm

The **Bernstein–Vazirani (BV)** algorithm is a quantum algorithm that determines a hidden bit string `s` using only **one query** to an oracle, while a classical algorithm would require `n` queries for an `n`-bit string.

---

## 📜 Problem Statement

We are given a function:
Where:
- `x` is an n-bit input.
- `s` is a secret n-bit string.
- `·` denotes the bitwise dot product mod 2.

Our task: **Find `s`**.

---

## ⚙ How the Algorithm Works

1. **Initialization**
   - Start with `n` qubits in `|0⟩` and 1 ancilla qubit in `|1⟩`.

2. **Hadamard Transformation**
   - Apply **H** gates to all qubits (including ancilla).

3. **Oracle Query**
   - The oracle flips the phase of the state depending on the value of `s · x`.

4. **Hadamard Transformation (again)**
   - Apply **H** gates to the first `n` qubits (ignore the ancilla for this step).

5. **Measurement**
   - Measure the first `n` qubits → the result is the secret string `s`.
