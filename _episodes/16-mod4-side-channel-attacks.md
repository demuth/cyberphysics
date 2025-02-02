---
title: "Side Channel Attacks using Electromagnetic Emissions"
teaching: 0
exercises: 0
questions:
- "Key question (FIXME)"
objectives:
- "First learning objective. (FIXME)"
keypoints:
- "First key point. Brief Answer to questions. (FIXME)"
---

# **Side-Channel Attacks Using Electromagnetic (EM) Emissions**  

## **1. Introduction to Side-Channel Attacks (SCAs)**  
Side-channel attacks (SCAs) exploit **unintended physical emissions** from electronic devices to extract **sensitive information** such as cryptographic keys, passwords, or data being processed. Among the various types of SCAs, **electromagnetic (EM) emissions attacks** are particularly concerning because they can be **conducted remotely and non-invasively**.  

### **🔴 Why Are EM Emissions a Security Risk?**  
- **Electronic circuits emit electromagnetic radiation** during operation.  
- **Attackers can capture and analyze these emissions** to infer secret data.  
- **No need for physical access**—attacks can be executed from a distance.  

📡 **Common Targets:**  
- Cryptographic hardware (AES, RSA, ECC)  
- Secure microcontrollers (TPMs, smart cards, HSMs)  
- Keyboards, monitors, and processors  
- IoT and embedded systems  

---

## **2. How Electromagnetic Side-Channel Attacks Work**  

### **2.1 Principles of EM Emission Attacks**  
Every electronic device produces **unintentional electromagnetic (EM) signals** due to the switching of transistors and power fluctuations. By capturing these signals using specialized hardware, an attacker can infer:  

✔ **Encryption keys from cryptographic processors**  
✔ **Keystrokes from keyboards (remote keylogging)**  
✔ **Data from air-gapped systems**  
✔ **Screen contents from unshielded monitors**  

### **2.2 Attack Process**  

1️⃣ **Signal Collection**  
   - Attacker places an **antenna or Software-Defined Radio (SDR)** near the target.  
   - Captures EM emissions **passively (eavesdropping)** or **actively (probing with RF signals)**.  

2️⃣ **Signal Processing**  
   - Uses **Fourier Transform & Machine Learning** to analyze signal patterns.  
   - Filters out noise to **isolate useful emissions** related to cryptographic computations or keystrokes.  

3️⃣ **Data Extraction**  
   - Recovers **encryption keys, passwords, or processed data**.  
   - Uses **statistical methods & machine learning** to refine results.  

---

## **3. Types of Electromagnetic Side-Channel Attacks**  

### **3.1 Cryptographic Key Extraction Attacks**  
🔹 **Principle**: Extract secret cryptographic keys from electromagnetic emissions of hardware performing encryption.  

| **Attack Type** | **Targeted Algorithm** | **Impact** |  
|---------------|----------------------|------------|  
| **TEMPEST (Van Eck Phreaking)** | RSA, AES, ECC, DES | Extracts private keys from CPUs & FPGAs |  
| **Simple EM Analysis (SEMA)** | AES, RSA | Reads EM fluctuations to infer key operations |  
| **Differential EM Analysis (DEMA)** | AES, ECC | Uses statistical correlation to recover full keys |  

📌 **Example:**  
- Researchers have successfully extracted **AES-128 encryption keys** from smartcards by analyzing EM emissions during computation.  

✅ **Defense:**  
✔ **Electromagnetic shielding (Faraday cages, TEMPEST-rated enclosures)**  
✔ **Side-channel hardened cryptographic algorithms**  
✔ **Randomized power consumption (masking techniques)**  

---

### **3.2 Keystroke & Data Leakage Attacks**  
🔹 **Principle**: Capture unintended EM emissions from keyboards, monitors, or processors to recover sensitive information.  

