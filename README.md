# circular-patch-antenna-array-unii

Design, simulation, fabrication, and experimental validation of a circular microstrip patch antenna operating in the U-NII band (5.725–5.925 GHz).

The project covers the full development cycle: theoretical design based on the cavity model, electromagnetic simulation in FEKO, PCB layout in EasyEDA, physical fabrication via JLCPCB, and experimental S-parameter measurement using a vector network analyzer.

---

## Key Results

| Parameter | Simulated | Measured |
|---|---|---|
| Resonance frequency | 5.72 GHz | 5.485 GHz |
| Minimum S11 | −37.6 dB | −42.4 dB |
| Bandwidth (S11 < −10 dB) | — | ~4.03 – 5.80 GHz |
| Input impedance | 50 Ω | 50 Ω |

The ~225 MHz downward frequency shift between simulation and measurement is consistent with the typical permittivity variation of commercial FR4 and the slightly greater substrate thickness of the fabricated board (1.6 mm vs. 1.575 mm in simulation). The prototype confirms the design operates within the target U-NII band.

---

## Repository Structure

```
circular-patch-antenna-array-unii/
│
├── simulation/      # FEKO simulation files and results
├── cad/             # STEP and FreeCAD geometry files
├── fabrication/     # Gerber files and EasyEDA layout
├── figures/         # Simulation plots and measurement graphs
├── prototype/       # Photos of the fabricated prototype
└── README.md
```

---

## Design Overview

The antenna is a **circular patch** on FR4 substrate, fed by a microstrip line and coupled through a slot in the ground plane, designed for a 50 Ω input impedance. Key geometric parameters were first calculated analytically using the cavity model and then refined in simulation to shift the resonance into the U-NII band.

### Design Parameters

| Parameter | Value |
|---|---|
| Substrate | FR4 (εr = 4.4, tan δ = 0.02) |
| Substrate thickness | 1.575 mm |
| Patch radius | 7.43 mm |
| Feed line width | 1.84 mm |
| Feed line length | 6.3 mm |
| Slot radius in patch | 4.31 mm |
| Slot width in ground plane | 19 mm |
| Substrate size | 30 × 30 mm |
| Design frequency | 5.5 GHz |
| Resonance frequency (simulated) | 5.72 GHz |

---

## Tools

| Tool | Purpose |
|---|---|
| FEKO (Altair) | Electromagnetic simulation |
| FreeCAD | CAD geometry adjustment |
| EasyEDA | PCB layout and Gerber generation |
| JLCPCB | PCB fabrication |
| Vector Network Analyzer | Experimental S-parameter measurement |

---

## Authors

Ricardo Felipe Bravo Arevalo — `rifebrare@udenar.edu.co`
David Jesus Lara Revelo — `dxddavid17@udenar.edu.co`
Departamento de Ingeniería — Universidad de Nariño, Pasto, Colombia
