---
title: "Software-Defined Radio for Signal Interception"
teaching: 0
exercises: 0
questions:
- "Key question (FIXME)"
objectives:
- "First learning objective. (FIXME)"
keypoints:
- "First key point. Brief Answer to questions. (FIXME)"
---

# **Software-Defined Radio (SDR) for Signal Interception**  

## **1. Introduction to Software-Defined Radio (SDR)**  
### **🔹 What is SDR?**  
Software-Defined Radio (SDR) is a **flexible radio communication system** where traditional hardware components (like mixers, filters, and amplifiers) are implemented via **software**. This allows for real-time **signal processing, interception, and manipulation** across a wide range of frequencies.  

📡 **Key Capabilities:**  
✔ **Intercept and analyze wireless signals** (WiFi, Bluetooth, GPS, RFID, cellular, etc.)  
✔ **Transmit, jam, or spoof radio signals**  
✔ **Perform security assessments of wireless networks**  
✔ **Conduct penetration testing & intelligence gathering**  

🛑 **Cybersecurity Concern**: SDR enables **passive eavesdropping, active jamming, replay attacks, and RF-based exploits**.  

---

## **2. How SDR Works for Signal Interception**  

### **2.1 SDR Components**  
An SDR system consists of:  

| **Component** | **Function** |  
|-------------|------------|  
| **Antenna** | Captures radio waves from the environment |  
| **RF Front-End** | Converts RF signals into digital form |  
| **Analog-to-Digital Converter (ADC)** | Digitizes analog signals for software processing |  
| **DSP (Digital Signal Processing)** | Extracts, analyzes, or modifies signals |  
| **Software Interface** | Controls frequency tuning, decoding, and demodulation |  

### **2.2 SDR Signal Interception Process**  
1️⃣ **Tuning**: The SDR tunes into a specific frequency range (e.g., 2.4 GHz for WiFi, 1090 MHz for aircraft ADS-B).  
2️⃣ **Capturing**: The antenna captures raw RF signals, and the SDR converts them into digital form.  
3️⃣ **Decoding & Demodulation**: Software tools process the signals to extract meaningful data (e.g., decrypting WiFi packets, listening to radio communications).  
4️⃣ **Analysis**: The attacker or researcher analyzes the captured data for vulnerabilities.  

---

## **3. SDR in Cybersecurity & Signal Interception**  

### **3.1 Passive RF Interception (Eavesdropping & Sniffing)**  
SDRs allow attackers to **listen to and decode unencrypted communications**, including:  

| **Targeted Signal** | **Vulnerability** | **SDR Tool** |  
|----------------|----------------|------------|  
| **WiFi (802.11)** | Capturing unencrypted packets | Aircrack-ng, Kismet |  
| **Bluetooth** | Sniffing unsecured Bluetooth devices | Ubertooth One |  
| **Cellular (GSM, LTE, 5G)** | IMSI catching & call interception | OpenBTS, IMSI-catcher |  
| **RFID & NFC** | Cloning RFID cards & eavesdropping | Proxmark3 |  
| **GPS Signals** | Spoofing GPS navigation | GPS-SDR-SIM |  

✅ **Defense**:  
✔ Use **end-to-end encryption (TLS, WPA3, AES-256)**.  
✔ Deploy **frequency-hopping spread spectrum (FHSS)**.  

---

### **3.2 Active SDR Attacks (Jamming, Spoofing & Replay Attacks)**  
SDRs can **transmit malicious signals** to disrupt or manipulate wireless communications.  

| **Attack Type** | **How It Works** | **Targeted Systems** |  
|--------------|----------------|------------------|  
| **WiFi Jamming** | Overloads 2.4 GHz / 5 GHz with interference | WiFi networks |  
| **GPS Spoofing** | Sends fake GPS coordinates | Drones, Vehicles |  
| **RFID Cloning** | Records and replays RFID signals | Access control, key fobs |  
| **IMSI Catching** | Tricks phones into connecting to rogue base stations | Mobile phones, IoT |  

📌 **Example**:  
- Using **HackRF One** to **jam WiFi or disrupt IoT devices**.  
- Using an **SDR-based IMSI catcher** to track mobile phones.  

✅ **Defense**:  
✔ **RF anomaly detection & signal authentication**.  
✔ **Use GPS receivers with multi-frequency & anti-spoofing tech**.  

---

### **3.3 Military & Intelligence Applications**  
SDRs are heavily used in **electronic warfare (EW), signals intelligence (SIGINT), and counterintelligence**.  

| **Use Case** | **Application** |  
|-------------|---------------|  
| **Electronic Warfare (EW)** | Jamming enemy radar & communications |  
| **Signals Intelligence (SIGINT)** | Intercepting military & diplomatic communications |  
| **Counter-Surveillance** | Detecting & neutralizing rogue SDR devices |  

---

## **4. Popular SDR Hardware & Software**  

### **4.1 Common SDR Devices**  

| **SDR Device** | **Frequency Range** | **Use Case** | **Price** |  
|--------------|----------------|------------|----------|  
| **RTL-SDR** | 500 kHz – 1.75 GHz | Basic RF monitoring, ADS-B, GSM | $20-$50 |  
| **HackRF One** | 1 MHz – 6 GHz | RF hacking, jamming, spoofing | $300 |  
| **LimeSDR** | 100 kHz – 3.8 GHz | Advanced RF experiments | $300-$500 |  
| **USRP (Ettus Research)** | DC – 6 GHz | Professional SIGINT, military use | $1,000+ |  

### **4.2 SDR Software for Cybersecurity & Hacking**  

| **Software** | **Purpose** |  
|------------|-----------|  
| **GNU Radio** | Open-source signal processing toolkit |  
| **SDR# (SDRSharp)** | Easy-to-use spectrum analysis tool |  
| **GQRX** | RF spectrum visualization & demodulation |  
| **Aircrack-ng** | WiFi interception & decryption |  
| **IMSI Catcher** | Mobile network sniffing & tracking |  

---

## **5. Defending Against SDR-Based Threats**  

🔒 **Encryption & Authentication**  
✔ Use **end-to-end encryption (AES-256, WPA3, TLS 1.3)**.  
✔ Deploy **frequency-hopping spread spectrum (FHSS) & DSSS**.  

🔒 **RF Anomaly Detection**  
✔ Monitor for **unauthorized RF signals**.  
✔ Use **SDRs for real-time spectrum monitoring**.  

🔒 **Physical Security & RF Shielding**  
✔ Implement **Faraday cages** for sensitive environments.  
✔ Restrict **unauthorized SDR devices** in secure locations.  

---

## **6. Conclusion**  
Software-Defined Radio (SDR) is a **powerful tool** for **signal interception, cybersecurity research, and electronic warfare**. However, it also presents **major security risks**, as attackers can **sniff, jam, spoof, and manipulate wireless communications** across a wide range of frequencies.  

✅ **Key Takeaways:**  
- SDR enables **wideband RF interception & active attacks**.  
- **WiFi, Bluetooth, RFID, GPS, and cellular networks** are vulnerable.  
- **Military, intelligence, and cybersecurity professionals** use SDR for **signals intelligence (SIGINT) and penetration testing**.  
- **Encryption, authentication, and RF monitoring** are critical defenses.  

📡 **Next Steps**: Would you like a detailed guide on **setting up an SDR for penetration testing, hands-on tutorials, or real-world case studies?** 🚀

