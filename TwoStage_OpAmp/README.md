## Two-Stage CMOS Operational Amplifier  
**SkyWater 130nm (Sky130A) | Xschem | NGSpice**

---

## Project Overview

This project focuses on the design and simulation of a **two-stage CMOS operational amplifier** implemented using the **SkyWater 130nm (Sky130A) Process Design Kit**.

The schematic is developed in **Xschem**, and all simulations are carried out using **NGSpice**. The main objective of this work is to analyze the **frequency response**, **voltage gain**, and **stability characteristics**, including **phase margin** and **gain margin**, of a classical two-stage op-amp employing **Miller compensation**.

---

## Tools & Technology

- **Xschem** – Schematic capture  
- **NGSpice** – Circuit simulation  
- **SkyWater 130nm (Sky130A) PDK** – CMOS device models  
- **Linux** – Simulation environment  

---

## Circuit Description

The two-stage operational amplifier consists of multiple functional blocks as described below.

### First Stage

- NMOS differential input pair  
- PMOS current mirror load  
- Provides high differential voltage gain  

### Second Stage

- Common-source amplifier topology  
- Further amplifies the signal from the first stage  
- Contributes to overall voltage gain  

### Compensation

- Miller compensation capacitor connected between:
  - Output of the first stage  
  - Input of the second stage  
- Improves stability and ensures adequate phase margin  

### Biasing

- Constant current sources used  
- Ensures proper operating points for both amplifier stages  

---

## Simulation Setup

The following analyses were performed using **NGSpice**:

- DC Operating Point Analysis  
- AC Analysis (Bode magnitude and phase response)  
- Stability Analysis (Gain Margin and Phase Margin)  

### AC Analysis Command

```spice
.ac dec 100 1 1e7
```
## Schematic 

<img width="1614" height="751" alt="image" src="https://github.com/user-attachments/assets/72b9d910-3e5d-429d-b3c6-5c6fb948c88b" />

## Simulation Results

### DC Gain

- Low-frequency voltage gain ≈ **38 dB**

### Unity Gain Bandwidth (UGB)

- Unity gain frequency ≈ **1 MHz**

### Phase Margin

- Phase at unity gain ≈ **60°**  
- Phase margin ≈ **60°**

### Gain Margin

- Gain at −180° phase ≈ **−10 dB**  
- Gain margin ≈ **10 dB**

---

## Performance Summary

| Parameter | Value |
|--------|-------|
| **DC Gain** | ~38 dB |
| **Unity Gain Bandwidth** | ~1 MHz |
| **Phase Margin** | ~60° |
| **Gain Margin** | ~10 dB |
| **Stability** | Stable |

The amplifier exhibits good stability characteristics due to proper Miller compensation.

---

## Waveforms & Plots

- Bode magnitude plot (Gain vs Frequency)  
 
<img width="938" height="684" alt="image" src="https://github.com/user-attachments/assets/bed83723-8abf-46b5-a181-489f535437f0" />

- Bode phase plot (Phase vs Frequency) 

<img width="940" height="688" alt="image" src="https://github.com/user-attachments/assets/ef44675a-d6d5-4891-87cc-41ed4934d8cd" />

*(Plots obtained from NGSpice AC analysis)*

---

## Learning Outcomes

- Understanding of two-stage CMOS operational amplifier architecture  
- Hands-on experience with the Sky130A Process Design Kit  
- Stability analysis using Bode magnitude and phase plots  
- Estimation of gain margin and phase margin  

---

## License

This project is intended **strictly for educational and academic purposes only**.

