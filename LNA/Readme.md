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

### 1. Transconductance (gm)

[
g_m = \mu_n C_{ox} \frac{W}{L} (V_{GS} - V_{th})
]

[
C_{ox} = \frac{\varepsilon_0 \varepsilon_{ox}}{t_{ox}}
]

Substituting values:

* ( \mu_n = 300 \times 10^{-4} )
* ( \varepsilon_0 = 8.854 \times 10^{-12} )
* ( \varepsilon_{ox} = 3.6 )
* ( t_{ox} = 2.2 \text{ nm} )

[
g_m = 10.86 \times 10^{-3} , S
]

---

### 2. Drain Current (Id)

[
g_m = \frac{2 I_D}{V_{GS} - V_{th}}
]

[
I_D = \frac{g_m (V_{GS} - V_{th})}{2}
]

[
I_D = 5.43 \times 10^{-4} , A
]

---

### 3. Load Resistance (RD)

[
R_D = \frac{V_{DD}}{2 I_D}
]

[
R_D = 1.1 , k\Omega
]

---

### 4. Inductor Conversion

[
X_L = 2\pi f L = R_D
]

[
L = \frac{R_D}{2\pi f}
]

[
L = 66.9 , nH
]

---

### 5. Input Matching Network

Given:

* ( R_s = 50\Omega )
* ( R_p = 10k\Omega )

[
X_s = \sqrt{R_s (R_p - R_s)} = 705.33
]

[
L = \frac{X_s}{2\pi f} = 46.77 , nH
]

[
X_p = \frac{R_s R_p}{X_s} = 708.88
]

[
C = \frac{1}{2\pi f X_p} = 93.5 , fF
]

---

### 6. Output Matching Network

[
|S_{22}| = 0.95
]

[
Z_L = 1.958 , k\Omega
]

[
X_s = \sqrt{50 (Z_L - 50)} = 308.91
]

[
L = \frac{X_s}{2\pi f} = 20.48 , nH
]

[
C = 0.21 , pF
]

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

## 📸 Required Plots (Upload These)

Add the following images inside this folder:

* `schematic.png` → Circuit schematic
* `s_parameters.png` → S11, S21, S22, S12 plot
* `noise_figure.png` → NF vs frequency
* `bandwidth.png` → Gain vs frequency
* `compression.png` → 1 dB compression point
* `harmonics.png` → Harmonic distortion

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
