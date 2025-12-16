# CMOS Inverter Layout using Magic (SCMOS)

---

## Overview

This repository contains the **physical layout of a CMOS inverter** designed using the **Magic VLSI Layout Tool** with **SCMOS technology**.

The layout represents a basic CMOS inverter structure and is intended for **VLSI layout practice**, **academic laboratory exercises**, and understanding **transistor-level physical design concepts**.

---

## Tools Used

- **Magic VLSI Layout Tool**  
- **SCMOS Technology**

---

## Layout Screenshot

*(CMOS inverter layout screenshot captured using Magic)*  
<img width="1362" height="686" alt="image" src="https://github.com/user-attachments/assets/0e4cbc27-1e5d-4dc6-be27-5b1f6b276085" />


---

## Files Included

| File Name | Description |
|----------|-------------|
| **jas_inverter_layout.mag** | CMOS inverter layout file |

---

## Layout Description

The CMOS inverter layout consists of the following components:

- One **PMOS transistor** placed inside the **n-well** and connected to **VDD**  
- One **NMOS transistor** placed in the **p-substrate** and connected to **GND**  
- A common **gate connection** forming the input node  
- A common **drain connection** forming the output node  

The layout follows **SCMOS design rules** and implements the standard **CMOS inverter topology**.

---

## How to Open the Layout

To open the layout using Magic, run the following command in the terminal:

```bash
magic -T scmos jas_inverter_layout.mag