| **Attack Type** | **Targeted Device** | **Impact** |  
|---------------|----------------|------------|  
| **Keystroke Emanation Attack** | Wired & Wireless Keyboards | Remote keylogging via RF analysis |  
| **Monitor Emanation Attack** | LCD/CRT Screens | Reads screen contents from RF emissions |  
| **Processor Timing Attack** | CPUs | Infers processed data based on EM fluctuations |  

📌 **Example:**  
- **Keylogging via EM Analysis**:  
   - Researchers demonstrated that **low-cost SDRs** can capture **keystrokes from wired keyboards** by analyzing emitted RF signals.  
   - Attackers can recover **typed passwords, emails, and banking credentials**.  

✅ **Defense:**  
✔ **Use shielded keyboards (e.g., military-grade TEMPEST keyboards)**  
✔ **Employ randomized keyboard signal processing**  
✔ **Use noise generation to obfuscate real signals**  

---

### **3.3 Air-Gap Bypass Attacks Using EM Emissions**  
🔹 **Principle**: Extract data from air-gapped computers by exploiting electromagnetic emissions.  

| **Attack Type** | **How It Works** | **Impact** |  
|---------------|----------------|------------|  
| **AirHopper Attack** | Uses VGA cable emissions to transmit data to a nearby attacker | Leaks sensitive screen data from air-gapped systems |  
| **GSMem Attack** | Uses memory bus EM emissions to send data to a nearby mobile phone | Exfiltrates classified data from air-gapped networks |  
| **TempestSDR Attack** | Uses Software-Defined Radio (SDR) to capture leaked data | Extracts information from isolated computers |  

📌 **Example:**  
- **AirHopper (Ben-Gurion University, 2014)**:  
   - Researchers showed that **malware could use VGA cables** as an **RF transmitter** to leak data from **air-gapped systems** to nearby receivers.  

✅ **Defense:**  
✔ **Use TEMPEST-certified shielding for sensitive environments**  
✔ **Deploy RF jamming & anomaly detection for unauthorized emissions**  
✔ **Monitor and control unauthorized hardware connections**  

---

## **4. Tools Used in EM Side-Channel Attacks**  

| **Tool** | **Purpose** |  
|----------|------------|  
| **HackRF One** | Captures and transmits RF signals |  
| **Software-Defined Radios (RTL-SDR, USRP, LimeSDR)** | EM signal eavesdropping and analysis |  
| **TEMPESTSDR** | Decodes leaked electromagnetic emissions from monitors |  
| **Open-source tools (ChipWhisperer, Riscure Inspector)** | Cryptographic side-channel analysis |  

---

## **5. Countermeasures Against EM Side-Channel Attacks**  

🔒 **Hardware-Level Protections**  
✔ Use **electromagnetic shielding (Faraday cages, conductive enclosures)**.  
✔ Employ **power and signal masking techniques** to prevent leakage.  
✔ Implement **randomized execution patterns in cryptographic algorithms**.  

🔒 **Software-Level Protections**  
✔ Use **constant-time cryptographic computations** to avoid EM leakage.  
✔ Implement **noise injection & signal obfuscation** techniques.  

🔒 **Network & Physical Security**  
✔ Deploy **RF jamming and spectrum monitoring systems**.  
✔ Restrict the use of **unsecured wireless peripherals (Bluetooth, RFID, NFC)**.  

---

## **6. Conclusion**  
Electromagnetic side-channel attacks **pose a serious cybersecurity risk** to cryptographic systems, secure computing environments, and air-gapped networks. Attackers can extract **encryption keys, passwords, and sensitive data** using **passive EM monitoring or active RF probing**.  

✅ **Key Takeaways:**  
- **EM emissions can be exploited to break encryption & capture keystrokes.**  
- **SDRs & advanced signal processing make these attacks accessible.**  
- **Defenses require a combination of shielding, encryption hardening, and noise injection.**  

📡 **Next Steps**: Would you like a detailed breakdown of **TEMPEST attacks, real-world case studies, or hands-on demonstrations with SDR tools?** 🚀
