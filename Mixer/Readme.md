# 🔀 Gilbert Cell Mixer Design @ 2.4 GHz

## 🚀 Overview

This project presents the design and simulation of a **CMOS Gilbert Cell Mixer** operating at **2.4 GHz** using **90nm technology** in Cadence Virtuoso.

The mixer performs **frequency conversion**, translating an RF signal to an intermediate frequency (IF) using a Local Oscillator (LO).

---

## 📚 Theory (Short & Clear)

A **mixer** is a nonlinear circuit used to shift the frequency of a signal. It combines two input signals:

* RF (Radio Frequency)
* LO (Local Oscillator)

The output contains:

* Sum frequency → (f_RF + f_LO)
* Difference frequency → (f_RF - f_LO)

👉 Core relation:

```
f_out = f_RF ± f_LO
```

### 🔹 Gilbert Cell Mixer

The **Gilbert cell** is an active mixer that uses:

* A transconductance stage (RF input)
* A switching stage (LO input)

Key advantages:

* Good conversion gain
* Differential operation (noise immunity)
* Reduced feedthrough

---

## 🧠 Key Concepts

* Frequency Conversion
* Conversion Gain
* LO Switching
* Non-linearity
* Differential Design

---

## ⚙️ Specifications

| Parameter            | Value     |
| -------------------- | --------- |
| Technology           | 90nm CMOS |
| Supply Voltage (VDD) | 1.2 V     |
| RF Frequency         | 2.4 GHz   |
| LO Frequency         | 2.25 GHz  |
| Output               | IF Signal |

---

## 📐 Design Calculations

### 🔹 Conversion Gain

Conversion gain is defined as:

Gain = V_IF / V_RF

Given:

* V_RF = 500 mV
* V_IF = 550.56 mV + 510.174 mV

V_IF ≈ 1060.734 mV

Gain = 1060.734 / 500
Gain ≈ 2.12

---

### 🔹 Gain in dB

Gain (dB) = 20 log(Gain)

Gain ≈ 6.52 dB

---

## 🧪 Simulation Results

| Parameter         | Value    |
| ----------------- | -------- |
| Conversion Gain   | 6.52 dB  |
| Noise Figure      | 13.06 dB |
| Power Consumption | ~4.8 W   |

---

## 🛠 Tools Used

* Cadence Virtuoso
* GPDK 90nm CMOS

---

## 📌 Design Insights

* Mixer works due to transistor non-linearity
* LO signal acts as a switching signal
* Differential structure improves noise immunity
* Conversion gain depends on biasing and switching efficiency

---

## ❗ Challenges Faced

* Achieving proper LO switching at GHz frequency
* Controlling noise figure
* Maintaining symmetry in differential design

---

## 🚧 Future Improvements

* Improve noise figure
* Optimize power consumption
* Add filtering for better IF extraction
* Layout implementation and parasitic analysis

---

## ✅ Conclusion

A Gilbert Cell Mixer was successfully designed for 2.4 GHz operation.
The circuit achieves frequency conversion with moderate conversion gain and demonstrates key RF mixing principles.

---
