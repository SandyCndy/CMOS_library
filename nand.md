# 🧠 2-Input NAND Gate CMOS Design (200nm Technology)

This repository presents the **schematic**, **layout**, and **SPICE simulation** of a **2-input NAND gate** using **200nm CMOS technology**. The project includes a transistor-level implementation with verified simulation results and layout design, based on accurate BSIM3v3 model cards.

---

## 🔍 Overview

- **Gate Type**: 2-Input NAND
- **Technology Node**: 200nm
- **Design Approach**: CMOS-based (2 PMOS in parallel, 2 NMOS in series)
- **Simulation Tool**: LTspice / Ngspice
- **Layout Tool**: Microwind / Magic VLSI
- **Modeling Standard**: BSIM3v3 (LEVEL 7)

---

## ⚙️ Transistor Sizing

| Transistor | Type  | Width (W) | Length (L) | Notes            |
|------------|-------|-----------|------------|------------------|
| M<sub>nmos@0</sub> | NMOS  | 0.6μm     | 0.4μm      | Net A to Net@7  |
| M<sub>nmos@1</sub> | NMOS  | 0.6μm     | 0.4μm      | Net@7 to GND    |
| M<sub>pmos@0</sub> | PMOS  | 0.6μm     | 0.4μm      | VDD to Net Y    |
| M<sub>pmos@2</sub> | PMOS  | 0.6μm     | 0.4μm      | VDD to Net Y    |


---

## 🧪 SPICE Simulation

### Input Stimuli

```spice
vpulse1 A GND PULSE (0 2 0 20n 20n 3m 8m)
vpulse2 B GND PULSE (0 2 0 10n 30n 4m 10m)
.tran 20ms
```

### Expected NAND Behavior

| A | B | Y (Output) |
| - | - | ---------- |
| 0 | 0 | 1          |
| 0 | 1 | 1          |
| 1 | 0 | 1          |
| 1 | 1 | 0          |

### 📈 Waveform Snapshot

![408742242-2af1f54b-2274-4610-9d5b-c935f8c717e3](https://github.com/user-attachments/assets/26646960-966a-4aa6-a7ec-6aa804ab0ed6)

---

## 🧱 CMOS Layout

* Layout includes metal1/poly/diffusion layers
* DRC and LVS-verified (Design Rule Check and Layout vs Schematic)
* Tools used: Microwind / Magic

![408741994-d17bbe55-522f-4009-85c9-bd81b7d27ec0](https://github.com/user-attachments/assets/2777e2d4-f0b7-43e4-bdc8-72d16c496d4f)


---

## 🧬 BSIM3v3 Model Cards

* Both NMOS and PMOS devices use **LEVEL 7** BSIM3v3 models
* Extracted from a 200nm technology process
* Accurate for transient and DC analysis

---

## 📜 License

This project is licensed under the **MIT License**. See [LICENSE](./LICENSE) for details.

---

## 🙋‍♂️ Author

**Sandeep kumar**
Electronics & Communication Engineer – VLSI Design Enthusiast
Feel free to connect for collaboration or questions!

---

## 📫 Contact

* Email: [your.email@example.com](mailto:your.email@example.com)
* GitHub: [github.com/yourusername](https://github.com/yourusername)


