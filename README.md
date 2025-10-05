# 🟢 Asynchronous Buck Converter — 12V → 3.3V @ 3A

![Simulation](https://img.shields.io/badge/LTspice-Simulation-blue)
![Voltage](https://img.shields.io/badge/Input-12V-orange)
![Output](https://img.shields.io/badge/Output-3.3V%20@%203A-green)
![Frequency](https://img.shields.io/badge/Frequency-150kHz-lightgrey)
![License](https://img.shields.io/badge/License-CC0%201.0-blueviolet)

A practical **asynchronous buck converter** designed and simulated in **LTspice**, targeting **12V → 3.3V / 3A** conversion.  
The project demonstrates a **professional power electronics workflow** — from simulation to hardware and firmware integration.

---

## 🔧 Specifications

| Parameter | Value |
|------------|--------|
| Input Voltage | 12 V |
| Output Voltage | 3.3 V |
| Output Current | 3 A |
| Topology | Asynchronous Buck |
| Switching Frequency | 150 kHz |
| Control Type | Open-loop PWM |
| Efficiency (simulated) | ~93% |

---

## 🧩 Schematic Overview

Main circuit nodes:
- `VIN` — Input 12 V supply  
- `SW` — Switching node (MOSFET drain / diode cathode)  
- `VOUT` — Filtered DC output  
- `GND` — Ground reference  

---

## ⚙️ LTspice Setup

1. **MOSFET**: IRLZ44N  
2. **Diode**: MBR360  
3. **Inductor**: 22 µH / 4 A  
4. **Capacitors**: 220 µF + 22 µF ceramic  
5. **PWM Source**: `PULSE(0 12 0 1n 1n 1.83u 6.67u)`  
6. **Load**: 3.3 Ω (≈3 A @ 3.3 V)  

---

## 📊 Simulation Measurements

- Average output voltage  
- Ripple voltage  
- Inductor current ripple  
- Efficiency estimation (Pout / Pin × 100)

---

## 📁 Repository Layout

See folder tree in project root for:
- `LTspice/` — simulation files  
- `Docs/` — schematics & reports  
- `Helpers/` — future sensing/protection circuits  
- `KiCad/` — hardware PCB implementation (next phase)  

---

## 👤 Author

**Al-Moataz Bellah Mohamed Essam Eldin**  
🔗 [LinkedIn](https://www.linkedin.com/in/moataz-ewees/)  
💻 [GitHub](https://github.com/moataz-essam)  
📄 License: CC0 1.0 Universal
