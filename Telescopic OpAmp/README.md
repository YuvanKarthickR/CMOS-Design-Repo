## Telescopic CMOS Operational Amplifier  
**SkyWater 130nm (Sky130A) | Xschem | NGSpice**

---

## Project Overview

This project presents the design and AC performance analysis of a **Telescopic CMOS Operational Amplifier** implemented using the **SkyWater 130nm (Sky130A) Process Design Kit**.

The schematic is created in **Xschem**, and simulations are performed using **NGSpice**. The primary goal is to study the amplifier’s **high-gain behavior**, **frequency response**, and the effect of **bias voltages**, **tail current**, and **transistor sizing (W/L ratios)** on overall performance.

---

## Tools & Technology

- **Xschem** – Schematic capture  
- **NGSpice** – Circuit simulation  
- **SkyWater 130nm (Sky130A) PDK** – CMOS transistor models  
- **Linux** – Simulation environment  

---

## Circuit Architecture

The telescopic operational amplifier is a **single-stage, high-gain topology** that employs **cascoding** to increase output resistance and voltage gain.

### Main Building Blocks

- NMOS differential input pair  
- NMOS and PMOS cascode transistors  
- Constant tail current bias source  
- Single-ended output node  

### Key Characteristics

- High intrinsic voltage gain  
- Low power consumption  
- Limited output swing compared to two-stage op-amps  
- Suitable for high-speed analog applications  

---

## Simulation Setup

### AC Analysis

Small-signal AC analysis is performed to evaluate the gain–frequency response of the amplifier.

```spice
.ac dec 100 1 1e9
