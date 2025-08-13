Superdense coding is a quantum communication protocol that allows the transmission of **two classical bits** of information by sending only **one qubit**, using pre-shared entanglement between the sender (Alice) and the receiver (Bob).

---

## 📜 How It Works

1. **Entanglement Setup**  
   - Alice and Bob share a Bell pair: (|00⟩ + |11⟩) / √2  
   - Alice holds `q0`, Bob holds `q1`.

2. **Encoding by Alice**  
   - Depending on the 2-bit message she wants to send, Alice applies one of the following gates to `q0`:

     | Classical bits | Gate applied on `q0` |
     |---------------|----------------------|
     | `00`          | Identity (I)         |
     | `01`          | X                    |
     | `10`          | Z                    |
     | `11`          | ZX (Z then X)        |

3. **Send Qubit**  
   - Alice sends her qubit `q0` to Bob.

4. **Decoding by Bob**  
   - Bob now has both qubits (`q0`, `q1`).
   - He applies **CNOT** (`q0` control, `q1` target)  
   - Then applies **H** on `q0`.
   - Finally, he measures both qubits to recover the 2 classical bits.
