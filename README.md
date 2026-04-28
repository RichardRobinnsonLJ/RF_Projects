# 📡 RF IC Design Portfolio (2.4 GHz)

This repository contains a collection of **RF circuit designs** implemented using **Cadence Virtuoso (GPDK 90nm CMOS technology)** as part of my Master's in VLSI.

The focus is on designing and analyzing key RF front-end building blocks operating around **2.4 GHz**, widely used in wireless communication systems.

---

## 🚀 Projects Included

### 1. Low Noise Amplifier (LNA)

* Cascode topology
* Input/output impedance matching (50Ω)
* Optimized for low noise figure and gain

### 2. Power Amplifier

* Designed for RF signal boosting
* Focus on gain, linearity, and efficiency
* Harmonic and compression analysis

### 3. Gilbert Cell Mixer

* Active mixer for frequency conversion
* Differential architecture
* Conversion gain and transient analysis

### 4. Voltage Controlled Oscillator (VCO)

* LC-based oscillator
* Frequency tuning using control voltage
* Stability and phase noise considerations

---

## 🧠 Key Concepts Covered

* S-Parameters (S11, S21, S22)
* Noise Figure Optimization
* Impedance Matching
* Frequency Conversion
* LC Resonance
* RF Non-linearity (P1dB, Harmonics)

---

## 🛠 Tools & Technology

* Cadence Virtuoso
* GPDK 90nm CMOS Technology

---

## 📊 Results Snapshot

| Circuit | Key Result                 |
| ------- | -------------------------- |
| LNA     | NF ≈ 2.85 dB, BW ≈ 316 MHz |
| Mixer   | Conversion Gain ≈ 6.52 dB  |
| VCO     | Tunable around 2.4 GHz     |
| PA      | Gain & linearity verified  |

---

## 📂 Repository Structure

```
RF-IC-Design/
│── Low-Noise-Amplifier/
│── Power-Amplifier/
│── Gilbert-Cell-Mixer/
│── Voltage-Controlled-Oscillator/
```

---

## 📸 Note

Simulation plots such as:

* S-parameters
* Noise figure
* Gain response
* Transient waveforms
  are included within each project folder.

---

## 🎯 Learning Outcomes

* Practical understanding of RF front-end design
* Hands-on experience with Cadence Virtuoso
* Trade-offs between gain, noise, and linearity
* Matching network design at GHz frequencies

---

## 🚧 Future Improvements

* Layout design and parasitic extraction
* Post-layout simulations
* Integration into complete RF receiver chain
* Extension to mmWave designs

---

## 👨‍💻 Author

Master’s VLSI Student focused on **Analog & RF IC Design**, aiming to build efficient and high-performance communication circuits.

---
