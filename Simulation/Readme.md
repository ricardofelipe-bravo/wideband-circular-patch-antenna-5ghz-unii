# Simulation

This folder contains the FEKO electromagnetic simulation files for the individual circular patch antenna.

## Software

- **FEKO** (Altair) — Method of Moments (MoM) electromagnetic solver
- Fine mesh configuration with **101 frequency points**
- Frequency sweep: 5.0 – 6.6 GHz

## Contents

- Individual antenna model — circular patch optimized for 5.72 GHz resonance
- Output results — S11 parameter, Smith chart input impedance, 3D radiation pattern

## Key Simulation Parameters

| Parameter | Value |
|---|---|
| Substrate | FR4 (εr = 4.4, tan δ = 0.02, h = 1.575 mm) |
| Solver | Method of Moments (MoM) |
| Frequency points | 101 |
| Port impedance | 50 Ω |
| Resonance frequency | 5.72 GHz |
| Minimum S11 | −37.6 dB |

## Notes

The design started from analytical dimensions calculated using the cavity model, targeting 5.5 GHz. Geometric parameters — patch radius, slot dimensions, and feed line width — were then iteratively adjusted in simulation to shift the resonance to 5.72 GHz and optimize impedance matching within the U-NII band. The final geometry was exported as a STEP file for fabrication.
