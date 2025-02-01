---
title: "Basics of Wave Physics"
teaching: 0
exercises: 0
questions:
- "Key question (FIXME)"
objectives:
- "First learning objective. (FIXME)"
keypoints:
- "First key point. Brief Answer to questions. (FIXME)"
---


<!--- how to render latex in markdown? https://stackoverflow.com/questions/10987992/using-mathjax-with-jekyll --->

### **Basics of Wave Physics: Frequency, Wavelength, and Energy**  

Electromagnetic waves are fundamental to wireless communication and cybersecurity. Understanding their properties—**frequency, wavelength, and energy**—is crucial for designing secure systems and mitigating threats.  

## **1. Frequency ($f$)**
- **Definition**: The number of wave cycles that pass a given point per second.  
- **Unit**: Hertz (Hz), where **1 Hz = 1 cycle per second**.  
- **Formula**:  
  
  $f = \frac{c}{\lambda}$  
  where:  
  - $f$ = frequency (Hz)  
  - $c$ = speed of light in a vacuum (approximately $3.0 \times 10^8 ~m/s$)  
  - $\lambda$ = wavelength (meters)  

### **Relevance to Cybersecurity**
- Different frequency bands are allocated for wireless communication (e.g., WiFi at **2.4 GHz and 5 GHz**, Bluetooth at **2.4 GHz**).  
- **Higher frequencies** (e.g., 5G at **28 GHz, 39 GHz**) allow for **faster data transfer** but have shorter range.  
- **Lower frequencies** (e.g., **AM/FM radio, military signals**) **travel further** and penetrate obstacles more easily.

## **2. Wavelength ($\lambda$)**
- **Definition**: The physical distance between successive wave peaks.  
- **Unit**: Meters (m).  
- **Formula**:  
  
  $\lambda = \frac{c}{f} $
  
- **Relationship**: Inversely proportional to frequency—**higher frequency = shorter wavelength** and vice versa.  

### **Relevance to Cybersecurity**
- Shorter wavelengths (high-frequency signals like **WiFi, 5G, millimeter waves**) are **more easily absorbed** by obstacles like walls, affecting security and coverage.  
- Longer wavelengths (low-frequency signals like **radio waves**) can **travel further** and be intercepted over long distances.  

## **3. Energy ($E$)**
- **Definition**: The energy carried by a wave is related to its frequency.  
- **Unit**: Joules ($J$).  
- **Formula**:

  $E=hf$  
  where:  
  - $E$ = energy (Joules)  
  - $h$ = Planck’s constant ($6.626 \times 10^{-34}~Js$ )  
  - $f$ = frequency (Hz)  

### **Relevance to Cybersecurity**
- **Higher-energy waves** (e.g., **X-rays, gamma rays**) can be used in radiation-based surveillance or hacking techniques.  
- **Microwave and infrared waves** can be used in covert communication and surveillance methods.  
- **Low-energy waves** (e.g., **radio waves**) are used in RFID, NFC, and WiFi, making them susceptible to **eavesdropping and jamming**.

## **Key Takeaways for Cybersecurity**

| Property    | Impact on Communication & Security |
|-------------|------------------------------------|
| **High Frequency (Short Wavelength)** | Faster data rates, but signals are easier to block (e.g., 5G, WiFi) |
| **Low Frequency (Long Wavelength)** | Longer range, but more susceptible to interception (e.g., radio, RFID) |
| **Higher Energy** | More difficult to block but requires more power (e.g., satellite communications) |

Understanding these wave properties helps in **designing secure networks**, mitigating **wireless attacks**, and implementing **defensive measures** against threats like **RF hacking, eavesdropping, and jamming**.  

{% include links.md %}
