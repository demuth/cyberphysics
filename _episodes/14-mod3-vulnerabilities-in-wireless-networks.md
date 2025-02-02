---
title: "Vulnerabilities in Wireless Networks"
teaching: 0
exercises: 0
questions:
- "Key question (FIXME)"
objectives:
- "First learning objective. (FIXME)"
keypoints:
- "First key point. Brief Answer to questions. (FIXME)"
---

# **Vulnerabilities of Wireless Networks: Man-in-the-Middle Attacks and Sniffing**  

Wireless networks are **inherently more vulnerable than wired networks** because they rely on radio signals, which can be **intercepted, manipulated, or disrupted** by attackers. Some of the most common wireless security threats include **Man-in-the-Middle (MITM) attacks and Packet Sniffing**, both of which can compromise sensitive data and network integrity.

---

## **1. Man-in-the-Middle (MITM) Attacks**  
### **1.1 What is a MITM Attack?**  
A **Man-in-the-Middle (MITM) attack** occurs when an attacker **intercepts and possibly alters** communication between two parties without their knowledge. The attacker positions themselves between the sender and receiver to **eavesdrop, steal data, or inject malicious content**.

**Example:**  
- **Attacker impersonates a trusted WiFi access point** in a coffee shop, tricking users into connecting.  
- The attacker **monitors all traffic** (logins, emails, messages, credit card details).  
- If connections are unencrypted, the attacker can **steal or alter the data in transit**.

---

### **1.2 Types of MITM Attacks in Wireless Networks**  

| **Attack Type** | **How It Works** | **Impact** |  
|---------------|---------------|---------|  
| **Rogue Access Point (Evil Twin Attack)** | Attacker sets up a fake WiFi hotspot with the same SSID as a legitimate network | Users unknowingly connect and expose sensitive data |  
| **WiFi Deauthentication Attack** | Attacker forces users to disconnect from a real WiFi and reconnect to a rogue AP | Attackers intercept login credentials and communications |  
| **Session Hijacking** | Attacker steals active session cookies to impersonate a user | Account takeover (email, banking, social media) |  
| **DNS Spoofing** | Redirects users to a fake website that mimics a legitimate one | Phishing and malware injection |  
| **SSL Stripping** | Downgrades HTTPS connections to HTTP to remove encryption | Exposes passwords, credit card info, and personal data |  

🔴 **High-Risk Wireless Networks**:  
- **Public WiFi (airports, hotels, coffee shops)**  
- **Open or weakly encrypted WiFi (WEP, WPA1)**  
- **IoT devices with weak authentication**  

---

### **1.3 MITM Attack Prevention Strategies**  

✅ **Use Encrypted Connections**  
- Always use **HTTPS** (TLS 1.3) websites.  
- Enable **VPNs (Virtual Private Networks)** on public WiFi.  
- Use **end-to-end encrypted messaging apps** (Signal, WhatsApp).  

✅ **Secure WiFi Configurations**  
- Use **WPA3** encryption for wireless networks.  
- Disable **SSID broadcasting** and use **MAC address filtering**.  
- Enable **network segmentation** to separate IoT from critical systems.  

✅ **Use Strong Authentication**  
- Implement **Multi-Factor Authentication (MFA)** to prevent session hijacking.  
- Use **certificates and public key authentication** for enterprise networks.  

✅ **Monitor Network Traffic**  
- Deploy **Intrusion Detection Systems (IDS) & Intrusion Prevention Systems (IPS)**.  
- Use **AI-driven anomaly detection** for unusual network behavior.  

---

## **2. Packet Sniffing Attacks**  

### **2.1 What is Packet Sniffing?**  
Packet sniffing is the process of **capturing and analyzing wireless network traffic** to extract sensitive information such as **passwords, emails, or financial transactions**.  

**Example:**  
- An attacker with a **WiFi adapter in monitor mode** can capture packets in an open WiFi network.  
- If the data is **unencrypted**, they can extract sensitive information such as **login credentials, API keys, or credit card numbers**.

