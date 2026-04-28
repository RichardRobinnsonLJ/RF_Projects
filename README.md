# 📡 RF & Mixed-Signal IC Design Portfolio (2.4 GHz)

This repository contains a collection of **RF and Mixed-Signal circuit designs** implemented using **Cadence Virtuoso (GPDK 90nm CMOS technology)** as part of my Master's in VLSI.

The focus is on designing and analyzing key RF front-end building blocks along with **data conversion and frequency synthesis systems**, operating around **2.4 GHz and beyond**.

---

## 🚀 Projects Included

### 1. Low Noise Amplifier (LNA)

* Cascode topology
* Input/output impedance matching (50Ω)
* Optimized for low noise figure and gain

---

### 2. Power Amplifier

* Designed for RF signal boosting
* Focus on gain, linearity, and efficiency
* Harmonic and compression analysis

---

### 3. Gilbert Cell Mixer

* Active mixer for frequency conversion
* Differential architecture
* Conversion gain and transient analysis

---

### 4. Voltage Controlled Oscillator (VCO)

* LC-based oscillator
* Frequency tuning using control voltage
* Stability and phase noise considerations

---

### 5. Flash ADC (Mixed-Signal)

* 1 GHz high-speed ADC design
* Includes Sample-and-Hold, Comparator, and Encoder
* Thermometer-to-binary conversion
* Performance analysis using SNDR, ENOB, DNL

---

### 6. Phase Locked Loop (PLL)

* Designed for ~2.7 GHz frequency synthesis
* Includes:

  * Phase Detector (PD)
  * Loop Filter (LF)
  * Ring Oscillator-based VCO
  * 24-bit Frequency Divider
* Closed-loop frequency stabilization
* Demonstrates frequency locking and control behavior

---

### 7. High-Frequency RF Signal Generator (Thesis Work)

* Cross-Coupled Oscillator + Frequency Multiplier based system
* Generates high-frequency signals using harmonic extraction
* Includes:

  * Cross-Coupled Oscillator (6 GHz fundamental)
  * Harmonic Frequency Multiplier (×2 → 12 GHz)
  * LC Bandpass Filter for spectral purity
  * RF Amplifier stage

📌 This work demonstrates efficient high-frequency signal generation using CMOS techniques 

---

## 🧠 Key Concepts Covered

* S-Parameters (S11, S21, S22)
* Noise Figure Optimization
* Impedance Matching
* Frequency Conversion
* LC Resonance
* RF Non-linearity (P1dB, Harmonics)
* Analog-to-Digital Conversion (ADC)
* Phase Locked Loops (PLL)
* Frequency Multiplication Techniques
* Mixed-Signal System Integration

---

## 🛠 Tools & Technology

* Cadence Virtuoso
* GPDK 90nm CMOS Technology

---

## 📊 Results Snapshot

| Circuit           | Key Result                          |
| ----------------- | ----------------------------------- |
| LNA               | NF ≈ 2.85 dB, BW ≈ 316 MHz          |
| Mixer             | Conversion Gain ≈ 6.52 dB           |
| VCO               | Tunable around 2.4 GHz              |
| PA                | Gain & linearity verified           |
| ADC               | SNDR ≈ 10.84 dB, ENOB ≈ 1.5 bits    |
| PLL               | Frequency locking at ~2.7 GHz       |
| Multiplier System | 6 GHz → 12 GHz frequency generation |

---

## 📂 Repository Structure

```id="rf_full_struct"
RF-IC-Design/
│── Low-Noise-Amplifier/
│── Power-Amplifier/
│── Gilbert-Cell-Mixer/
│── Voltage-Controlled-Oscillator/
│── Flash-ADC/
│── PLL/
│── Frequency-Multiplier-System/
```

---

## 📸 Note

Simulation plots such as:

* S-parameters
* Noise figure
* Gain response
* Transient waveforms
* FFT, DNL (ADC)
* Phase noise (VCO, PLL)
* Spectrum analysis (Multiplier)

are included within each project folder.

---

## 🎯 Learning Outcomes

* Practical understanding of RF front-end design
* Hands-on experience with Cadence Virtuoso
* Trade-offs between gain, noise, and linearity
* Frequency synthesis using PLL
* High-frequency signal generation using multipliers
* Integration of analog and digital blocks in mixed-signal systems

---

## 🚧 Future Improvements

* Layout design and parasitic extraction
* Post-layout simulations
* Full RF receiver chain integration
* Higher resolution ADC design
* Low phase-noise PLL optimization
* Extension to mmWave / THz systems

---

## 👨‍💻 Author

Master’s VLSI Student focused on **Analog, RF & Mixed-Signal IC Design**, aiming to build efficient and high-performance communication systems.

---
