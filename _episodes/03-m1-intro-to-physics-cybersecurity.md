---
title: "Introduction to Physics Cybersecurity"
teaching: 0
exercises: 0
questions:
- "Key question (FIXME)"
objectives:
- "First learning objective. (FIXME)"
keypoints:
- "First key point. Brief Answer to questions. (FIXME)"
---

### Module 1: Introduction to Physics Cybersecurity ###

Cybersecurity threats involving physics often exploit physical principles to compromise systems. Here are some key threats:

### **1. Electromagnetic Eavesdropping (TEMPEST Attacks)**
   - Electromagnetic emissions from electronic devices (monitors, keyboards, processors) can be intercepted remotely.
   - Attackers can reconstruct signals from unintentional emissions.
   - Countermeasures: Shielding, Faraday cages, and secure hardware designs.

### **2. Radio Frequency (RF) Hacking**
   - Unauthorized access to wireless communications (WiFi, Bluetooth, RFID).
   - RF jamming attacks disrupt signals and prevent communication.
   - Software-Defined Radios (SDR) can be used for signal interception and manipulation.
   - Countermeasures: Encryption, frequency hopping, and anti-jamming techniques.

### **3. Acoustic Side-Channel Attacks**
   - Sounds emitted by keyboards, printers, or hard drives can be analyzed to infer data.
   - Attackers can use sensitive microphones or AI models to reconstruct typed passwords.
   - Countermeasures: Noise generators, soundproofing, and randomized typing patterns.

### **4. Power Analysis Attacks**
   - Monitoring power consumption variations to extract encryption keys.
   - Used in cryptographic attacks like Differential Power Analysis (DPA).
   - Countermeasures: Power obfuscation techniques, secure cryptographic implementations.

### **5. Laser-Based Attacks**
   - Lasers can be used to inject signals into electronic circuits remotely (e.g., attacking voice assistants via MEMS microphones).
   - Optical sensors in cameras or other devices can be blinded or manipulated.
   - Countermeasures: Optical shielding, secure microphone designs.

### **6. Electromagnetic Interference (EMI) Attacks**
   - Inducing faults in electronic systems using electromagnetic pulses (e.g., hardware glitches, data corruption).
   - Intentional EMI attacks can crash systems or disrupt critical infrastructure.
   - Countermeasures: Shielding, EMI-resistant hardware, and redundancy.

### **7. Thermal Side-Channel Attacks**
   - Thermal residue left on keypads or touchscreens can reveal passwords.
   - Attackers use thermal cameras to analyze heat signatures.
   - Countermeasures: Randomized touch interactions, heat-resistant keypads.

### **8. Hardware Trojans & Supply Chain Attacks**
   - Malicious modifications in hardware during manufacturing.
   - Exploits could enable remote control, data leaks, or system sabotage.
   - Countermeasures: Secure supply chains, hardware verification techniques.

{% include links.md %}