---

### **2.2 Types of Packet Sniffing Attacks**  

| **Attack Type** | **How It Works** | **Impact** |  
|---------------|---------------|---------|  
| **Passive Sniffing** | Attacker quietly monitors and captures data packets without interfering | Silent data theft, credential harvesting |  
| **Active Sniffing** | Attacker injects packets into the network to manipulate or redirect traffic | MITM, session hijacking |  
| **WiFi Eavesdropping** | Attackers use sniffing tools like Wireshark to capture unencrypted WiFi traffic | Leaks passwords, emails, and financial transactions |  
| **ARP Spoofing (Address Resolution Protocol Attack)** | Attacker associates their MAC address with a target’s IP to intercept traffic | Network takeover, MITM attacks |  
| **DNS Snooping** | Monitoring DNS requests to track user activity and redirect traffic | Phishing, malware injection |  

🔴 **Common Tools Used for Packet Sniffing**:  
- **Wireshark** (network protocol analyzer)  
- **tcpdump** (command-line packet capture tool)  
- **Bettercap** (MITM framework)  
- **Aircrack-ng** (WiFi sniffing and cracking suite)  

---

### **2.3 Preventing Packet Sniffing Attacks**  

✅ **Encrypt Wireless Traffic**  
- Use **WPA3 or WPA2-AES** encryption for WiFi networks.  
- Enable **end-to-end encryption (TLS 1.3, VPNs, SSH)**.  
- Use **encrypted DNS (DNS-over-HTTPS, DNS-over-TLS)** to prevent snooping.  

✅ **Secure WiFi Connections**  
- **Avoid connecting to public/open WiFi networks**.  
- Use **personal mobile hotspots instead of public WiFi**.  
- If using public WiFi, **enable a VPN** to encrypt traffic.  

✅ **Monitor Network Traffic for Anomalies**  
- Use **network monitoring tools (Zeek, Snort, Suricata)** to detect suspicious activity.  
- Deploy **firewalls and IDS/IPS** to prevent unauthorized packet capture.  

✅ **Use Secure Authentication Methods**  
- Use **certificate-based authentication** instead of passwords.  
- Implement **Zero-Trust security models** for access control.  

---

## **3. Comparing MITM Attacks & Sniffing**  

| **Attack Type** | **Method** | **Target** | **Impact** |  
|---------------|-----------|--------|--------|  
| **MITM Attack** | Intercepts and manipulates communication | Encrypted or unencrypted wireless networks | Data theft, session hijacking, phishing |  
| **Packet Sniffing** | Captures unencrypted data packets | Open WiFi, weak encryption (WEP, WPA1) | Credential theft, monitoring, data exfiltration |  

🔴 **Key Difference**:  
- **MITM attacks modify data in transit**, while **packet sniffing passively captures data**.  
- **MITM attacks often involve deception (spoofing, phishing, rogue APs)**, while sniffing relies on **listening to existing transmissions**.  

✅ **Best Defense Strategy**: **Use strong encryption (WPA3, VPNs, TLS 1.3) and secure authentication methods to protect against both MITM and sniffing attacks.**  

---

## **4. Conclusion**  
Wireless networks are **highly vulnerable to MITM attacks and packet sniffing**, making security measures **critical**. Attackers exploit **open WiFi, weak encryption, and insecure authentication** to **steal credentials, manipulate traffic, and compromise data integrity**.  

### **🔐 Best Practices for Wireless Security**  
✔ **Use WPA3 encryption** for WiFi security.  
✔ **Avoid public WiFi** or use **VPNs** when necessary.  
✔ **Enable Multi-Factor Authentication (MFA)** to protect against account takeovers.  
✔ **Use HTTPS & TLS 1.3** to encrypt sensitive data.  
✔ **Monitor networks for anomalies** with IDS/IPS.  

{% include links.md %}
