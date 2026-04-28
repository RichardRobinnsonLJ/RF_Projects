# 📡 Low Noise Amplifier (LNA) Design @ 2.4 GHz

## 🚀 Overview

This project presents the design and simulation of a **Cascode CMOS Low Noise Amplifier (LNA)** operating at **2.4 GHz** using **90nm technology** in Cadence Virtuoso.

The objective is to achieve:

* Low Noise Figure (NF)
* High Gain
* Proper impedance matching (50Ω)
* Adequate bandwidth

---

## 🧠 Key Concepts

* Noise Figure (NF)
* S-Parameters (S11, S21, S22, S12)
* Impedance Matching
* Cascode Topology
* Gain vs Noise trade-off

---

## ⚙️ Specifications

| Parameter               | Value     |
| ----------------------- | --------- |
| Technology              | 90nm CMOS |
| Supply Voltage (VDD)    | 1.2 V     |
| Operating Frequency     | 2.4 GHz   |
| Input/Output Impedance  | 50 Ω      |
| Threshold Voltage (Vth) | 0.2 V     |
| Gate Voltage (VGS)      | 0.3 V     |

---

## 📐 Design Calculations

### 🔹 Given Parameters

* VDD = 1.2 V
* f = 2.4 GHz
* VGS = 0.3 V
* Vth = 0.2 V
* W = 25 um, L = 100 nm
* tox = 2.2 nm
* ε0 = 8.854e-12
* εox = 3.6
* μn = 300e-4

---

### 🔹 Step 1: Oxide Capacitance

Cox = (ε0 × εox) / tox
Cox = (8.854e-12 × 3.6) / (2.2e-9)
Cox ≈ 1.45e-2 F/m²

---

### 🔹 Step 2: Transconductance (gm)

gm = μn × Cox × (W/L) × (VGS - Vth)

gm ≈ 10.86e-3 S

---

### 🔹 Step 3: Drain Current (Id)

gm = 2Id / (VGS - Vth)

Id = (gm × (VGS - Vth)) / 2
Id ≈ 5.43e-4 A

---

### 🔹 Step 4: Load Resistance (RD)

RD = VDD / (2 × Id)
RD ≈ 1.1 kΩ

---

### 🔹 Step 5: Inductor Conversion

XL = RD

L = RD / (2πf)
L ≈ 66.9 nH

---

### 🔹 Step 6: Input Matching

Rs = 50 ohm
Rp = 10k ohm

Xs = √[Rs(Rp - Rs)] ≈ 705.33

L = Xs / (2πf) ≈ 46.77 nH

Xp = (Rs × Rp) / Xs ≈ 708.88

C = 1 / (2πfXp) ≈ 93.5 fF

---

### 🔹 Step 7: Output Matching

ZL ≈ 1.958k ohm

Xs ≈ 308.91

L ≈ 20.48 nH

C ≈ 0.21 pF


---

## 🧪 Simulation Results

| Parameter    | Target      | Achieved  |
| ------------ | ----------- | --------- |
| S11          | ≤ -10 dB    | -11.64 dB |
| S21          | ≥ 15 dB     | 12.56 dB  |
| S22          | ≤ -10 dB    | -17.74 dB |
| S12          | Negative    | -47.60 dB |
| Noise Figure | < 3 dB      | 2.85 dB   |
| Bandwidth    | 200–400 MHz | 316 MHz   |

---

## 🛠 Tools Used

* Cadence Virtuoso
* GPDK 90nm CMOS

---

## 📌 Design Insights

* Cascode topology improves gain and isolation
* Matching network is critical for minimizing reflections
* Trade-off exists between gain and noise figure
* Slight gain drop observed due to matching constraints

---

## 🚧 Future Improvements

* Improve gain beyond 15 dB
* Layout design + parasitic extraction
* Stability factor (K-factor) analysis
* Power optimization

---

## ✅ Conclusion

A 2.4 GHz CMOS LNA was successfully designed and simulated.
The design achieves **low noise figure and good impedance matching**, making it suitable for RF front-end applications.

---
