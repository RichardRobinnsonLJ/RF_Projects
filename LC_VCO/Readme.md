# 🎯 Voltage Controlled Oscillator (VCO) Design @ 2.4 GHz

## 🚀 Overview

This project presents the design and simulation of a **CMOS LC Voltage Controlled Oscillator (VCO)** operating at **2.4 GHz** using **90nm technology** in Cadence Virtuoso.

The VCO generates an oscillating signal whose frequency is controlled by an input voltage, making it a key component in **PLL and frequency synthesizers**.

---

## 📚 Theory (Short & Clear)

A **Voltage Controlled Oscillator (VCO)** generates a periodic signal where the **output frequency depends on the control voltage (Vctrl)**.

### 🔹 LC Oscillator Principle

The oscillation frequency is determined by an LC tank circuit:

```id="eq1"
f = 1 / (2π√(LC))
```

### 🔹 Working

* Energy oscillates between inductor (L) and capacitor (C)
* Active devices compensate losses to sustain oscillation
* Changing capacitance (via control voltage) changes frequency

### 🔹 Applications

* Phase Locked Loops (PLL)
* Frequency Synthesizers
* RF Transceivers

---

## 🧠 Key Concepts

* LC Resonance
* Frequency Tuning
* Phase Noise
* Stability
* Feedback in Oscillators

---

## ⚙️ Specifications

| Parameter            | Value     |
| -------------------- | --------- |
| Technology           | 90nm CMOS |
| Supply Voltage (VDD) | 1.8 V     |
| Target Frequency     | 2.4 GHz   |
| Feedback Ratio (β)   | 0.3       |

---

## 📐 Design Calculations

### 🔹 Given Parameters

* f = 2.4 GHz
* β = 0.3
* C1 = 1 nF

---

### 🔹 Step 1: Total Capacitance (CT)

β = CT / C1

CT = β × C1
CT = 0.3 × 1 nF
CT = 0.3 nF

---

### 🔹 Step 2: Calculate C2

CT = (C1 × C2) / (C1 + C2)

Rearranging:

C2 = (CT × C1) / (C1 - CT)

C2 = (0.3 × 1) / (1 - 0.3)
C2 ≈ 0.4285 nF

---

### 🔹 Step 3: Inductor Calculation

Using resonance condition:

(2πf)² = (C1 + C2) / (L × C1 × C2)

Rearranging:

L = (C1 + C2) / ((2πf)² × C1 × C2)

L ≈ 14.6 pH

---

### 🔹 Step 4: Tuning Capacitance

At resonance:

C = 1 / (L × (2πf)²)

C ≈ 0.301 nF

---

## 🧪 Simulation Results

| Control Voltage (mV) | Frequency (GHz) |
| -------------------- | --------------- |
| 100                  | 2.31            |
| 150                  | 2.39            |
| 200                  | 2.40            |
| 250                  | 2.41            |

---

## 🛠 Tools Used

* Cadence Virtuoso
* GPDK 90nm CMOS

---

## 📌 Design Insights

* Frequency tuning achieved by varying capacitance
* LC tank determines oscillation frequency
* Stability depends on proper feedback design
* Trade-off exists between tuning range and phase noise

---

## ❗ Challenges Faced

* Achieving stable oscillation at GHz frequency
* Maintaining consistent amplitude
* Sensitivity to component variations

---

## 🚧 Future Improvements

* Phase noise optimization
* Integration with PLL
* Layout design and parasitic extraction
* Wider tuning range

---

## 🔍 Practical Insight

VCOs are core components in PLL systems used in communication circuits for frequency generation and synchronization.

---

## ✅ Conclusion

A CMOS LC VCO was successfully designed at 2.4 GHz.
The circuit demonstrates stable oscillation with controllable frequency, making it suitable for RF and communication applications.

---
