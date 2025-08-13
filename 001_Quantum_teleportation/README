# Quantum Teleportation

Quantum teleportation is a protocol that transfers an unknown quantum state from one qubit (Alice) to another qubit (Bob), using quantum entanglement and classical communication.  
The original state is destroyed on Alice's side and recreated exactly on Bob's side.

---

## 📜 How It Works

1. **Prepare the state to teleport**  
   - Qubit `q0` holds the unknown state |ψ⟩ we want to teleport.

2. **Create entanglement between `q1` and `q2`**  
   - Apply **H** on `q1`  
   - Apply **CNOT** with `q1` as control, `q2` as target  
   - This creates the Bell state: (|00⟩ + |11⟩) / √2

3. **Bell measurement on Alice's qubits (`q0` and `q1`)**  
   - Apply **CNOT** with `q0` as control, `q1` as target  
   - Apply **H** on `q0`  
   - Measure both `q0` → classical bit `c0`, and `q1` → classical bit `c1`

4. **Classical corrections on Bob's qubit (`q2`)**  
   - If `c1 = 1` → apply **X** on `q2`  
   - If `c0 = 1` → apply **Z** on `q2`

5. **Result**  
   - After corrections, `q2` contains the original |ψ⟩ state.
