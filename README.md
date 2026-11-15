# ⚡ BJT Long-Tail Pair (Differential Amplifier) — Hardware & Simulation Design

**Author:** Sithum Sathsara Vitharana &nbsp;|&nbsp; **Reg. No:** E/21/420  
**Course:** EE403 / EE559 — Integrated Analog Electronic Circuits &nbsp;|&nbsp; **Department:** Electrical & Electronic Engineering, University of Peradeniya

---

## 📌 Project Overview

This repository contains the design, simulation, and hardware PCB implementation of a **BJT Long-Tail Pair (Differential Amplifier)** using matched dual transistors (**SSM2212 SMD**).

The project covers theoretical design, circuit simulation across operating regimes in **Qucs**, and schematic capture / PCB layout in **KiCad**.

---

## 🎯 Objectives & Key Observations

1. **Circuit Design & Sizing:** Design a balanced differential pair and current mirror tail for target operating point and power rails ($\pm 5\text{ V}$).
2. **Simulation Analysis (Qucs):**
   - DC transfer characteristics and differential voltage gain ($A_d$)
   - Common-mode response and Common Mode Rejection Ratio (CMRR)
   - Frequency response and $-3\text{ dB}$ bandwidth
   - Maximum undistorted output voltage swing
3. **Hardware Implementation (KiCad PCB):**
   - Professional schematic capture using surface-mount components (SMD 1206 resistors & SOIC-8 dual BJTs)
   - Custom PCB layout for low parasitic interference and symmetry

---

## 🛠️ Components & Tools

| Category | Details |
|----------|---------|
| **Active Components** | SSM2212 matched NPN dual transistor pairs (SOIC-8 SMD) |
| **Passive Components** | SMD 1206 precision resistors ($680\ \Omega$, $1.8\ \text{k}\Omega$, $6.8\ \text{k}\Omega$, $10\ \text{k}\Omega$) |
| **Power Rails** | Dual supply ($\pm 5\text{ V}$) |
| **Circuit Simulation** | [Qucs](http://qucs.sourceforge.net/) (Quite Universal Circuit Simulator) |
| **PCB CAD Tool** | [KiCad](https://www.kicad.org/) (Schematic & 2-Layer PCB Layout) |

---

## 📁 Repository Structure

```
bjt-long-tail-pair/
│
├── kicad/
│   └── long_tail_pair/
│       ├── long_tail_pair.kicad_pro   # KiCad project file
│       ├── long_tail_pair.kicad_sch   # Differential amplifier schematic
│       └── long_tail_pair.kicad_pcb   # 2-layer PCB layout
│
├── simulation/
│   └── qucs/
│       ├── Mini_Project.sch           # Differential gain & DC sweep simulation
│       ├── Mini_Project_B.sch         # AC bandwidth & frequency response
│       ├── Mini_Project_C.sch         # Common-mode voltage & CMRR analysis
│       ├── Mini_Project_D.sch         # Extended parameter variations
│       ├── *.dpl                      # Simulation plot configurations
│       └── netlist.txt                # Exported SPICE/Qucs netlist
│
├── docs/
│   ├── project_report.pdf             # Comprehensive project report (EE403)
│   └── schematic.pdf                  # Exported vector schematic diagram
│
├── .gitignore
└── README.md
```

---

## 🔬 Circuit Architecture

The amplifier consists of:
- **Differential Pair:** Matched NPN pair with emitter degeneration / common-emitter connection.
- **Tail Current Source:** Current mirror configuration using matched SSM2212 transistors to provide high dynamic output impedance, maximizing CMRR.
- **Load:** Matched collector resistors ($R_{C1}, R_{C2}$) delivering balanced differential output ($V_{od} = V_{out1} - V_{out2}$).

---

## 🚀 How to Open & Inspect

### KiCad Project:
1. Install [KiCad 7 or 8](https://www.kicad.org/download/).
2. Open `kicad/long_tail_pair/long_tail_pair.kicad_pro`.
3. Open the schematic (`.kicad_sch`) or PCB editor (`.kicad_pcb`).

### Qucs Simulation:
1. Install [Qucs](http://qucs.sourceforge.net/).
2. Open any schematic file in `simulation/qucs/` (e.g. `Mini_Project.sch`).
3. Press **F2** to simulate and view the data displays.
