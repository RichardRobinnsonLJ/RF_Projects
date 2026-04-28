# 🔊 RF Power Amplifier Design @ 2.4 GHz

## 🚀 Overview

This project presents the design and simulation of a **CMOS RF Power Amplifier (PA)** operating at **2.4 GHz** using **90nm technology** in Cadence Virtuoso.

The goal of the design is to:

* Increase signal power for transmission
* Maintain linearity
* Ensure proper impedance matching (50 ohm)

---

## 🧠 Key Concepts

* Power Gain
* Linearity (1 dB Compression Point)
* Harmonic Distortion
* Efficiency
* Load Matching

---

## ⚙️ Specifications

| Parameter              | Value     |
| ---------------------- | --------- |
| Technology             | 90nm CMOS |
| Supply Voltage (VDD)   | 1.2 V     |
| Operating Frequency    | 2.4 GHz   |
| Input/Output Impedance | 50 ohm    |
| Drain Current (Id)     | 17 mA     |

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

* Gain response verified at 2.4 GHz
* 1 dB compression point observed
* Harmonic distortion analyzed

---

## 🛠 Tools Used

* Cadence Virtuoso
* GPDK 90nm CMOS

---

## 📌 Design Insights

* Load matching plays a key role in maximizing power transfer
* Linearity is limited by device nonlinearity at high input power
* Trade-off exists between gain and efficiency

---

## 🚧 Future Improvements

* Efficiency optimization (Class AB / Class E design)
* Load-pull analysis
* Layout and parasitic extraction
* Thermal considerations

---

## ❗ Challenges Faced

* Achieving both high gain and linearity simultaneously
* Maintaining stability at high frequency
* Proper tuning of matching network

---

## ✅ Conclusion

A 2.4 GHz CMOS Power Amplifier was successfully designed and analyzed.
The circuit demonstrates effective signal amplification with acceptable linearity and matching performance.

---
