Here is a complete `README.md` file for your **CMOS Inverter Layout Design in 200nm Technology** project, based on the data you've provided:

---

```markdown
# CMOS Inverter Layout Design (200nm Technology)

## 📌 Project Overview

This repository contains the **custom layout design, simulation setup, and verification details** for a **CMOS Inverter** implemented using **200nm CMOS technology**. A CMOS inverter is a fundamental building block in digital VLSI circuits, composed of a complementary pair of PMOS and NMOS transistors.

The goal of this project is to create a full-custom layout of the inverter, simulate it using industry-grade BSIM3 Level 7 models, and verify its switching behavior under pulse stimulus conditions.

---

## 🧱 Design Specifications

- **Technology Node:** 200nm (0.2µm)
- **Transistor Models:** BSIM3 Level 7 for both NMOS and PMOS
- **Supply Voltage (VDD):** 2V
- **Channel Length (L):** 0.4µm
- **Channel Width (W):** 0.6µm

### ⚙️ Transistor Parameters

#### NMOS:
```

Mnmos\@0 Y A gnd gnd NMOS L=0.4U W=0.6U AS=5.5P AD=1.3P PS=15.4U PD=5U

```

#### PMOS:
```

Mpmos\@0 Y A vdd vdd PMOS L=0.4U W=0.6U AS=5.5P AD=1.3P PS=15.4U PD=5U

````

---

## 🧪 Simulation Setup

### 🛠 Pulse Source:
```spice
vpulse1 A GND PULSE(0 2 0 20n 20n 3m 8m)
````

* Rise Time: 20ns
* Fall Time: 20ns
* Pulse Width: 3ms
* Period: 8ms

### 🔁 Transient Analysis:

```spice
.tran 20ms
```

---

## 📂 Included Files

* `layout_image.png` – Screenshot of the final layout
* `simulation_image.png` – Output waveform showing correct inverter behavior
* `cmos_inverter.sp` – SPICE netlist of the inverter
* `model_nmos.txt` – NMOS transistor model (BSIM3 Level 7)
* `model_pmos.txt` – PMOS transistor model (BSIM3 Level 7)

---

## ✅ Verification

The layout was verified using:

* **Design Rule Check (DRC)** – Passed
* **Layout Versus Schematic (LVS)** – Matched
* **Transient Simulation** – Validated logic inversion

The simulated waveform shows the expected logic behavior of a CMOS inverter:

* When input is HIGH (2V), output is LOW (0V)
* When input is LOW (0V), output is HIGH (2V)

---

## 🧠 Technical Insight

A CMOS inverter uses:

* **PMOS** transistor connected to VDD
* **NMOS** transistor connected to GND
* Common gate as input, common drain as output

The output node swings between VDD and GND depending on the input, ensuring low static power dissipation and high noise margins.

---

## 📸 Project Snapshots

### 📐 Layout Design

---![411303258-b5b1e1d1-2d38-428f-a7ed-9f01e2c6924e](https://github.com/user-attachments/assets/1eb9b84f-7674-4d55-8ad6-f990d9a67d21)


### 📊 Simulation Result

![411303185-70ef45c9-77b2-4e4a-aaff-9c9700b8c513](https://github.com/user-attachments/assets/d339f324-bdb4-4fad-ac2f-1d063db65dcb)


---

## 👨‍💻 Author

*Sandeep Kumar* – VLSI Enthusiast | ECE Student



## 📄 License

This project is licensed under the MIT License – feel free to use or modify for academic and research purposes.

---

```

Let me know if you'd like to customize it with your name, university, or compress it into a `.md` file format.
```
