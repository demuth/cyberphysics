---
title: "Quantum Cryptography and the Physics of Secure Communication"
teaching: 0
exercises: 0
questions:
- "Key question (FIXME)"
objectives:
- "First learning objective. (FIXME)"
keypoints:
- "First key point. Brief Answer to questions. (FIXME)"
---

# **Quantum Cryptography and the Physics of Secure Communication**  

## **1. Introduction**  
Quantum cryptography leverages the **laws of quantum mechanics** to achieve **unbreakable encryption** and **secure communication**. Unlike classical cryptography, which relies on mathematical complexity, quantum cryptography is rooted in **the fundamental principles of physics**, making it resistant to computational attacks, including those from quantum computers.  

🚀 **Key Concept**: **Quantum Key Distribution (QKD)** is the most well-known quantum cryptographic technique, ensuring that eavesdropping is **physically detectable**.  

---

## **2. Physics Principles Behind Quantum Cryptography**  

### **2.1 The Heisenberg Uncertainty Principle**  
🔹 States that **measuring a quantum system inevitably disturbs it**.  
🔹 If an eavesdropper (Eve) tries to intercept a quantum transmission, the system will change, alerting legitimate users.  

🔹 **Mathematical Formulation:**  
\[
\Delta x \cdot \Delta p \geq \frac{\hbar}{2}
\]
- Any attempt to measure quantum states introduces **uncertainty**, which can be detected in secure communication.  

---

### **2.2 Quantum Superposition and Qubits**  
🔹 **Qubits (Quantum Bits)** can exist in **multiple states simultaneously** (unlike classical bits, which are 0 or 1).  
🔹 **Encoding information in qubits** enables new forms of cryptographic protocols.  

🔹 **Example: Quantum Bit Representation**  
\[
|\psi\rangle = \alpha |0\rangle + \beta |1\rangle
\]
where \( \alpha \) and \( \beta \) are probability amplitudes.  

🚀 **Benefit**: **Impossible to clone an unknown quantum state** (**No-Cloning Theorem**), preventing attackers from copying qubits undetected.  

---

### **2.3 Quantum Entanglement**  
🔹 When two particles are **entangled**, their states are **instantaneously correlated**, no matter the distance.  
🔹 This enables **secure key exchanges** over long distances.  

🔹 **Mathematical Formulation (Bell States Example):**  
\[
|\Phi^+\rangle = \frac{1}{\sqrt{2}}(|00\rangle + |11\rangle)
\]
- If one qubit is measured, the other’s state **is instantly determined**.  

🚀 **Benefit**: **Eavesdropping disrupts entanglement**, making detection possible.  

---

## **3. Quantum Cryptographic Techniques**  

### **3.1 Quantum Key Distribution (QKD)**  
QKD allows two parties (Alice & Bob) to securely exchange cryptographic keys using quantum mechanics.  

🔹 **BB84 Protocol (Bennett & Brassard, 1984)** – Uses quantum states to encode bits:  
1. Alice sends **randomly polarized photons** to Bob.  
2. Bob measures them using a random basis.  
3. If Eve intercepts, the measurement changes, exposing eavesdropping.  

🔹 **Ekert91 Protocol** – Uses quantum entanglement to detect eavesdropping via **Bell's Theorem**.  

🚀 **Security Advantage**: QKD is **information-theoretically secure**—even quantum computers **cannot break it**.  

---

### **3.2 Post-Quantum Cryptography (PQC)**  
🔹 While QKD relies on quantum mechanics, **post-quantum cryptography** (PQC) is based on **mathematically hard problems** that even quantum computers struggle with (e.g., lattice-based encryption).  
🔹 Examples: **CRYSTALS-Kyber**, **NTRUEncrypt**.  

🚀 **Future-Proofing Security**: PQC ensures classical networks remain secure **even against quantum attacks**.  

---

## **4. Real-World Applications of Quantum Cryptography**  
🔹 **Government & Military**: Quantum-secured networks for classified communications.  
🔹 **Financial Institutions**: Quantum-safe transactions to prevent future hacking.  
🔹 **Satellite-Based QKD**: China’s **Micius satellite** demonstrated global quantum encryption.  

---

## **5. Conclusion**  
Quantum cryptography **fundamentally changes cybersecurity** by using **laws of physics** rather than computational difficulty.  

✅ **Key Takeaways:**  
- **Heisenberg’s Uncertainty Principle & No-Cloning Theorem** ensure **undetectable eavesdropping**.  
- **Quantum Key Distribution (QKD)** enables **unbreakable encryption**.  
- **Quantum entanglement & superposition** provide unique cryptographic advantages.  
- **Post-Quantum Cryptography (PQC)** is crucial for protecting classical networks from **future quantum threats**.  

📡 **Next Steps**: Would you like a deeper dive into **quantum-resistant encryption algorithms or real-world QKD implementations?** 🚀

{% include links.md %}
