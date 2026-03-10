# Simulation

This folder contains the FEKO electromagnetic simulation files for the individual circular patch antenna.

## Software

- **FEKO** (Altair) — Method of Moments (MoM) electromagnetic solver

## Contents

- **CadFEKO file** (`.fek`) — editable antenna model, open this to modify the geometry and re-run the simulation
- **PostFEKO file** (`.feko`) — results project file, open this to visualize S11, Smith chart, and radiation pattern without re-running
- **Solver output** (`.out`) — full solver log generated after running the simulation

## Simulation Configurations

Two frequency sweeps were used depending on the purpose:

| Configuration | Frequency Range | Points | Purpose |
|---|---|---|---|
| Individual antenna model | 3 – 7 GHz | 51 | Design and optimization of the patch element |
| Comparative analysis | 4 – 7 GHz | 101 | Overlay with VNA measurements (see `figures/`) |

## Key Simulation Parameters

| Parameter | Value |
|---|---|
| Substrate | FR4 (εr = 4.4, tan δ = 0.02, h = 1.575 mm) |
| Solver | Method of Moments (MoM) |
| Port impedance | 50 Ω |
| Resonance frequency | 5.72 GHz |
| Minimum S11 | −37.6 dB |

## Notes

The design initially targeted 5.5 GHz following the cavity model procedure. The resonance was intentionally shifted to 5.72 GHz by adjusting the patch radius, slot dimensions, and feed line width. This shift was deliberate — moving the resonance toward the center of the U-NII band (U-NII-2C/2e, U-NII-3, U-NII-4: 5.470–5.925 GHz) increases the operational bandwidth and ensures coverage across the target sub-bands used in high-capacity wireless communications. The final geometry was exported as a STEP file for fabrication (see `cad/`).
