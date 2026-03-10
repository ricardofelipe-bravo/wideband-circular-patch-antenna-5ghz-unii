# wideband-circular-patch-antenna-5ghz-unii

Design, simulation, fabrication, and experimental validation of a wideband circular microstrip patch antenna operating across the U-NII bands in the 5 GHz range.

The project covers the full development cycle: theoretical design based on the cavity model, electromagnetic simulation in FEKO, PCB layout in EasyEDA, physical fabrication via JLCPCB, and experimental S-parameter measurement using a vector network analyzer.

---

## Key Results

| Parameter | Simulated | Measured |
|---|---|---|
| Resonance frequency | 5.71 GHz | 5.485 GHz |
| Minimum S11 | −37.57 dB | −42.37 dB |
| Bandwidth (S11 < −10 dB) — full sweep | 1875 MHz (4.0–5.875 GHz) | 1770 MHz (4.03–5.80 GHz) |
| Bandwidth (S11 < −10 dB) — U-NII band only | 405 MHz (5.47–5.875 GHz) | 645 MHz (5.155–5.80 GHz) |
| Input impedance | 50 Ω | 50 Ω |

The ~225 MHz downward frequency shift between simulation and measurement is consistent with the typical permittivity variation of commercial FR4 and the slightly greater substrate thickness of the fabricated board (1.6 mm vs. 1.575 mm in simulation). Despite this shift, the fabricated prototype achieved stronger adaptation and a wider measured bandwidth than predicted, confirming the design operates across the target U-NII sub-bands.

### U-NII Band Coverage (S11 < −10 dB)

| Sub-band | Range | Simulated | Measured |
|---|---|---|---|
| U-NII-2C / U-NII-2e | 5.470–5.725 GHz | Almost complete | Full |
| U-NII-3 | 5.725–5.850 GHz | Full | Full |
| U-NII-4 / DSRC | 5.850–5.925 GHz | Partial | Full |

---

## Repository Structure

```
wideband-circular-patch-antenna-5ghz-unii/
│
├── simulation/      # FEKO simulation files (.fek, .feko, .out)
├── cad/             # STEP and FreeCAD geometry files
├── fabrication/     # DXF files, EasyEDA project and Gerbers
├── figures/         # Simulation plots, VNA data and comparison graphs
├── prototype/       # Photos of the fabricated prototype
└── README.md
```

---

## Design Overview

The antenna is a **circular patch** on FR4 substrate, fed by a microstrip line and coupled through a slot in the ground plane, designed for a 50 Ω input impedance. The design initially targeted 5.5 GHz using the cavity model. The resonance was then intentionally shifted to 5.72 GHz by adjusting the patch radius, slot dimensions, and feed line width — moving it toward the center of the U-NII band to maximize bandwidth coverage across U-NII-2C, U-NII-3, and U-NII-4.

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
| FreeCAD | CAD geometry adjustment and DXF export |
| EasyEDA | PCB layout and Gerber generation |
| JLCPCB | PCB fabrication |
| Vector Network Analyzer | Experimental S-parameter measurement |
| MATLAB | Data processing and simulation vs. measurement comparison |

---

## Authors

Ricardo Felipe Bravo Arevalo — `rifebrare@udenar.edu.co`
David Jesus Lara Revelo — `dxddavid17@udenar.edu.co`
Departamento de Ingeniería — Universidad de Nariño, Pasto, Colombia
