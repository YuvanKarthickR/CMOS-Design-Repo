## 5T Operational Transconductance Amplifier (OTA)  
**Technology:** SKY130 (sg13_lv devices)  
**Tools:** Xschem, Ngspice  
**Supply Voltage:** 1.5 V

---

## Project Overview

This project implements a **5-Transistor Operational Transconductance Amplifier (5T OTA)** using the **SKY130 CMOS process**. The design emphasizes a **low-power**, **minimal-transistor-count** analog amplifier, making it suitable for fundamental analog building blocks and educational VLSI design studies.

The work includes:
- Transistor-level schematic design  
- Biasing and enable-control circuitry  
- AC frequency response analysis  
- DC operating point verification  

---

## OTA Architecture

The 5T OTA consists of the following components:

- NMOS differential input pair  
- PMOS current mirror load  
- Tail current source  
- Enable-controlled biasing network  

This topology provides:
- Low power consumption  
- Compact and area-efficient design  
- Simple biasing, at the cost of limited gain and output swing  

---

## Schematics

### Transistor-Level OTA Schematic

The complete OTA schematic includes the NMOS differential pair, PMOS current mirror load, and the associated biasing circuitry.


*(Transistor-level schematic implemented in Xschem)*

### AC Testbench Schematic

The OTA is evaluated using an AC small-signal testbench created in Xschem.

<img width="1456" height="857" alt="image" src="https://github.com/user-attachments/assets/bba5247a-acf7-4f2b-a6e3-d8fb452248c7" />

**Simulation setup:**
- Differential AC excitation  
- Output load capacitance: **50 fF**  
- Frequency sweep range: **1 kHz – 100 MHz**  

---

## AC Frequency Response

<img width="876" height="633" alt="image" src="https://github.com/user-attachments/assets/f8ce5ea4-0835-4f11-9b27-9305661d6653" />

The AC frequency response of the OTA shows stable single-pole behavior.

### Observed Performance

- **DC Gain:** ~30–32 dB  
- **Dominant Pole:** ~1 MHz (approx.)  
- **Gain Roll-Off:** −20 dB/dec  
- **Unity Gain Frequency:** ~10–20 MHz  

The response confirms stable operation characteristic of a single-stage OTA.

---

## DC Operating Point

DC operating point analysis confirms:
- All transistors operate in saturation  
- Proper bias voltages across both NMOS and PMOS devices  
- Reliable operation under a **1.5 V** supply  

---

## Key Design Parameters

| Parameter | Value |
|--------|-------|
| **Technology** | SKY130 |
| **Supply Voltage** | 1.5 V |
| **Tail Current** | ~4 µA |
| **Load Capacitance** | 50 fF |
| **OTA Type** | Single-stage 5T OTA |

---

## Simulation Details

- **Simulator:** Ngspice  

### Analyses Performed

- `.op` – DC operating point analysis  
- `.ac` – AC frequency response analysis  

Gain and bandwidth are extracted using Ngspice control commands.

---

## Learnings

- Design trade-offs in low-transistor-count OTA architectures  
- Biasing challenges at low supply voltages  
- Dominant pole behavior in single-stage amplifiers  
- Practical AC analysis using Ngspice  

